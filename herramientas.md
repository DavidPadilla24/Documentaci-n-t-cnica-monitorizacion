Los sistemas operativos modernos incluyen herramientas integradas para la monitorización de recursos. Estas permiten obtener información detallada sobre el rendimiento y el estado del sistema.


# **Monitorizacion de Procesos**

## **ps**


----

- El comando ``ps`` muestra información sobre los procesos en ejecución.

Con ``ps aux`` se muestra información sobre todos los procesos de todos los usuarios en formato largo y con información adicional.

![psaux](/img/psaux.png)


Si quieres info sobre un proceso en concreto, puedes usar `` ps -C <nombre> ``


![psnano](/img/psnano.png)


Si quieres ver los procesos que mas ocupen, por ejemplo, los 5 que mas ocupan memoria, puedes usar ``ps -eo user,pid,%cpu,%mem,time --sort=-%cpu``

![pseo](/img/5procesosquemasconsumen.png)

---

## **top**

- El comando top permite monitorear en tiempo real el uso de recursos del sistema, como CPU, memoria y procesos en ejecución.

![top](/img/top.png)


---

``top -b -n 1 > top.txt``   Genera una captura de top y guardar la informacion en un archivo

![topb](/img/topb.png)

---


## **atop**

``atop`` es una herramienta de monitorización avanzada para sistemas Linux, que proporciona información detallada sobre el uso de recursos y procesos.

![atop](/img/atop.png)




# **Monitorizacion de Red**

## TCPDUMP


El comando ``tcpdump``es una herramienta de línea de comandos que permite capturar y analizar paquetes de red en un sistema. Es muy útil para depurar problemas de red, analizar tráfico y realizar tareas de seguridad.


![tcpdump](/img/tcpdump.png)



## TCPDUMP con tu tarjeta de red

Para capturar paquetes de red con tcpdump, necesitas especificar la interfaz de red que deseas monitorear. Puedes ver las interfaces de red disponibles en tu sistema con el comando ifconfig o ip a.


``sudo tcpdump -i eth0``

![tcpdump-i](/img/tcmpdumpi.png)


## TCPDUMP redirección a un archivo

Para guardar la salida de tcpdump en un archivo, puedes redirigir la salida a un archivo de texto.


``sudo tcpdump -i eth0 -w capturas``

![tcpdump-ieno](/img/capturapaquetesopenweb.png)

![tcpdump-ieno](/img/paquetesopenwebinar.png)

---

``tcpdump -r capturas ``

El comando tcpdump -r se utiliza para leer archivos de captura de paquetes de red previamente guardados


![tcpdump-r](/img/tcpcapturas.png)




## TCPTRACK


``tcptrack`` es una herramienta de línea de comandos que muestra el tráfico de red en tiempo real. Muestra información sobre conexiones TCP activas en un sistema, incluidas las direcciones IP, los puertos y el estado de la conexión.

![tcptrack](img/tcptracken1.png)

---

## IPTRAF

``iptraf`` es una herramienta de monitorización de red en tiempo real para sistemas Linux, diseñada para proporcionar estadísticas detalladas sobre el tráfico de red.

![iptraf](/img/iptraf.png)


![iptraf](/img/iptrafresultado.png)

---

## BMON

``bmon (Bandwidth Monitor) `` es una herramienta de monitorización en Linux utilizada para supervisar el ancho de banda y el tráfico de red en tiempo real. 


![BMON](/img/bmon.png)



# **Monitorizacion de Almacenamiento**

## free

El comando ``free`` muestra la cantidad de memoria libre y utilizada en el sistema. Usando ``free -h``, la salida se muestra en un formato más legible para el usuario.

Para verlo en intervalos de 3s por ejemplo, se puede usar ``free -s 3``.


![free](/img/freememoriaRAM.png)

 ## ESPACIO

Con el comando ``df``, se puede ver el espacio en disco disponible y utilizado en el sistema.

Usando ``df -hT``, se muestra el espacio en disco en un formato más legible para el usuario.

Si quiero ver algun espacio en concreto, por ejemplo el de /, se puede usar ``df -hT`` /.


![df](/img/df-htamañodiscos.png)


Si quiero calcular el espacio, por ejemplo, de un directorio en concreto, se puede usar ``du -sh`` /directorio.


![du](/img/du-hs.png)

--- 

## iostat

El comando ``iostat`` muestra estadísticas de uso de CPU y dispositivos de E/S.

![iostat](/img/iostatnombredisco.png)



Con la opción ``-x``, se muestra información extendida sobre las estadísticas de dispositivos de E/S.

Si quiero verlo en intervalos de 5s por ejemplo, se puede usar iostat ``-x nvme0n1 -s 5``.

![iostat](/img/iostat-x.png)





