# CONECTAR AO WIFI ATRAVES DO NMCLI
## listar os dispositivos de rede
nmcli device status

## ATIVAR
nmcli radio wifi on 

## ESCANEAR REDES PROXIMAS
nmcli device wifi list 

## CONECTAR
nmcli device wifi connect "NOME DA REDE" password "SENHA"

## VERIFICAR CONEXAO ativar
nmcli connection show --active

