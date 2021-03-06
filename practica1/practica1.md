# Práctica 1: Preparación de las herramientas

 
*En esta práctica el objetivo es configurar las máquinas virtuales para trabajar en
prácticas posteriores, asegurando la conectividad entre dichas máquinas.
Como resultado de la práctica 1 se mostrarán dos máquinas funcionando al
profesor en clase (accesos con curl para solicitar páginas web sencillas, así como el
acceso por SSH entre ambas máquinas).
Específicamente, hay que llevar a cabo las siguientes tareas:*
1. *acceder por ssh de una máquina a otra*
2. *acceder mediante la herramienta curl desde una máquina a la otra*

-------

En mi caso he decidido emplear **VMWare Workstation** para la realización de las prácticas. La instalación de Ubuntu Server ha sido realizada como se indica en el guión. 

El primer paso para poder conectar ambas máquinas es conocer la IP mediante
`ifconfig`

### IP de la primera máquina
![ip1](./img/ip1.png)
### IP de la segunda máquina
![ip2](./img/ip2.png)

En los siguientes pasos, las máquinas quedarán identificadas por su dirección IP.

-----
## Acceso mediante SSH

Para acceder a una máquina por SSH esta debe estar operativa y conocer su dirección IP y credenciales de acceso. La conexión se realiza mediante `ssh <user>@<ip>`

### Primera máquina conectada a la segunda
`ssh ubuserver@172.16.164.128`

![ssh1](./img/ssh1to2.png)

### Segunda máquina conectada a la primera
`ssh ubuserver@172.16.164.129`

![ssh2](./img/ssh2to1.png)

----
## Acceso mediante CURL

En este caso se procederá a descargar un archivo HTML del servidor web desplegado en la máquina. Para ello se empleará `curl http://<ip>/hola.html`

### Primera máquina conectando a la segunda
`curl http://172.16.164.128/hola.html`

![ssh1](./img/curl1to2.png)

### Segunda máquina conectando a la primera
`curl http://172.16.164.129/hola.html`

![ssh2](./img/curl2to1.png)

-----
[Práctica 2](../practica2/practica2.md)
