1. MESURES DE PROTECCIO DE LES DADES||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||


MESURES DE SEGURETAT

1. Preventives (Actives)

Permiten anticipar un desastre para actuar antes que de produja.
Ej.:SMART (Self-Monitoring, Analysis, and Reporting Technology) en discos duros.

Es una funcion que monitorea la info interna de las unidades de almacenamiento.

2. Correctores o pal·liatives (Passives)

Estas medida buscar devolver al estado anterior al desastre lo antes possible. Pj.: Restablecer backup previamente hecho.


RESPOSTES TIPIQUES A FALLADES DE MAQUINARI

1. SUBSTITUIR

1.1 Desembalar
1.2 Instalar S.O
1.3 Instalar drivers
1.4 Actualizar S.O
1.5 Instalar doftware y conf

2. DUPLICACIO (REDUNDANCIA): ALTA DISPONIBILITAT O HA (HIGH AVAILABILITY)

2.1 Fuentes de alimentación duplicadas
2.2 Controladores de discos duplicados.
2.3 Channel bonding (Duplicar tajetas de red)
2.4 Discos duros duplicados (RAID)
2.5 Servidores completos duplicados 
2.6 CPD Completo 
2.7 Mirroring de la red (El Port Mirroring es una técnica que permite duplicar selectivamente el tráfico de red de un puerto o varios puertos en un switch y enviarlo a otro puerto para su análisis. Esto facilita la monitorización del tráfico sin afectar el rendimiento de la red.)


RESPOSTES TIPIQUES A FALLADES DE PROGRAMARI

Solución básica: Reinstalar. Puede ser mucha perdida de tiempo.
	Necesitas solucionar los problemas lo antes posible.
	Hay organizaciones que no se pueden permitir estar mucho tiempo paradas.
Restaurar una imagen completa del sistema.
	És una solución preferible, por ser mucho mas rapida.
	Despues seguramente hara falta restaurar datos de programas.

PLA DE CONTINGENCIAEs necesario tener un plan de contingencia, no se pueden tomar decisiones en el mmomento del desastre, ya que es un aemergencia.

Plan de contingnecia: Documento que contiene en el la descripcion paso a paso para volver a la normalidad en caso de un incidente de seguridad.

	Previene los problemas antes de que pasen
	Determina cuales son los elementos criticos y los no criticos.
	Determina que hacer en caso de fallada
	Determia la politica de copias de seguridad
	Determina las responsabilidad del personal



2.MITJANS D’EMMAGATZEMAMENT||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||

CLASSIFICACIO DE DISPOSITIUS

1. SEGONS EL MODE D’ACCÉS A LES DADES

Acceso secuencial: El cabezal de lectura del dispositivo debe pasar por la totalidad de los datos guardados previamente a los datos que se quiere acceder.
	Ej.: Para llegar al datoe n posicion 5, has de pasar por 1,2,3,4
	Funcion normal de las unidades de cinta.

Acceso aleatorio: El cabezal de lectura accede directamente donde se encuentra fisicamente la informacion que se quiere acceder.
	Se situa el cabezal encima de la posicion del dato que se quiere acceder.
	Es el funcionamiento normal de los discos y las memorias semiconductoras.

2. SEGONS L’ACCÉS DES DE LA CPU ALS DISPOSITIUS

Dispositivos primarios: RAM, accesible directamente des de la CPU. Al apagar se peirde la info

Dispositivos secundarios: Dispositivos que se encuentran desnto del equipo pero no accesible directamente por la CPU.
	Apaagr mantiene la info.
	Ej.: Discdo duro interno, disco ssd interno

Dispositivo terciarios: Sistemas generalmente mas lentos que los anteriores.
	Necesidad de un soporta (cd, dvd, cinta) cuando queires utilizarlos.

Dispositivo off-line: Dispositivos secundarios o terciarios que se desconectan al terminar, conectados a un puerto del equipo con llave USB.
	Pen drive, USB externo

Emplazamiento remoto: Los dispositivos de almacenamiento residen en equipos conectados vía red local o red WAN.
	Ej.: NAS, SAN, Cloud


