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
Pré-requisitos
Antes de usar este código, é importante garantir que você tenha o ambiente de desenvolvimento Arduino IDE configurado para o ESP32 e que as seguintes bibliotecas estejam instaladas:

"WiFi.h": Para a conexão Wi-Fi.
"PubSubClient.h": Para a comunicação MQTT.
"DHT.h": Para a leitura do sensor DHT11.
"Wire.h" e "LiquidCrystal_I2C.h": Para o controle do display LCD.
Configuração do Código
Configure as informações de rede Wi-Fi, incluindo o SSID (nome da rede) e a senha no início do código:
cpp
Copy code
const char* SSID = "SUA_REDE_WIFI";
const char* PASSWORD = "SUA_SENHA_WIFI";
Defina as informações do servidor MQTT, incluindo o endereço do broker e a porta:
cpp
Copy code
const char* BROKER_MQTT = "SEU_BROKER_MQTT";
int BROKER_PORT = 1883;
Configure os tópicos MQTT para publicação e subscrição:
cpp
Copy code
#define TOPICO_SUBSCRIBE    "/TEF/lamp115/cmd"
#define TOPICO_PUBLISH      "/TEF/lamp115/attrs"
#define TOPICO_PUBLISH_2    "/TEF/lamp115/attrs/l"
#define TOPICO_PUBLISH_3    "/TEF/lamp115/attrs/h"
#define TOPICO_PUBLISH_4    "/TEF/lamp115/attrs/t"
Defina um ID MQTT exclusivo para o seu dispositivo:
cpp
Copy code
#define ID_MQTT  "seu_id_unico"
Uso do Código
Carregue o código no seu ESP32 usando a Arduino IDE ou outra ferramenta de programação compatível.

Conecte o ESP32 à fonte de energia e à rede Wi-Fi configurada.

Certifique-se de que o servidor MQTT configurado no código esteja funcionando e acessível.

O ESP32 começará a ler os sensores e publicar os dados nos tópicos MQTT definidos.

O código também está configurado para responder a comandos via MQTT, como ligar ou desligar um LED (se estiver conectado ao pino D4).

Observações Importantes
Certifique-se de que você tenha acesso a um servidor MQTT funcional para que o código possa se conectar e publicar informações.

Os tópicos MQTT usados no código podem ser personalizados de acordo com as suas necessidades.

Este código é um exemplo educacional e pode ser adaptado para atender a diferentes requisitos de projeto.

Ao utilizar um servidor MQTT público, tenha em mente questões de segurança e privacidade ao publicar informações.

A conexão Wi-Fi deve ser confiável para o funcionamento adequado do código.

Contribuições e Suporte
Este código é fornecido como um exemplo e não inclui todas as funcionalidades possíveis. Você é encorajado a adaptá-lo e estendê-lo para atender aos seus requisitos específicos. Para suporte adicional, consulte a documentação das bibliotecas utilizadas e recursos online relacionados ao ESP32, MQTT e sensores.

Licença
Este código é fornecido sob a licença que governa as bibliotecas utilizadas. Respeite os termos de uso das bibliotecas e, ao compartilhar ou distribuir este código, siga as respectivas diretrizes de licença.
<h1>Colaboradores</h1>
<li>Debora da Silva Amaral RM 550412</li>
<li>Levy Nascimento Junior RM 98655</li>
<li>Lívia Namba Seraphim RM 97819</li>
