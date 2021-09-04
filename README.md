# Cambiar puerto por defecto de ssh


Editar archivo de configuración de ssh, para cambiar el puerto por defecto y dejar disponible el puerto 22 para el honeypot 

```bash
sudo vim /etc/ssh/sshd_config
```
Agregar la siguiente linea

```bash
Port 222
```
Reiniciar ssh

```bash
sudo service ssh restart
```



# Clonar el repositorio


clonar

```bash
git clone https://github.com/SrEnrique/SrEnrique-docker-ssh-honeypot.git
```

Ejecutar Docker 

```bash
cd docker-ssh-honypot
sudo docker-compose up -d
```

Leer los logs de Docker 

```bash
sudo docker logs -f $(sudo docker ps -f name=ssh_honeypot_webapp_1 -q)
```


## Referencias 

[hub.docker.com wildwildangel/ssh-honeypotd](https://hub.docker.com/r/wildwildangel/ssh-honeypotd)