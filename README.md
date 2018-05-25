# Meganha
## Parte hardware

### Material:

* Raspberry Pi model 3
* Módulo Rele 

### Passo 1 - Atualização:

* sudo apt-get update -y
* sudo apt-get upgrade -y

### Passo 2 - Instalação do Apache2 e php

* sudo apt install apache2 libapache2-mod-php7.0.


### Passo 3 - Ligação do Harware (RPi + módulo):

![Hardware - RPi e módulo relé](https://i.imgur.com/Ax7tEyQ.png)


### Passo 4 - Código Python:

```import RPi.GPIO #biblioteca GPIO
imsport sys #biblioteca sys

def incializaBoard():
    GPIO.setmode(GPIO.BOARD)
    GPIO.setwarnings(False)
    
def definePinoComoSaida(numeroPino):
    GPIO.setup(numeroPino, GPIO.OUT)

def escreveParaPorta(numeroPino, estadoPorta):
    GPIO.output(numeroPino, estadoPorta)
    
numeroPino = int(sys.argv[1]) #Ler os parametros
estadoPorta = int(sys.argv[2])


inicializaBorad()
definePinoComoSaida(numeroPino)
escreveParaPorta(numeroPino, estadoPorta)
```

### Passo 5 - Marcação PHP

* [Arquivo php.index](https://drive.google.com/open?id=1C5P7FTTj5g_hb-LXcZPLzfmiKNAOX8uF) 

### Passo 6 - Autorização php - GPIO

O php possui usuários exclusivos para poder trabalhar. Sendo assim é necessário autorizar a biblioteca GPIO para se relacionar com o php.

* sudo usermod -aG gpio www-data
* sudo service apache2 restart
