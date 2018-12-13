O 8051 HAT
**********

é uma placa para ensino sobre o microcontrolador 8051, desenvolvida especialmente para ser utilizada em conjunto com um microcomputador Raspberry Pi 3. Pode também ser utilizada em modo isolado, sendo para tal necessário recorrer a um programador ISP, como por exemplo o USB ASP.

A grande vantagem desta placa é o facto de quase todos os pinos de E/S estarem ligados aos pinos de GPIO do Raspberry Pi, permitindo a interacção entre os dois.

Esta interligação, permite diversos tipos de situações, em que quer o microcontrolador, quer o RPi, podem para actuação ou leitura de sinais. O exemplo mais básico da interacção entre eles é a utilização do RPi para verificar o funcionamento do clássico *blinky* no microcontrolador sem necessitar de recorrer a uma resistência e um LED, bastanto para tal cirar/utilizar um pequeno programa, por exemplo, em *Python* para ler o estado de um pino de GPIO do RPi e apresentar essa informação ao utilizador.