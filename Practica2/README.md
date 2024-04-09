# **Práctica 1**

## **Manual Técnico📚**


### **0. Topología de Red📡**

La topología de red para esta práctica es de tipo estrella, en la cual se tiene un nodo central que es el servidor y los nodos periféricos que son los clientes. Se adjunta la imagen de la topología de red.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 214950.png" width="600"/></div>

### **1. Configuracion de las VPCs📡**

Para la configuración de las VPCs se utilizó el siguiente formato para las ip's de las VPCs:
```
192.168.xy.zw
```

Donde:
```
x & y: Son los ultimos dos dígitos de mi carnet.
```
```
z: Es el número de nivel en donde se encuentra la VPC.
```

```
w: Es el número de la VPC en el nivel.
```

-  **Nivel 1: Recursos Humanos**

En esta área se encuentra el departamento de Recursos Humanos, se adjunta la configuración de la VPC.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 223259.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 223251.png" width="300"/></div>

<br>

- **Nivel 1: Administración**

En esta área se encuentra el departamento de Administración, se adjunta la configuración de la VPC.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224555.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224544.png" width="300"/></div>

<br>

- **Nivel 1: Gerencia/Secretaria**

En esta área se encuentra el departamento de Gerencia y su Secretaria, se adjunta la configuración de la VPC.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224608.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224601.png" width="300"/></div>


<br>

- **Nivel 1: Atención al cliente**

En esta área se encuentra el departamento de Atención al cliente, se adjunta la configuración de la VPC.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224624.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224616.png" width="300"/></div>


<br>

- **Nivel 2: Oficionas "A"**

En esta área se encuentra el departamento de Oficinas "A", se adjunta la configuración de la VPC.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224714.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224707.png" width="300"/></div>

<br>

- **Nivel 2: Oficionas "B"**

En esta área se encuentra el departamento de Oficinas "B", se adjunta la configuración de la VPC.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224659.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224650.png" width="300"/></div>

<br>

- **Nivel 2: Oficionas "C"**

En esta área se encuentra el departamento de Oficinas "C", se adjunta la configuración de la VPC.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224641.png" width="600"/></div>

Se adjunta la imagen del equipo.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 224633.png" width="300"/></div>


### **2. Comunicación entre Hosts🖥️**

- **Conexión entre Administración y Oficinas "C"**

```
Computadora "ADMIN" --> Computadora "C1"
Ip de "ADMIN": 192.168.47.11
Ip de "C1": 192.168.47.21
```


En esta conexión se realizó un ping desde la VPC de Administración hacia la VPC de Oficinas "C", dichas VPCs se encuentran en niveles diferentes para ser específicos Administración está en el Nivel 1 y Oficinas "C" en el Nivel 2, se adjunta la imagen de la conexión.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 232411.png" width="600"/></div>


Muestra de ARP de la VPC de Administración, luego de realizar el ping.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 232611.png" width="600"/></div>


<br>

- **Conexión entre Recursos Humanos y Atención al Cliente**

```
Computadora "RRHH1" --> Computadora "ATCLI1"
Ip de "RRHH1": 192.168.47.15
Ip de "ATCLI1": 192.168.47.13
```
En esta conexión se realizó un ping desde la VPC de Recursos Humanos hacia la VPC de Atención al Cliente, dichas VPCs se encuentran en el mismo nivel específicamente en el Nivel 1, se adjunta la imagen de la conexión.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 233323.png" width="600"/></div>

Muestra de ARP de la VPC de Recursos Humanos, luego de realizar el ping.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 233335.png" width="600"/></div>

<br>

- **Conexión entre Oficinas "A" y Oficinas "B"**

```
Computadora "A1" --> Computadora "B1"
Ip de "A1": 192.168.47.210
Ip de "B1": 192.168.47.24
```

En esta conexión se realizó un ping desde la VPC de Oficinas "A" hacia la VPC de Oficinas "B", dichas VPCs se encuentran en el mismo nivel específicamente en el Nivel 2, se adjunta la imagen de la conexión.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 233921.png" width="600"/></div>

Muestra de ARP de la VPC de Oficinas "A", luego de realizar el ping.


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 233929.png" width="600"/></div>


### **3. Captura de Paquetes ARP/ICMP💾**

Para realizar la captura de paquetes se hará conexión entre Atención al cliente que es de Nivel 1 y Oficinas "C" que es de Nivel 2, se adjunta la captura de paquetes.




```
Computadora "ATCLI2" --> Computadora "C2"
Ip de "ATCLI2": 192.168.47.14
Ip de "C2": 192.168.47.22
```

Empezamos con la captura de paquetes en la VPC de Atención al cliente.
<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 234934
.png" width="600"/></div>

<br>

Acá se puede observar el ARP manda los paquetes a todas las VPCs.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 234952.png" width="600"/></div>

<br>


<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 235001.png" width="600"/></div>

<br>

Como se puede ver acá aparece con cheque el paquete las veces que se realizó el ping.

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 235219.png" width="600"/></div>

<br>

<div align="center"><img src="./Images/Captura de pantalla 2024-02-16 235303.png" width="600"/></div>


Y por ultimo un `arp -a` para ver la tabla ARP de la VPC de Atención al cliente.

<br>

<div align="center"><img src="./Images/Captura de pantalla 2024-02-17 000617.png" width="600"/></div>