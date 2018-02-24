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

La actual es la versión v0.1.1 , una ligera modificación de la original.
