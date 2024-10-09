CARRINHO E LED CONTROLADOS PELO MINDWAVE

DESCRIÇÃO: Nosso projeto utiliza o dispositivo Mindwave para captar ondas cerebrais e medir o nível de concentração. A partir disso, desenvolvemos um carrinho básico com Arduino e motores DC para se movimentar, juntamente com o módulo HC-05 para conexão Bluetooth com o Mindwave. Além do carrinho, integramos 4 LEDs em sequência numa protoboard. Usando também um Arduino e o módulo HC-05, os LEDs acendem gradualmente conforme o nível de concentração do usuário aumenta. O carrinho começa a se mover para frente quando a concentração atinge 55%. Para conectar o Mindwave aos módulos HC-05, utilizamos comandos AT para obter a serial do Mindwave.

BIBLIOTECAS UTILIZADAS: O código foi desenvolvido utilizando a linguagem Arduino e algumas bibliotecas, como:

cpp
Copiar código
#include <SoftwareSerial.h>
#include <Mindwave.h>
-> A biblioteca Mindwave.h pode ser baixada como arquivo zip e adicionada ao aplicativo Arduino.

COMANDOS AT:
AT+UART=57600,0,0
AT+ROLE=1
AT+PSWD="0000"
AT+CMODE=0
AT+BIND=xxxx,xx,xxxxxx (endereço MAC do Mindwave, obtido conectando o dispositivo a outro via Bluetooth)
AT+IAC=9E8B33
AT+CLASS=0
AT+INQM=1,9,48
CÓDIGO DOS LEDS: Disponível no arquivo "ComandoDosLEDS.ino".

CÓDIGO DO CARRINHO: Disponível no arquivo "ComandoDoCarrinho.ino".

COMPONENTES UTILIZADOS:

2 Arduinos
2 Motores DC
Dispositivo Mindwave
Chassi do carrinho
Fonte de alimentação (Bateria 9V para Arduino)
4 pilhas AA para alimentar os motores DC
4 LEDs
Protoboard
Jumpers
Resistores
Shield Ponte H L298n
FUNCIONAMENTO: O Mindwave capta a atividade elétrica do cérebro e calcula o nível de concentração do usuário. Esse dado é enviado ao Arduino, que controla os motores do carrinho. À medida que a concentração aumenta, o carrinho avança; se diminuir, o carrinho para. Com os LEDs, o processo é similar: quanto maior a concentração, mais LEDs acendem, e, com a queda da concentração, eles se apagam.

OBJETIVOS:

Demonstrar a relação entre a atividade cerebral e ações físicas.
Proporcionar uma experiência educativa sobre neurociência e tecnologia.
Explorar as múltiplas aplicações possíveis para assistência a pessoas com necessidades especiais, como o desenvolvimento de uma mão robótica para indivíduos que tenham perdido a mão.
RESULTADOS ESPERADOS:
Mostrar o potencial da tecnologia para transformar vidas e criar soluções adaptáveis para necessidades especiais, alinhadas à temática pós-apocalíptica da Fecart.
