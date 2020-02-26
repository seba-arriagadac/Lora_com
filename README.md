# Lora_com
Pruebas con modulos sx1278 (XL1278-SMT) a 433 MHz usando nodeMCU v2, arduino IDE y vscode.
## Comenzando

### Lista de Materiales
- Módulo sx1278 (XL1278-SMT) con su antena
- Adaptador de pines de con separación de 1 _mm_ a 2.54 _mm_ (para conectar el módulo a una protoboard)
- Protoboard
- Cables de conexión (o jumpers)
- NodeMCU - Amica (NodeMCU v2)
- Cables microUSB para conectar la tarjeta.
### Armado
Las conexiones del módulo se describen a continuación.
__IMPORTANTE!!!
Antes de conectar el módulo es necesario conectar la antena, de no hacerlo podría quemarse el chip del módulo.__
las conexión se describe gráficamente como se muestra a continuación.
```
    TRANSMISOR                       RECEPTOR
_______     _________          _______     _________
N   GND|---|GND      |        |N   GND|---|GND      |
o    D0|---|RST   S  |        |o    D0|---|RST   S  |
d    D2|   |DIO0  X  |        |d    D2|---|DIO0  X  |
e    D8|---|NSS   1  |        |e    D8|---|NSS   1  |
M    D5|---|SCLK  2  |        |M    D5|---|SCLK  2  |
C    D7|---|MOSI  7  |        |C    D7|---|MOSI  7  |
U    D6|---|MISO  8  |        |U    D6|---|MISO  8  |
    VCC|---|VCC      |        |    VCC|---|VCC      |
______ |   | _______ |        |______ |   | _______ |
```
__NOTA
Se deben conectar las tierras del módulo para que este funcione.__

### Software Necesario

* [Drivers CP210x](https://www.silabs.com/community/interface/knowledge-base.entry.html/2016/12/30/downloading_cp210xd-ek07) - Para que windows reconozca la tarjeta NodeMCU
* [Arduino IDE](https://www.arduino.cc/en/main/software) - Para compilar el código
* [Visual Studio Code](https://code.visualstudio.com/) - Para escribir el código

## Imagenes de la conexión.
![Configuracion física del módulo transmisor](https://github.com/seba-arriagadac/Lora_com/blob/master/implementacion/TX_config.jpeg) ![Configuracion física del módulo receptor](https://github.com/seba-arriagadac/Lora_com/blob/master/implementacion/RX_config.jpeg)


## la librería usada está en
[sandeepmistry](https://github.com/sandeepmistry/arduino-LoRa)
