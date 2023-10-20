<h1>Código ESP32 com MQTT e Sensores</h1>
Este código é um exemplo de um programa para o ESP32, que se conecta a uma rede Wi-Fi, comunica-se com um servidor MQTT e realiza a leitura de sensores DHT11 e um sensor de luminosidade.

<h2>Resumo do Código</h2>
O código consiste em um conjunto de funções e configurações para realizar as seguintes tarefas:
<br></br>
Inicialização das conexões Wi-Fi, MQTT e configuração dos tópicos MQTT.
Leitura de sensores:
<li>Sensor DHT11 para umidade e temperatura.</li>
<li>Sensor de luminosidade.</li>
<li>Publicação dos dados dos sensores nos tópicos MQTT apropriados.</li>
<li>Controle de um LED e exibição de informações em um display LCD.</li>
<li>Função de callback para lidar com comandos recebidos via MQTT.</li>
<br></br>
<h2>Pré-requisitos:</h2>
As seguintes bibliotecas estejam instaladas:
<li>"WiFi.h": Para a conexão Wi-Fi.</li>
<li>"PubSubClient.h": Para a comunicação MQTT.</li>
<li>"DHT.h": Para a leitura do sensor DHT11.</li>
<li>"Wire.h" e "LiquidCrystal_I2C.h": Para o controle do display LCD.</li>
<br></br>
<h2>Para acessar o MQTT Mobile</h2>
BROKER = 46.17.108.113
BROKER_PORT = 1883
<h2>Para configurar os tópicos MQTT para publicação e subscrição:</h2>
(sem as "aspas")
<li>"/TEF/lamp115/cmd"</li>
<li>"/TEF/lamp115/attrs"</li>
<li>"/TEF/lamp115/attrs/l"</li>
<li>"/TEF/lamp115/attrs/h"</li>
<li>"/TEF/lamp115/attrs/t"</li>

<h2>Como utilizar o código:</h2>
<li>Carregue o código no seu ESP32 usando a Arduino IDE ou outra ferramenta de programação compatível.</li>
<li>Conecte o ESP32 à fonte de energia e à rede Wi-Fi configurada.</li>
<li>Certifique-se de que o servidor MQTT configurado no código esteja funcionando e acessível.</li>
<li>O ESP32 começará a ler os sensores e publicar os dados nos tópicos MQTT definidos.</li>
<li>O código também está configurado para responder a comandos via MQTT, como ligar ou desligar um LED (se estiver conectado ao pino D4).</li>

<h2>Colaboradores</h2>
<li>Debora da Silva Amaral RM 550412</li>
<li>Levy Nascimento Junior RM 98655</li>
<li>Lívia Namba Seraphim RM 97819</li>
