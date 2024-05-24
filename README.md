# FECAP - Fundação de Comércio Álvares Penteado

<p align="center">
<a href= "https://www.fecap.br/"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhZPrRa89Kma0ZZogxm0pi-tCn_TLKeHGVxywp-LXAFGR3B1DPouAJYHgKZGV0XTEf4AE&usqp=CAU" alt="FECAP - Fundação de Comércio Álvares Penteado" border="0"></a>
</p>

# Bueiro Inteligente 

## Em busca de estágio 

## Integrantes: <a href="https://www.linkedin.com/in/anderson-fernandez-2aa13924b/">Anderso Yavi Fernandez</a>, <a href="https://www.linkedin.com/in/gustavocastro01/">Gustavo de Souza Castro</a>, <a href="">Kaique Neres de Oliveira</a>, <a href="">Jorge Augusto Lourenço Ignacio. </a>

## Professores Orientadores: <a href="https://www.linkedin.com/in/victorbarq/">Victor Bruno Alexander Rosetti de Quiroz</a>, <a href="https://www.linkedin.com/in/adriano-valente-534576135/">Adriano Valente </a>

## Descrição
<p>
  Criar um sistema de monitoramento em tempo real capaz de identificar o nível de resíduos presentes nos bueiros. Dessa forma, sendo possível evitar alagamentos e enchentes nas cidades
</p>

<p align="center">
<img src="https://github.com/2024-1-NADS1-A/Projeto3/assets/164703668/e8346331-0ac0-41cd-8e7a-a6163d760798.png" alt="NOME DO JOGO" border="0">
  Projeto feito por <a href="">Anderson Fernandez</a>, <a href =""> Gustavo Castro </a>, <a>Kaique Neres</a>, <a>Jorge Ignacio.</a>
</p>


Sobre o projeto
<p>Em São Paulo, são produzidas cerca de 20 mil toneladas de lixo por dia. Durante as chuvas, parte desse lixo é arrastado para bueiros, rios e córregos, sendo um dos principais causadores de alagamentos na cidade. Nosso projeto visa resolver este problema de bueiros entupidos utilizando um cesto com um sensor embutido. 
  
Este sensor será capaz de monitorar a evasão de água e calcular o volume de resíduos nos bueiros. Quando o bueiro estiver cheio, o sistema enviará um alerta para as equipes de limpeza, permitindo a intervenção antes que ocorra um alagamento. Esperamos que este sistema seja implementado de forma eficiente e utilizado com sucesso na cidade de São Paulo.

## 🛠 Estrutura de pastas

-Raiz<br>
|<br>
|-->documentos<br>
  &emsp;|-->antigos<br>
  &emsp;|Documentação.docx<br>
|-->executáveis<br>``
|-->imagens<br>
|-->src<br>
 
|readme.md<br>

A pasta raiz contem dois arquivos que devem ser alterados:

<b>README.MD</b>: Arquivo que serve como guia e explicação geral sobre seu projeto. O mesmo que você está lendo agora.

Há também 4 pastas que seguem da seguinte forma:

<b>documentos</b>: Toda a documentação estará nesta pasta.

<b>imagens</b>: Imagens do sistema

<b>src</b>: Pasta que contém o código fonte.
## 🛠 Ferramentas Utilizadas 
<h3>Equipamentos:</h3>

- Protoboard<br>

- Esp32<br>

- Sensor Ultrassonico HC-SR04<br>

- Cabos Jumper Macho e Fêmea<br>

- Cesto coletor<br>
<h3>Softwares:</h3>

- Arduino IDE<br>
  
- Blynk<br>

## 🛠 Instalação

<h2>Arduino IDE<h2>

Instalar o Arduino IDE: Visite o site oficial do Arduino em www.arduino.cc e vá para a seção "Software". Escolha a versão adequada do Arduino IDE para o seu sistema operacional (Windows, Mac, Linux) e faça o download do instalador. Depois de baixar o arquivo, execute-o e siga as instruções do instalador para concluir o processo de instalação.<br>

