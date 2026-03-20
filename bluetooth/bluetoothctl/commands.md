# comandos de conexao bluetooth atraves do terminal

## instalacao & configuracao

sudo pacman -Syy bluez bluez-utils 

sudo systemctl  enable --now bluetooth.service

## conexao

bluetoothctl
power on 
scan on
pair <MAC_ADDRESS>
connect <MAC_ADDRESS>

## *detalhe

Para automatizar e mais fácil, use o atalho 'CTRL + R' com as palavras chaves 'remove e connect' por conta que estará armazenado o MAC_ADDRESS do dispositivo bluetooth
