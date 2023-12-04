# BalancedaorAWS
# Índice
[Introducción.](#introducción)

[Configuración.](#configuración)

[Solucion de errores en el proceso.](#Errores)
# Introducción
En el siguiente manual realizaremos una configuración en 3 niveles que constara e los siguientes apartados:

Un balanceador en capa 1 expuesta a red pública.

Dos servidor web en Backend, capa 2 (red privada).

Un servidor de BBDD en capa 3 (red privada).

# Configuración

### Configuración de VPC

![](fotos/Imagen1.png)

![](fotos/Imagen2.png)

![](fotos/Imagen3.png)

![](fotos/Imagen4.png)

![](fotos/Imagen5.png)

![](fotos/Imagen6.png)
### Balanceador
![](fotos/Imagen7.png)

![](fotos/Imagen8.png)

![](fotos/Imagen9.png)

![](fotos/Imagen10.png)

![](fotos/Imagen11.png)

![](fotos/Imagen12.png)

![](fotos/Imagen13.png)
### Maquinas Backend
![](fotos/Imagen14.png)

![](fotos/Imagen15.png)

![](fotos/Imagen16.png)

![](fotos/Imagen17.png)

![](fotos/Imagen18.png)

![](fotos/Imagen19.png)

![](fotos/Imagen20.png)

![](fotos/Imagen22.png)

![](fotos/Imagen23.png)

![](fotos/Imagen24.png)

![](fotos/Imagen25.png)

![](fotos/Imagen26.png)

### Servidor GGBB

![](fotos/Imagen27.png)

![](fotos/Imagen28.png)

![](fotos/Imagen29.png)

![](fotos/Imagen30.png)
## Certificado

![](fotos/Imagen31.png)


![](fotos/Imagen33.png)


## Errores

# Error del puerto 80 al crear el certificado
#### Al crear el certificado me a dado un fallo del puerto 80 para solucionarlo se debe crear un fichero en sites-available y habilitarlo con sudo a2ensite "fichero".conf.
# A la hora de conectar de una maquina a otra
### deberás dar los siguientes permisos:
```
sudo chmod 400 clave.pem
```
### A continuacion pasaremos la clave de una maquina a otra con el siguiente comando:
```
scp -i "clave.pem" clave.pem admin@192.168.1.240:/home/admin
```
### Una vez realizado podremos conectar con la otra maquina
```
ssh -i "clave.pem" admin@192.168.1.240
```

