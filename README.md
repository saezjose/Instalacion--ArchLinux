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

## Configuracion de distribucion de teclado

- Lo primero que haremos es configurar la distribucion del teclado, comunmente este estara en la distribucion del teclado en ingles si queremos colocarlo en nuestra distribucion de teclado en español latino colocamos la siguiente linea de comando:

- `loadkeys la-latin1`

## conexion a internet 

- Ahora Verificamos si tenemos internet coloca la siguiente linea de comando:

- `ping -c 4 google.com `

- esto lo que hara es establecer una conexion con google para enviar paquetes de datos a la direccion de google.com con tal de verificar la conectividad con el servidor de google

## Particion de discos.

ahora veremos los discos disponibles desde la maquina virtual usando el siguiente comando:

 - `fdisk -l `

 importante! el Disco que vamos a utilizar comunmente se conoce como "/dev/sda"

 Ahora particionaremos el disco en este caso haremos 3 particiones en el disco haremos la primerta particion root que es para el sistema la segunda particion para los datos personnales que esta montada en Home y la tercera para el espacio de intercambio

ahora para hacer la particion se introduce este comando:

-  `fdisk  /dev/sda`

-  presiona la letra "p" para mostrar las particiones del disco

-  ahora crearemos una tabla de particiones presionando la letra "o"

-  ahora para crear una particion presiona la letra n

-  nos preguntara si la particion sera primaria o extendida, para la particion del sistema tiene que ser primaria para que pueda bootear

-  para este caso se presiona la letra "p"

nos preguntaran el numero de particion del disco en este caso ahora mismo no hay ninguna particion del disco creada entonces simplemente colocamos "1" 

- ahora nos preguntan donde empieza la particion del disco en este paso simplemente presionamos "Enter"  siempre que nos pregunten el primer sector se deja en blanco.

- el ultimo sector va ser el tamaño que va tener la primera particion en este caso le estableceremos 10gb entonces colocas en la terminal:

-  ` +10G`

-  listo la primera particion creada

-  Ahora haremos particion 2 y 3 en esta particiones debemos crearla en una particion extendida

-  a
