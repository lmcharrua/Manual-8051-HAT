O 8051 HAT
**********

é uma placa para ensino sobre o microcontrolador 8051, desenvolvida especialmente para ser utilizada em conjunto com um microcomputador Raspberry Pi 3. Pode também ser utilizada em modo isolado, sendo para tal necessário recorrer a um programador ISP, como por exemplo o USB ASP.

A grande vantagem desta placa é o facto de quase todos os pinos de E/S estarem ligados aos pinos de GPIO do Raspberry Pi, permitindo a interacção entre os dois.

Esta interligação, permite diversos tipos de situações, em que quer o microcontrolador, quer o RPi, podem para actuação ou leitura de sinais. O exemplo mais básico da interacção entre eles é a utilização do RPi para verificar o funcionamento do clássico *blinky* no microcontrolador sem necessitar de recorrer a uma resistência e um LED, bastanto para tal cirar/utilizar um pequeno programa, por exemplo, em *Python* para ler o estado de um pino de GPIO do RPi e apresentar essa informação ao utilizador.

Interligação RPi <-> microcontrolador
=====================================

A tabela apresenta a correspondência entre os pinos E/S do microcontrolador e os GPIO do Raspberry Pi, bem como as suas funcionalidades.

.. tabularcolumns:: |c|c|c|c|c|c|

+------+------+------------+------+-----------+--------+
|       Raspberry Pi       |         8051              |
+------+------+------------+------+-----------+--------+
| GPIO | Pino | Função     | Pino | Porto/bit | Função |
+======+======+============+======+===========+========+
|  02  |  03  | SDA1, I2C  |  42  |   P1.2    |        |
+------+------+------------+------+-----------+--------+
|  03  |  05  | SCL1, I2C  |  43  |   P1.3    |        |
+------+------+------------+------+-----------+--------+
|  04  |  07  | GPCLK0     |  08  |   P3.2    | /INT0  |
+------+------+------------+------+-----------+--------+
|  05  |  29  | GPCLK1     |  10  |   P3.4    |   T0   |  
+------+------+------------+------+-----------+--------+
|  06  |  31  | GPCLK2     |  11  |   P3.5    |   T1   |
+------+------+------------+------+-----------+--------+
|  07  |  26  | CE0_N SPI0 |  12  |   P3.6    |        |
+------+------+------------+------+-----------+--------+
|  08  |  24  | CE1_N SPI0 |  44  |   P1.4    |  /SS   |
+------+------+------------+------+-----------+--------+
|  09  |  21  | MISO SPI0  |  02  |   P1.6    |  MISO  |
+------+------+------------+------+-----------+--------+
|  10  |  19  | MOSI SPI0  |  01  |   P1.5    |  MOSI  |
+------+------+------------+------+-----------+--------+
|  11  |  23  | CLK SPI0   |  03  |   P1.7    |  SCK   |
+------+------+------------+------+-----------+--------+
|  12  |  32  | PWM0       |  40  |   P1.0    |   T2   |
+------+------+------------+------+-----------+--------+
|  13  |  33  | PWM1       |  09  |   P3.3    | /INT1  |
+------+------+------------+------+-----------+--------+
|  22  |  15  |            |  13  |   P3.7    |        |
+------+------+------------+------+-----------+--------+
|  23  |  16  |            |  37  |   P0.0    |        |
+------+------+------------+------+-----------+--------+
