# MESURES DE PROTECCIO DE LES DADES

## MESURES DE SEGURETAT

### Preventives (Actives)
Permeten anticipar un desastre per actuar abans que es produeixi. Exemple: SMART (Self-Monitoring, Analysis, and Reporting Technology) en discos durs. És una funció que monitora la informació interna de les unitats d'emmagatzematge.

### Correctores o pal·liatives (Passives)
Aquesta mesura busca tornar a l'estat anterior al desastre el més aviat possible. Exemple: Restablir una còpia de seguretat prèviament feta.

## RESPOSTES TÍPIQUES A FALLADES DE MAQUINARI

### SUBSTITUIR
1. Desembalar
2. Instal·lar sistema operatiu
3. Instal·lar controladors
4. Actualitzar sistema operatiu
5. Instal·lar programari i configuració

### DUPLICACIÓ (REDUNDÀNCIA): ALTA DISPONIBILITAT O HA (HIGH AVAILABILITY)
1. Fonts d'alimentació duplicades
2. Controladors de discos duplicats
3. Channel bonding (Duplicar targetes de xarxa)
4. Discos durs duplicats (RAID)
5. Servidors complets duplicats
6. Centre de Processament de Dades (CPD) complet
7. Mirroring de la xarxa (El Port Mirroring és una tècnica que permet duplicar selectivament el tràfic de xarxa d'un port o diversos ports en un switch i enviar-lo a un altre port per a la seva anàlisi. Això facilita la monitorització del tràfic sense afectar el rendiment de la xarxa.)

## RESPOSTES TÍPIQUES A FALLADES DE PROGRAMARI
Solució bàsica: Reinstal·lar. Pot ser una gran pèrdua de temps. Cal solucionar els problemes el més aviat possible. Hi ha organitzacions que no es poden permetre estar molt temps aturades. Restaurar una imatge completa del sistema és una solució preferible per ser molt més ràpida. Després probablement caldrà restaurar dades de programes.

## PLA DE CONTINGÈNCIA
És necessari tenir un pla de contingència, no es poden prendre decisions en el moment del desastre, ja que és una emergència.

Plan de contingència: Document que conté una descripció pas a pas per tornar a la normalitat en cas d'un incident de seguretat.

- Preveu els problemes abans que passin
- Determina quins són els elements crítics i els no crítics
- Determina què fer en cas de fallada
- Determina la política de còpies de seguretat
- Determina les responsabilitats del personal

---

# MITJANS D’EMMAGATZEMAMENT

## CLASSIFICACIÓ DE DISPOSITIUS

### SEGONS EL MODE D’ACCÉS A LES DADES
- **Accés seqüencial**: El capçal de lectura del dispositiu ha de passar per la totalitat de les dades guardades prèviament a les dades a les quals es vol accedir. Exemple: Per arribar a la dada en posició 5, s'ha de passar per 1, 2, 3, 4. Funcionament normal de les unitats de cinta.
- **Accés aleatori**: El capçal de lectura accedeix directament a la ubicació física de la informació que es vol accedir. Es situa el capçal a sobre de la posició de la dada que es vol accedir. És el funcionament normal dels discos i les memòries semiconductores.

### SEGONS L’ACCÉS DES DE LA CPU ALS DISPOSITIUS
- **Dispositius primaris**: RAM, accessible directament des de la CPU. Al apagar es perd la informació.
- **Dispositius secundaris**: Dispositius dins de l'equip però no accessibles directament per la CPU. Al apagar manté la informació. Exemple: Disc dur intern, disc SSD intern.
- **Dispositius terciaris**: Sistemes generalment més lents que els anteriors. Necessiten un suport (CD, DVD, cinta) quan es volen utilitzar.
- **Dispositius off-line**: Dispositius secundaris o terciaris que es desconnecten al finalitzar, connectats a un port de l'equip amb clau USB. Exemple: Pen drive, USB extern.
- **Emplazament remot**: Els dispositius d'emmagatzematge resideixen en equips connectats via xarxa local o xarxa WAN. Exemple: NAS, SAN, Cloud.

### SEGONS EL SUPORT QUE UTILITZEN
- **Memòria RAM**: La més ràpida en lectura/escriptura. Són volàtils, es perd la informació al apagar l'ordinador.
- **Memòria ROM**: Lectura ràpida, però no es pot escriure. No són volàtils.
- **Memòria Flash**: Es pot llegir i escriure i no són volàtils. 
    - Molt alta velocitat en lectura/escriptura, però amb poca capacitat.
    - Normalment, molt més ràpides en lectura que en escriptura.
    - Les memòries flash augmenten de capacitat i baixen de preu cada dia.
    - Actualment existeixen "discos durs" amb memòries flash, els SSD.

- **Suports magnètics**: 
    - Existeix una superfície de plàstic o de metall sobre la qual el capçal de lectura "llegirà" els registres magnètics emmagatzemats en un material magnètic que es interpretaran com 0's i 1's.
    - Aquest material magnètic pot estar repartit sobre una superfície circular (disc) o sobre una cinta que es desplaçarà d'una bobina a una altra.
    - Tenen molta menys velocitat de lectura/escriptura que les memòries de semiconductors.
    - Tenen molta més capacitat de dades que les memòries de semiconductors.
    - Cal tenir cura, es trenca l'imant fàcilment.
    - Exemple: Disquets, discos durs, cintes de backup.

- **Suports òptics**:
    - La capa superior té "forats" que es interpreten com 1's i 0's.
    - La capa inferior fa reflectir el raig làser i calculant la diferència de temps en el reflex, es pot determinar si és un 0 o un 1.
    - La seva capacitat de dades és mitjana: més que les memòries i menys que els suports magnètics.
    - La seva velocitat d'accés també és mitjana. Més lent que els discos durs i més ràpida que les cintes i disquets.

### EMMAGATZEMAMENT REMOT: SAN, NAS, CLOUD

- **SAN (Storage Area Network)**: 
    - Tenim una xarxa utilitzada per connectar servidors, arrays de discos i biblioteques de suport. Basada en tecnologia Fibre Channel i iSCSI.

- **NAS (Network Attached Storage)**:
    - Tecnologia d'emmagatzematge dedicada a compartir la capacitat d'un servidor amb ordinadors personals o servidors clients a través d'una xarxa d'ús general (normalment TCP/IP). Ús de protocols CIFS, SMB, NFS, FTP o TFTP.

- **CLOUD**:
    - Emmagatzematge al núvol també coneguda com a disc dur virtual. És un espai en un servidor que utilitzem per guardar arxius.

---

# ORGANITZACIÓ DE DISCOS

## DISC DURS
- **Plato**: Cada disc del disc
- **Cara**: Ambdues cares del disc
- **Capçalera**: Número de capçaleres.
- **Pista**: Circumferència dins de la cara.
- **Cilindre**: Conjunt de diverses pistes.
- **Sector**: Cada una de les divisions d'una pista.

## PARTICIONS
1. Crear partició
2. Formatjar amb un sistema de fitxers (EXT4, NTFS, etc)

### Models de particionat
- **MBR (Master Boot Record)**: Funcionava amb sistema d'arrencada BIOS
- **GPT (GUID Partition Table)**: Model més nou. Funciona amb sistema d'arrencada UEFI

### Avantatges de fer particions
- Ús de sistemes de fitxers antics
- Guardar una còpia de restauració ràpida en una altra partició
- Dual S.O
- Separar partició d'intercanvi (SWAP) per millor rendiment
- Creació de quotes físiques

### PARTICIONAT MBR

- **BIOS**: Primer programa que s'executa a l'arrencar. Creat per IBM 1983. S'emmagatzema en memòria flash ubicada a la placa base independentment del sistema d'emmagatzematge.
- **MBR**: Registre en sector 0 llegit per BIOS a l'arrencar. Microsoft en 1983. Taula de 4 entrades, 1 per partició. Cada entrada indica inici de partició en disc.

### ESTRUCTURA DE UN DISC AMB MBR
- **TIPUS DE PARTICIONS MBR**
    - Partició Primària: Fins a 4 o fins a 3 i 1 estesa.
    - Partició estesa: Partició que es divideix en particions lògiques.
    - Partició lògica: Subdivisió de la partició estesa. Es poden crear les que es vulguin dins.
    - Partició Activa: Estat de partició primària.

### PARTICIONAT GPT

- **GPT**: Nou estàndard substitueix MBR i està associat a UEFI. A cada partició se li associa un identificador únic GUID o UUID en Linux.

### Avantatges de GPT
- Identificador GUID (id disc) i identificador de partició únic (PARTUUID).
- Etiqueta per partició individual.
- GPT no té límit de particions. 128 particions en Windows.
- No es necessiten particions esteses ni lògiques.
- Usa LBA amb mida màxima de disc de 2 ZiB (2^30 GiB).
- GPT crea capçalera i taula de particions de backup.
- Utilitza CRC32 per detectar errors i corrupció.

---

# SISTEMES DE FITXERS

Controla com es guarden o recuperen les dades.

### Funcions
- Gestió de l'espai de noms de fitxers
- Gestió d'espai d'emmagatzematge
- Assignar espai a arxius
- Alliberar espai d'arxius esborrats
- Administració d'espai lliure/ocupat
- Accés a les dades guardades
- Organitzar fitxers del sistema
- Assegurar protecció de fitxers (ACL's)

### TIPUS DE SISTEMES DE FITXERS

- **FAT (16, 32)**: File Allocation Table (MSDOS, Windows 95, 98)
- **NTFS**: New Technology File System (Windows NT en endavant)
- **Ext2, 3, 4**: Extended File System (Versió 2, 3, 4, Linux)
- **HFS**: Hierarchical File System (Mac OS)
- **HFS+**: Extended Hierarchical File System (Mac OS)

---

# EMMAGATZEMAMENT REDUNDANT: RAID

### CONCEPTE RAID
Sistema de replicar la informació en diferents discos estàndard, de manera que el sistema els veu com un sol disc nomenat VOLUM.

### Ús
- Tolerància a fallades
- Augment de rendiment
- Capacitat d'afegir discos i afegir discos en calent
- Alta disponibilitat, si un disc falla tenim els altres

### TIPUS DE RAID SEGONS CONSTRUCCIÓ

- **Software**
    - Funciona instal·lant controladors de disc estàndard i programari executant-se en l'equip.
    - **Avantatges**: Mètode universal, poden transportar discos i recuperar sense maquinària específica.
    - **Desavantatges**: El sistema operatiu fa els càlculs necessaris i l'accés als discos en controladors de discos diferents, cosa que carrega la CPU.

- **Hardware**
    - Necessitat d'un controlador de discos especial amb múltiples ports (placa base o PCIe).
    - **Avantatges**: No carrega el sistema operatiu.
    - **Desavantatges**: Propietari, en cas de fallada del controlador, els discos no es poden llegir amb una altra marca. Necessitat de tenir el recanvi disponible.

### TIPUS DE RAID

- **Raid 0**: Sense tolerància a fallades
- **Raid 1**: Tolerància a fallades, 2 discos mínim
- **Raid 5**: Tolerància a fallades mínim 3 discos

### RAID 0
- Dades es distribueixen en diferents discos com si fossin un sol disc.
- Alt rendiment.
- Si falla un disc, es perden les dades.

### RAID 1
- Dades es copien en 2 discos.
- Tolerància a fallades.
- Si un disc falla, es pot seguir treballant fins que es canviï.
- 50% d'espai aprofitable.

### RAID 5
- Tolerància a fallades.
- Mínim 3 discos.
- Dades es copien consecutivament i alternativament en els discos.
- Si un disc falla, es pot continuar treballant.

---

# COPIA DE SEGURETAT

Mesura de seguretat lògica i passiva que consisteix en crear duplicats de dades. Assegurem integritat i disponibilitat.

### Polítiques de còpies de seguretat
- Identificar quines dades cal preservar
- Establir la freqüència dels processos de còpies i planificar la còpia
- Calcular el volum de dades
- Dispositius i suports d'emmagatzematge
- Emmagatzematge físic ignífug
- Planificar la restauració de dades
- Xifrat i compressió

### Estratègia de còpies de seguretat 3-2-1
- 3: Tindrem 3 còpies de seguretat
- 2: Guardar còpies en 2 formats diferents, USB i NAS
- 1: Guardar una còpia en 1 ubicació remota

### TIPUS DE COPIES
- **Completa**: Inclou tota la informació.
- **Diferencial**: Còpia parcial, només copia les dades modificades des de l'última còpia completa.
- **Incremental**: Còpia parcial, només copia les dades modificades des de l'última còpia completa o incremental.
