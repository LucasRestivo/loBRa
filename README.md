
Este repositório contém a biblioteca LoBRa, que foi baseada nos esforços de tftelkamp (LMIC) e que possibilita o uso otimizado para o cenário brasileiro de IoT em 915 MHz.
O uso de LoBRa permite integração com módulos SX1276/SX1278 e foi validada com setups Arduino/Dragino - Raspberry Pi/Dragino e também com setups entre módulos Heltec ESP32 LoRa.
LoBRa é uma variação de código definido em LMIC que por sua vez contempla padrões utilizáveis para diversas frequências operacionais, mas que não tem necessidade de permanecer no caso brasileiro e, por isso, foi aperfeiçoada para ser utilizada somente nas frequências úteis que são aceitas pelas normas da Agência Nacional de Telecomunicações (Anatel).
Esta biblioteca foi testada e aprovada utilizando a IDE do Arduino v1.8.7.

INSTALAÇÃO

Para instalar esta biblioteca:
Fazer o download do arquivo zip proveniente do github usando o botão "Download ZIP" e instalar usando o IDE ("Sketch", "Include Library", "Adicionar .ZIP Library ...") ou clonar o repositório diretamente para o diretório de bibliotecas do Arduino nos Documentos.
Mais informações em: https://www.arduino.cc/en/Guide/Libraries

CARACTERÍSTICAS

Permite a configuração de canais em frequências dependentes de 915 MHz tanto em módulos com Dragino quanto em módulos ESP32;
Permite utilização de SF7 a SF12 em 915 MHz;
Informa status de envio/recebimento de pacotes;
Sincroniza com servidores web para avaliação de dados;
Ainda não suporta:
Banda superior a 250 kHz;
Mensagens em downlink;
Modulação FSK;

DEPENDÊNCIAS

É preciso habilitar SPI e instalar WiringPi na configuração com Draginos;

CONFIGURAÇÃO

Padrão: SF7, 915 MHz, 125 kHz de banda;

Para o setup Dragino, main.cp deve ser editado para configurar novos valores de SF;

Inserir localização, e-mail e descrição regional para o setup;

Deve-se mudar a Placa na IDE do Arduino quando alternado os setups Draginos/ESP32;

As entradas do gateway no setup ESP32 é configurado somente via web pelo IP do módulo;






