# Meganha
##Parte hardware

###Material:

* Raspberry Pi model 3
* Módulo Rele 

###Passo 1 - Atualização:

* sudo apt-get update -y
* sudo apt-get upgrade -y

###Passo 2 - 

* 


###Passo ?? - Ligação do Harware (RPi + módulo):

![Hardware - RPi e módulo relé](https://i.imgur.com/Ax7tEyQ.png)


###Passo ? - Código Python:

`import RPi.GPIO #biblioteca GPIO
imsport sys #biblioteca sys`

`def incializaBoard():
    GPIO.setmode(GPIO.BOARD)
    GPIO.setwarnings(False)`
    
`def definePinoComoSaida(numeroPino):
    GPIO.setup(numeroPino, GPIO.OUT)

def escreveParaPorta(numeroPino, estadoPorta):
    GPIO.output(numeroPino, estadoPorta)
    
numeroPino = int(sys.argv[1]) #Ler os parametros
estadoPorta = int(sys.argv[2])

inicializaBorad()
definePinoComoSaida(numeroPino)
escreveParaPorta(numeroPino, estadoPorta)`