3. SEGONS EL SUPORT QUE FAN SERVIR:

Memoria RAM: La más rápida en R/W. Son volátiles, o bien, si se apaga el ordinador se pierde su información.

Memoria ROM: Lectura rápida, pero no se puede escribir. No son volátiles.

Memoria Flash: Se puede llegar y escribir y no son volátiles.

	De muy alta velocidad en R/W, pero con poca capacidad.
	Normalmente, mucho más rápido en lectura que en escritura.
	Las memorias flash cada día aumentan de capacidad y bajan de precio.
	Actualmente existen «discos duros» con memorias flash, los SSD.

Suport magnètics

Existe una superficie de plástico o de metal sobre la que el cabezal de lectura «llegará» con registros magnéticos enmagtzemades en un material magnético que se interpretarán como 0's i 1's.

Este material magnético puede estar repartido sobre una superficie circular (disco) o sobre una cinta que se desplazará de una bobina a otra.

Tienen mucha menos velocidad de R/W que las memorias de semiconductores.

Tienen mucha más capacidad de datos que las memorias de semiconductores.

Cuidado se rompe el iman facil.

Ej.: Disquetes, discos duros, cintas de backup.

Suports òptics

La capa superior tiene "agujeros" que se interpretan como 1's y 0's.

La capa inferior hace reflejar el rayo láser y calculando la diferencia de tiempo en el reflejo, puede determinarse si es un 0 o un 1.

Su capacidad de datos es media: más que las memorias y menos que los soportes magnéticos.

Su velocidad de acceso también es media. Más lento que los discos duros y más rápida que las cintas y disquetes.

EMMAGATZEMAMENT REMOT: SAN, NAS, CLOUD

1. SAN Storage Area Network

Tenemos una red utilizada para conectar servidores, *arrays de discos y librerías de apoyo. Basada en tecnología *fibre *channel y *iSCSI.

2. NAS Network Attached Storage

Tecnología de almacenamiento dedicada a compartir la capacidad de un Servidor con ordenadores personales o servidores clientes a través de una red de uso general (normalmente *TCP/IP). Uso de protoclos CIFS, SMB, NFS, FTP o TFTP.

3. CLOUD

Almacenamiento a la nube también conocida como disco duro virtual. Es un espacio en un servidor que utilizamos para guardar archivos.


3. ORGANITZACIO DE DISCOS|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||

DISC DURS
	Plato: Cada disco del disco
	Cara: Amabs caras del disco
	Cabezera: Numero de cabezeras.
	Pista: Circumferencia dentro de cara.
	Cilindro: Conjunto de varias pistas.
	Sector: Cada una de las divisiones de una pista.

PARTICIONS

Crear Particion
Formatear con un sistema de archivos (EXT4, NTFS,etc)

Models de particionat

MBR (Master Boot Record) Funcionaba con sistema de arranque BIOS
GPT (GUID Partition Table) Modelo modelo Fujnciona con ssitema de arranque UEFI

VENTAJAS DE HACER PARTICIONES

Uso de sistemas de archivos antiguos
Guardar un acopia de restauracion rapida en otra particion
Dual S.O
Separar particion de intercambio (SWAP) para mejor rendimiento
Creacion de cuotas fisicas

PARTICIONADO MBR

BIOS: Primer prgorama que se ejecuta al arrancar
	Creado por IBM 1983
	Se almacena en memoria flash ubicada placa base
	independiente al sistema de almacenamiento

MBR: Registro en sector 0 leidop por BIOS en arrancar
	Microsoft en 1983
	Tabla de 4 entradas, 1 por particion
	Cada entrada indica inicio de particion en disco

ESTRUCTURA DE UN DISCO CON MBR

	TIPOS DE PARTICIONES MBR
		Particion Primaria: Hasta 4 o hasta 3 y 1 extendida.
		Particion extensa: Particion que se divide en particiones lógicas.
		Particion logica: Subdivision de la particion extensa. Se pueden crear las que quieras dentro.
		Particion Activa: Estado de particion primaria.

PARTICIONADO GPT

GPT: nuevo estandar sustituye MBR y esta asociado a UEFI.
A cada particion se le asocia un unido identificador GUID o UUID en Linux.

