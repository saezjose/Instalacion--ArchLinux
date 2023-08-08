# Instalacion--ArchLinux desde una Maquina Virtual
Esta guía te proporcionará instrucciones paso a paso para instalar ArchLinux, una distribución Linux ligera y altamente personalizable. Si eres nuevo en el mundo de ArchLinux, no te preocupes, esta guía está diseñada para ser lo más entendible y amigable posible.

# Requisitos Previos

- Tener instalado el programa de VirtualBox para poder inciar ArchLinux desde una Maquina Virtual.

- Descargar la ISO de ArchLinux desde la siguiente pagina [Sitio oficial de ArchLinux](https://archlinux.org)

- Equipo compatilbe con la arquitectura de 64 Bits

- Conexion a internet

# Configuracion de virtual Box 

Para montar la ISO de ArchLinux a La maquina virtual VirtualBox haz los siguientes pasos.

- Asignale un nombre a tu Maquina Virtual.

[![v1.png](https://i.postimg.cc/ZnF5yp3p/v1.png)](https://postimg.cc/8fcS2FZz)

- Monta la ISO de ArchLinux a tu maquina virtual.
  
- Asignale cuanto Procesador y Memoria Base va a tener tu Maquina Virtual.

[![v3.png](https://i.postimg.cc/SscMDXCN/v3.png)](https://postimg.cc/mz2krgm0)

- Asignale Espacio a tu Maquina Virtual (Recomendable 20gb)

[![v4.png](https://i.postimg.cc/Wz3stCNL/v4.png)](https://postimg.cc/7GpFWBJm)

- Y finalemente presiona Terminar.

##  Configura La conexion de internet a tu maquina virtual

Ahora configuraremos la conexion de internet a tu maquina virtual llendo a la configuracion de tu Maquina Virtual buscas la opcion de red, de forma predeterminada estara en el adapator 1, Haz click en (Hablitar Adaptador de Red) y cambias la opcion de NAT a Adaptador de Fuente. Lo que sucede al cambiar esta configuracion  es que va a utilizar la conexion de internet de tu sistema operativo para poder utilizarla en tu maquina virtual.

[![v5.png](https://i.postimg.cc/prTnxs3y/v5.png)](https://postimg.cc/8J2CmmpV)



# Instalacion de Archlinux 

Una vez todo ya una vez configurado inicia tu Maquina virtual y te iniciara la Iso de Archlinux te saldra la siguiente imagen

[![v6.png](https://i.postimg.cc/C16QsxT1/v6.png)](https://postimg.cc/47VPJZ3k)


ahora seleccionas: ArchLinux install medium (x86_64 BIOS) y te mandara a la terminal de ArchLinux.

una vez que haya cargado toda la terminal de ArchLinux te saldra en pantalla **root@archiso ~ #** lo que significa que estamos en la terminal de instalacion de ArchLinux.

- Lo primero que haremos es configurar la distribucion del teclado, comunmente este estara en la distribucion del teclado en ingles si queremos colocarlo en nuestra distribucion de teclado en español latino colocamos la siguiente linea de comando:

- `loadkeys la-latin1`

- Ahora Verificamos si tenemos internet coloca la siguiente linea de comando:

- `ping -c 4 google.com `

- esto lo que hara es establecer una conexion con google para enviar paquetes de datos a la direccion de google.com con tal de verificar la conectividad con el servidor de google

## Particion de discos.