Instalar o suporte ao ESP32 no Arduino IDE: Após instalar o Arduino IDE, abra-o e vá para o menu "File" -> "Preferences". Na janela de preferências, cole o seguinte URL no campo "Additional Board Manager URLs": https://dl.espressif.com/dl/package_esp32_index.json. Clique em "OK" para fechar a janela. 
Em seguida, vá para o menu "Tools" -> "Board" -> "Boards Manager...". Na caixa de pesquisa, digite "ESP32" e instale o pacote "esp32" desenvolvido pela Espressif Systems.<br>

Selecionar o ESP32 como placa: Com o suporte do ESP32 instalado, vá para o menu "Tools" -> "Board" e selecione a placa "ESP32 Dev Module".<br>

Conectar o ESP32 ao computador: Conecte o ESP32 ao seu computador usando um cabo USB. Certifique-se de que o driver USB correto seja instalado automaticamente pelo sistema operacional.<br>

Verificar a porta serial: Vá para o menu "Tools" -> "Port" e selecione a porta serial que corresponde ao seu ESP32. Esta porta pode variar dependendo do sistema operacional e do número de dispositivos conectados.<br>

<h2>Blynk:<h2>

Crie uma conta no Blynk: Abra o aplicativo/site Blynk e crie uma conta.

Crie um novo projeto: Após fazer login, clique em "Novo Projeto" e dê um nome ao seu projeto. Selecione o tipo de conexão que você usará (Wi-Fi, Bluetooth, etc.) e o dispositivo que você está usando (ESP32, Arduino, Raspberry Pi, etc.).<br>

Obtenha seu Token de Autenticação: Após criar o projeto, você receberá um Token de Autenticação via e-mail. Este token é necessário para conectar o seu dispositivo ao projeto no aplicativo Blynk.<br>

Configure o hardware: No seu dispositivo (como o ESP32), instale a biblioteca Blynk no Arduino IDE, como mencionado anteriormente. Use o Token de Autenticação recebido para configurar o código do seu dispositivo para se conectar ao projeto no Blynk.<br>

Conecte o dispositivo ao projeto: No código do seu dispositivo, insira o Token de Autenticação e as configurações de conexão Wi-Fi. Faça o upload do código para o seu dispositivo.<br>

Visualize e controle seu dispositivo: Arraste e solte os widgets desejados na tela do projeto para controlar e visualizar seu dispositivo remotamente.<br>

Teste e ajuste:  Se necessário, faça ajustes no código ou no layout do aplicativo para atender às suas necessidades.


## 🗃 Histórico de lançamentos

A cada atualização os detalhes devem ser lançados aqui.

* 0.2.1 - 23/01/2024
    * MUDANÇA: Alteramos o Cesto e projeto finalizado no github
* 0.2.0 - 17/05/2024
    * MUDANÇA: Ajustes no código sobre o tipo de alerta e a distancia referenciada.
* 0.1.0 - 10/05/2024
    * Os primeiros testes com o sensor ultrassonico, funcionando perfeitamente (@Anderson)
* 0.0.1 - 03/05/2024
    * Iniciando o trabalho

## 📋 Licença/License

 <p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/2024-1-NADS1-A/Projeto3">Bueiro Inteligente</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/2024-1-NADS1-A/Projeto3">FECAP, ANDERSON YAVI FERNANDEZ, KAIQUE NERES DE OLIVEIRA, GUSTAVO DE SOUZA CASTRO E JORGE AUGUSTO LOURENÇO IGNÁCIO</a> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Creative Commons Attribution 4.0 International<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p>

## 🎓 Referências

Aqui estão as referências usadas no projeto.

1. <https://docs.arduino.cc/tutorials/projects/control-your-iot-cloud-kit-via-blynk/>
2. <https://blynk.io/blog/step-by-step-video-guide-to-making-your-first-project-on-the-new-blynk>
3. <https://www.youtube.com/watch?v=ZQT8sIrXTnA>
4. <https://blog.brkambiental.com.br/enchentes-no-brasil/>
5. <https://www.crescerengenharia.com/post/monitorando-tanques-agua-esp32>
6. <https://www.crescerengenharia.com/post/google-sheets-esp32-enviando-email-sms>
7. <https://www.crescerengenharia.com/post/aprenda-como-usar-o-esp32-para-publicar-dados-no-google-sheets>