VENTAJAS DE GPT

Identificador GUID (id disco) y identificador de particion unico (PARTUUID).
Etiqueta por particion individual
GPT no tiene limite de particiones. 128 particiones en windows.
No se necesitas particiones extensas niu logicas
USA LBA tamaño maximo de disco de 2 ZiB (2^30 GiB)
GPT crea cabecera y tabla de particiones de backup
Utiliza CRC32 para detectar error y corrupcion.

SISTEMAS DE ARCHIVOS

Controla como se guardan o recuperan los datos.

Funciones
	Gestion del espacio de nmombres de ficheros
	Gestion de espacio de almacenamiento
		Assignar espacio a archivos
		Liberar espacio de archivos borrados
	Administracion de espacio libre/ocupado
	Acceso a los datos guardados
	Organizar ficheros del sistema
	Asegurar proteccion de ficheros ACL's

TIPOS DE SISTEMAS DE ARCHIVOS

FAT (16,32) Fille Allocation Table MSDOS, Windows 95,98
NTFS New Thechnology File System Windows NT a delante
Ext2, 3, 4 Extended File System Version2, 3, 4, Linux
HFS Hierarchical File System, Mac OS
HFS+ Extended Hierarchival File System Mac OS


EMMAGATZEMAMENT REDUNDANT: RAID|||||||||||||||||||||||||||||||||||||||||||||||||

CONCEPTO RAID
	Sistema de replicar la informacion en diferentes discos estandard, de manera que el sistema los ve como un sol odisco nombrado VOLUMEN.
Uso
	Tolerancia a falos
	Augemnto de rendimiento
	Capacidad de añadir descos y añadir discos en caliente
	Alta disponibilidad, si un disco muere tenemos los otros

TIPOS DE RAID SEGUN CONSTRUCCION

Software
Funciona instalando controladores de disco estandar y software ejecutandose en el equipo
	Ventajas: Metodo universal, Pueden transportar discos y recueprar sin maquinarioa especifica
	Desventajas: S.O hace calculos necesarios y el acceso a los discos en controladores de discos diferentes, cosa que carga la CPU

Hardware
Necesidad de un conttrolador de discod especial con multiples puertos ( placa base o PCIe)
	Ventajas: No carga el S.O
	Desventajas: Propietario, en caso de fallada de la controladora, los discos no se pueden leer con otra marca. Necesidad de tener el recambio disponible.

TIPOS DE RAID

Raid 0: Sin tolerancia a fallas
Raid 1: Tolerancia a fallas, 2 discos min
Raid 5: Tolerancai a fllas min 3 discos

RAID 0
Datos se distribuyen en diferentes discos como si fuesen un solo disco
Alto rendimiento
Si falla un disco pierdes datos

RAID 1
Datos de escriben en 2 discos
Teolerancia a fallas
Si un disco falla dse puede seguir trabajando ahsta qeu se cambie
50% de espacio aprovechable

RADI 5
Tolernacia a fallas
Minimo 3 discos
Datos se escriben consecutivamente i alternativamente en los discos
Si un disco falla, se puede continuar trabajando.



COPIA DE SEGURETAT||||||||||||||||||||||||||||||||||||

Medida de seguridad logica y passiva que conssite en crear duplicados de datos.

Aseguramos integridad y disponiblidad


Polítiques de còpies de seguretat

	Identificar que datos necesitas preservar
	Establecer la frecuencia de los procesos de copias y planificar la copia
	Calcular volumen de datos
	Dispositivos y soporte de almacenamiento
	Almacenamiento fisico ignifugo
	Planificar la restauracion de datos
	Cifrado y compression
	

Estrategia de copias de seguridad 3-2-1

3: Tendremos 3 copias de seguridad 
2: guardar en copias en 2 formatos distintos, USB y NAS
1: Guardar una copia en 1 ubicacion remota


TIPOS DE COPIAS

Completa: Incluye toda la informacion
Diferencial: Copia parcial, Soloc copia los datos modificados des de la ultima copia completa
Incremental: Copia parcial, Solo copia los datos modificados des de la ultima copia completa o incremental
