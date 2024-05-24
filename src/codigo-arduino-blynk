#define BLYNK_TEMPLATE_ID           "TMPL2RVpshIHi"
// Define o ID do template do Blynk
#define BLYNK_TEMPLATE_NAME         "Quickstart Template"
// Define o nome do template do Blynk
#define BLYNK_AUTH_TOKEN            "GyjnOnhSMSmUNHAydoZayj8MoFHzGBYP"
// Define o token de autenticação do Blynk
#define BLYNK_PRINT Serial 
// Define que as mensagens de depuração do Blynk serão impressas no monitor serial

//Inclusão das bibliotecas:
#include <WiFi.h>  // Inclui a biblioteca para conexão WiFi
#include <WiFiClient.h>  // Inclui a biblioteca para cliente WiFi
#include <BlynkSimpleEsp32.h>  // Inclui a biblioteca do Blynk para ESP32
#include <Ultrasonic.h> // Inclui a biblioteca para o sensor ultrassônico


Ultrasonic ultrasonic(18, 5); // Inicializa o sensor ultrassônico, definindo os pinos de trigger (18) e echo (5)


char ssid[] = "CLARO_2G4B95C5";
// Define o SSID (nome) da rede WiFi usada no caso, substitua pela sua.

char pass[] = "E74B95C5";
// Define a senha da rede WiFi

float distance; // Variável para armazenar a distância medida pelo sensor ultrassônico

String estado; // Variável para armazenar o estado (nível de ocupação)

int tamanhoTotal = 23; // Define o tamanho total do recipiente em cm

float valorPorcentagem; // Variável para armazenar a porcentagem de ocupação calculada

BlynkTimer timer; // Inicializa o timer do Blynk

BLYNK_WRITE(V0)
{
  int value = param.asInt(); // Lê o valor do virtual pin V0 como inteiro

  Blynk.virtualWrite(V1, value); // Escreve o valor no virtual pin V1
  
}
//CONEXÃO COM O BLYNK
BLYNK_CONNECTED()
{
  Blynk.setProperty(V3, "offImageUrl", "https://static-image.nyc3.cdn.digitaloceanspaces.com/general/fte/congratulations.png");
  // Define a URL da imagem para o estado "off" do widget no virtual pin V3

  Blynk.setProperty(V3, "onImageUrl",  "https://static-image.nyc3.cdn.digitaloceanspaces.com/general/fte/congratulations_pressed.png");
  // Define a URL da imagem para o estado "on" do widget no virtual pin V3

  Blynk.setProperty(V3, "url", "https://docs.blynk.io/en/getting-started/what-do-i-need-to-blynk/how-quickstart-device-was-made");
  // Define a URL associada ao widget no virtual pin V3
}

void myTimerEvent()
{
  Blynk.virtualWrite(V2, millis() / 1000);
  // Escreve o tempo decorrido (em segundos) no virtual pin V2
}
void getDados()
{
  distance = ultrasonic.read();
  // Lê a distância medida pelo sensor ultrassônico

  valorPorcentagem = distance / tamanhoTotal * 100;
  // Calcula a porcentagem de ocupação

  float porcentFinal = 100 - valorPorcentagem;
  // Calcula a porcentagem final invertida

  Serial.print(valorPorcentagem);
  // Imprime a porcentagem no monitor serial

  Serial.print(" - Distância em cm: ");
  // Imprime uma mensagem no monitor serial

  Serial.print(distance);
  // Imprime a distância medida no monitor serial

  if(distance <= 3){
    estado = "URGENTE!!!";
    // Define o estado como "URGENTE!!!" se a distância for menor ou igual a 3 cm

    Serial.print(" - ");
    // Imprime uma mensagem no monitor serial

    Serial.println(estado);
    // Imprime o estado no monitor serial
} else if(distance < 6){
    estado = "Cheio";
    // Define o estado como "Cheio" se a distância for menor que 6 cm

    Serial.print(" - ");
    Serial.println(estado);
} else if(distance < 9){
    estado = "Médio";
    // Define o estado como "Médio" se a distância for menor que 9 cm

    Serial.print(" - ");
    Serial.println(estado);
} else if(distance < 11){
    estado = "Baixo";
    // Define o estado como "Baixo" se a distância for menor que 11 cm

    Serial.print(" - ");
    Serial.println(estado);
} else{
    estado = "Vazio";
    // Define o estado como "Vazio" se a distância for maior ou igual a 11 cm

    Serial.print(" - ");
    Serial.println(estado);    
}

  Blynk.virtualWrite(V5, estado);
  // Escreve o estado no virtual pin V5

  Blynk.virtualWrite(V4, porcentFinal);
  // Escreve a porcentagem final no virtual pin V4

  delay(1000);
  // Aguarda 1 segundo
}
void setup()
{
  Serial.begin(115200);
  // Inicia a comunicação serial a 115200 bps

  Blynk.begin(BLYNK_AUTH_TOKEN, ssid, pass);
  // Conecta ao Blynk usando o token de autenticação e as credenciais WiFi

  timer.setInterval(1000L, myTimerEvent);
  // Configura o timer para chamar a função myTimerEvent a cada 1 segundo

  timer.setInterval(100L, getDados);
  // Configura o timer para chamar a função getDados a cada 100 milissegundos
}
void loop()
{
  Blynk.run();
  // Mantém o loop principal do Blynk funcionando

  timer.run();
  // Mantém os timers funcionando continuamente
}





