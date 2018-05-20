# Meganha
Parte hardware

--------------------------------------------------- PRINCIPAIS COMANDOS RPI--------------------------------------------------------
-----COMANDOS INICIAIS

sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get dist-upgrade -y
sudo rpi-update

-----REMOVER PROGRAMAS OBSOLETOS
sudo apt-get autoremove
sudo apt-get autoclean

-----TIGHTVNCSERVER
sudo apt-get install tightvncserver -y
sudo tightvncserver

-----REAL VNC
sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer

-----OPENCV
sudo apt-get install build-essential
sudo apt-get install python-dev
sudo apt-get install gfortran
sudo apt-get install python-opencv
sudo apt-get install python-matplotlib
sudo apt-get install python-numpy
