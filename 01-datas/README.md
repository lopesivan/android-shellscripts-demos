# Trabalhando com datas

## Alterar a data do **android** usando comando de linha

Para tanto, vamos utilizar o comando adb, para se comunicar com nosso
dispositivo android.

Seja `adb shell date -s "YYYYMMDD.hhmmss"`

No meu computador tenho a seguinte saída do comando date:
```sh
    $ date +%Y%m%d.%H%M%S
    20170507.033758
```

### Vamos para nossas tentativas de alterar a a data/hora do sistema.

* O comando adb recebendo como parametro a data a ser configurada.

```sh
    adb shell date -s $(date +%Y%m%d.%H%M%S)
```
resultado: não funcionou

* Entrando no shell do android e tentando configurar manualmente.

```sh
$ adb shell
$ date
Fri Feb 25 06:43:15 BRT 2011
$ date -s "20170507.033758"
Fri Feb 25 06:43:27 BRT 2011
$ date
Fri Feb 25 06:43:34 BRT 2011
$
$ su
# date -s "20170507.033758"
Sun May  7 03:37:58 BRT 2017
# $
```

resultado: funcionou somente quando ativamos o modo de **root**.


