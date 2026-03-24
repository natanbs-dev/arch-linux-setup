## arch linux = install


## disk
```bash
cfdisk /dev/nvme0n1
```
> **formatação**
> 	1. crie primeiramente 1G para o /boot
> 	2. entre na opção de type e escolha a tipagem como EFI para essa partição de 1G mencionada antes
> 	3. criado a partição de boot, utilize o resto do espaço para a partição raiz
> 	4. entre na opçaõ [WRITE] e confirme as alterações

### formatando as partições e montando

> tendo feito o passo anterior, confirme com o comando lsblk para verificar se foram criadas as partições corretamente:
```
    lsblk 
```
ou seja:
```
nvme0n1p5 -> /boot/
nvme0n1p6 -> / (raiz)
```

> confirmadas, formate as duas partições seguindo esse padrão, lembrando, primeiramente a partição de boot e em segundo a raiz, que serão colocadas com os números 5 e 6 para exemplo
> 	**Formatando partições: FAT32 e EXT4:**
```
    mkfs.fat -F32 /dev/nvme0n1p5
 	mkfs.ext4 /dev/nvme0n1p6   # mkfs.btrfs - btrfs
```
> **Montagem**    
```
 	mount /dev/nvme0n1p6 /mnt (que será a maior partição, a partição raiz)
 	mkdir /mnt/boot
 	mount /dev/nvme0n1p5 /mnt/boot/
```
> **Consulte:**
```
 	lsblk
```
 > **/mnt no archinstal:**
 > no particionamento, escolha a opção de pre-mounted e, na opção de 
 diretório, seleciona a opção de montagem:
 ```
 /mnt
 ```
