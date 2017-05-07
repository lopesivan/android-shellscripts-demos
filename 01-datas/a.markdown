# Trabalhando com datas

## Alterar a data do *android* usando comando de linha

Seja `adb shell date -s "YYYYMMDD.hhmmss"`


* 22:56:00  (Vinte e duas horas, cinquenta e seis segundos e zero segundos)
* 06  (dia 6)
* 05 (mes cinco)
* 2017 (ano de dois mil e desessete)

```sh
    adb shell date -s "20170506.225600"
```

```sh
adb shell date -s $(date +%Y%m%d.%H%M%S)
```
