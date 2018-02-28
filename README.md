# BloqueoBloqueo
Script bash para bloqueo de IPs por medio de IPTABLES

El artículo original para crear el script está aquí -> [Banear IPs en linux automáticamente con IPTABLES](http://rolandocaldas.com/linux/script-banear-ips-en-linux-iptables)

## Opciones

### Script como servicio

El script se ejecuta como un servicio así que es necesario iniciar el script para usarlo.

Para iniciar el servicio ejecutar:


```bash
/etc/bloqueobloqueo/bloqueobloqueo start
```

### Lista de IPs baneadas automáticamente

El script lee un archivo de texto y bloquea todas las direcciones IP de este archivo cuando el script inicia

### Banear una nueva IP

Puedes agregar una nueva IP a la lista de IPs baneadas ejecutando el siguiente comando:

```bash
/etc/bloqueobloqueo/bloqueobloqueo ban [ip]
```

### Desbanear una IP

Puedes remover una IP de la lista de baneadas corriendo el siguiente comando:

```bash
/etc/bloqueobloqueo/bloqueobloqueo unban [ip]
```

### Geolocalizar una IP

Puedes localizar el país de origen de una dirección IP con el siguiente comando:

```bash
/etc/bloqueobloqueo/bloqueobloqueo geoip [ip]
```
### Bloquear un rango de IP por país

Después de conocer el código de país puedes bloquearlo con el siguiente comando (Cuidado aquí ya que si bloqueas tu propio país o el país de tu proveedor VPS no podrás acceder a tu servidor):

```bash
/etc/bloqueobloqueo/bloqueobloqueo geoblock [código de país]
```

### Detener el Firewall

Puedes detener el Firewall (y remover todas las reglas)si ejecutas el siguinete comando:

```bash
/etc/bloqueobloqueo/bloqueobloqueo stop
```

### Reiniciar el Firewall

Puedes reiniciar el firewall con el siguiente comando:

```bash
/etc/bloqueobloqueo/bloqueobloqueo restart
```

## Version info

La actual es la versión v0.2 , se agregó en esta versión la geolocalización de país al introducir una dirección IP y la posibilidad de realizar un bloqueo por país, para la instalación de GeoIP se pueden basar en este artículo -> https://juantrucupei.wordpress.com/2015/07/01/iptables-con-geoip/
