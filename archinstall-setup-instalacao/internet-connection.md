## corregar o tipo de teclado em br-abnt2
```
loadkeys br-abnt2
```
## conectar a internet
```
iwctl
device list
station wlan5 get-networks
station wlan5 connect NETWORK.SSID
```
## verifique se conectou
```
station wlan5 show
```
