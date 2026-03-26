## iwctl, erro quanto ao powered da placa

## primeiramente, verifica as placas detectadas
```
iwctl
list devices
```

## comando para ligar a placa detectada
```
iwctl
device wlan5 set-property Powered on
adapter phy5 set-property Powered on
```

### em sequencia, procure pelas redes próximas
```
station wlan5 get-networks
```
caso não funcione, use 
```
station wlan5 scan
```

## se ainda persistir o erro, use rfkill
```
rfkill list
rfkill unblock wifi
iwctl
list devices
```
