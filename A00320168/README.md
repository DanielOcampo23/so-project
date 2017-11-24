## Miniproyecto Sistemas Operativos

**Universidad ICESI**  

**Nombres:**
  * Esteban Camacho B. - A00320168  
  * Oscar Daniel Molano. - A00267576 
  
**Github URL:** https://github.com/LookIron/so-project

**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:**  Servicios web  
**Correo:** daniel.barragan at correo.icesi.edu.co

## Objetivos
* Desplegar una aplicación en un servidor que ejecuta el sistema operativo Linux
* Realizar los ajustes y depuración necesarios para desplegar una
aplicación en Linux
* Realizar aplicaciones para obtener información del sistema operativo

## Descripción
Para el despliegue de una aplicación en un servidor se requiere conocer los procedimientos necesarios relacionados con la configuracion de las interfaces de red, ajustes de seguridad, instalación de dependencias, usuarios y herramientas de depuracíon del sistema operativo.

El siguiente proyecto consiste en el despliegue de una aplicación web para obtener información del sistema operativo (La aplicación debe permitir consulta uso de CPU, memoria y espacio en disco). Para este propósito se debe emplear el sistema operativo Ubuntu Server 16.04, el microframework flask y ambientes virtuales.

<p align="center">
  <img src="images/vista-despliegue.png" alt="webservice architecture"/>
</p>

## Actividades
* Nombre y código de todos los integrantes del grupo (máximo 3) (5%)
* Ortografía y redacción (5%)
* Descripción breve de los pasos para cumplir con lo solicitado
  * Sistema operativo Ubuntu Server 16.04 (10%)
  * Configuración de interfaces de red (10%)
  * Configuración de puertos (10%)
  * Instalación de dependencias (10%)
  * Creación de ambientes virtuales (10%)
  * Aplicación en Python (10%)
  * Validación de la ejecución del servicio (netstat) (10%)
* Pruebas de la solución a través de capturas de pantalla. Puede emplear si lo desea una herramienta de captura de pantalla a formato .gif (10%)
* El informe debe ser entregado en formato pdf a través del moodle y el informe en formato README.md debe ser subido a un repositorio de github. El repositorio de github debe ser un fork de https://github.com/ICESI-Training/so-project y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (10%).

-------------

## Solución

Para la realización del proyecto seguimos los siguientes pasos:

1. ######_Intalación de Ubuntu 16.04:_ Se descargó la ISO de `Ubuntu Server` y se realizó la instalacción utilizandop VirtualBox como se muestra a continuación:

  * Configuración de la maquina virtual
  
     <p align="center">
     <img src="images/ubuntu1.png" alt="webservice architecture"/>
     </p>
     
  * Instalacción de `Ubuntu Server 16.04`
  
     <p align="center">
     <img src="images/ubuntu2.png" alt="webservice architecture"/>
     </p>
    
  * Posterior a esto se creó un usuario proyecto para la realización de los demás pasos.
  
     ```vim
     # adduser proyecto
     # pwdpass ********
     
     ```
  * 
  

2. ######_Configuración de la interfaces de red:_ Ésta se realizó a través de la interfaz de VirtualBox en modo `Adaptador puente (Bridge)` el cual nos permite conectar dos segmentos de red iguales o distintos para que así a traves de otro nodo se pueda acceder al servicio de wed del nodo en el que se pondra el servicio web a través de flask. A continuación mostramos como se realizó dicho proceso.

  * Configuración de la red
  
     <p align="center">
     <img src="images/.png" alt="webservice architecture"/>
     </p>
    
  * Verificación del archivo interfaces: Debido a que nuestra red cuenta con `dhcp` la ip se genera dinamicamente por la tanto no es necesario que nuestra interfaces sea estatica y no se estipule en el archivo de configuración.
  
     <p align="center">
     <img src="images/.png" alt="webservice architecture"/>
     </p>
      

3. ######_Configuración de puertos:_ Una vez configurada la interfaces de red, proseguimos a congigurar los puertos, para esto se realizaron los siguientes pasos:

  * Se habilito el firewall a través de la herramienta `ufw` con el siguiente comando
  
     ```vim
     # ufw enable

     ```
     
  * Se habilito el puerto 8080 para los servicios que se van a prestar, con el siguiente comando
  
     ```vim
     # ufw allow 8080

     ```
  
  * Por último verificamos que efectivamente estan habilitado, con el siguiente comando.
  
     ```vim
     # ufw status verbose

     ```
  * Prueba de funcionamiento
  
     <p align="center">
     <img src="images/confPuerto.png" alt="webservice architecture"/>
     </p>
  

4. ######_Instalación de las dependencias:_ Para esto realizamos los siguientes pasos

  *

5.

  * Configuración de la red
  
  *
  
  *
  
  






 
## Referencias
* https://www.ubuntu.com/download/server

