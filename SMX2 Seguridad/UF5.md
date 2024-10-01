# FIREWALLS I SEGURETAT PERIMETRAL

## Conceptes previs:
### IP, màscara, gateway, DNS:
- **IP**: Adreça que identifica un dispositiu en una xarxa.
- **Màscara de subxarxa**: Determina quina part de l'IP correspon a la xarxa i quina als hosts.
- **Gateway**: Dispositiu que connecta una xarxa local amb una altra xarxa.
- **DNS**: Servei que tradueix noms de domini a adreces IP.

### Mapes de xarxa lògic:
- Representació visual d'una xarxa, mostrant dispositius i connexions.
- Eines per dibuixar: Microsoft Visio, Lucidchart, etc.

### Taula de rutes:
- Informació que permet als routers determinar la millor ruta per enviar dades.

### Segmentació de xarxa:
- Dividir una xarxa gran en subxarxes més petites per millorar la gestió i la seguretat.

### Protocols de xarxa i model OSI:
- **Model OSI**: Estructura en capes que descriu les funcions d'una xarxa.
- **Exemple de burocràcia**: Cada capa del model OSI realitza una funció específica, similar a un departament en una empresa.

## Firewalls i seguretat perimetral
### Mesures de seguretat perimetral:
- **Firewall**: Dispositiu que bloqueja el tràfic no autoritzat i permet l'autoritzat.
- **DMZ (Zona Desmilitaritzada)**: Segment de xarxa on es ubiquen servidors públics.
- **IDS (Sistema de Detecció d'Intrusos)** i **IPS (Sistema de Prevenció d'Intrusos)**: Dispositius que monitoregen la xarxa per detectar i/o bloquejar activitats malicioses.
- **Passarel·les antivirus i antispam**: Filtren tràfic maliciós.
- **Honeypots**: Sistemes dissenyats per atraure i analitzar atacs.

### Tipus de firewall:
- **Implementació**:
    - **Hardware**: Més cars i eficients, dedicats exclusivament a funcions de firewall.
    - **Software**: Més econòmics, es poden instal·lar en hardware general.
- **Ubicació**:
    - **Corporatius o de xarxa**: Entre xarxes LAN i WAN.
    - **Basats en host (personals)**: Protegeixen un sol dispositiu.
- **Comportament i nivell del model OSI**:
    - **Firewalls de paquets (Packet filter)**: Treballen en les capes 3 (Xarxa) i 4 (Transport).
    - **Firewalls amb control d'estat (Stateful)**: Mantenen informació sobre connexions actives.
    - **Firewalls de nivell d'aplicació (Application Layer)**: Analitzen el tràfic en la capa 7 (Aplicació).

### Limitacions dels firewalls:
- No poden protegir contra atacs interns, negligència d'usuaris, enginyeria social, ni malware en arxius interns.

### Configuració de firewalls:
- **Política permissiva**: Permetre tot el tràfic excepte el explícitament bloquejat.
- **Política restrictiva**: Bloquejar tot el tràfic excepte el explícitament permès.

### Arquitectures de seguretat amb firewalls:
- **Arquitectura d'1 router**:
    - Usat en xarxes petites/domèstiques.
    - Permet tot el tràfic de sortida i bloqueja el d'entrada no autoritzat.
- **DMZ de host (Bastió)**:
    - El tràfic extern es dirigeix a un únic host (bastió).
    - Menys segur que una DMZ física.
- **Dual Homed Host (o Gateway)**:
    - Un host bastió intercepta tot el tràfic entre la xarxa interna i externa.
    - No hi ha reenviament de tràfic directe entre xarxes LAN i WAN.
- **DMZ amb un sol firewall (3-legged model)**:
    - Firewall amb tres interfícies de xarxa: externa, DMZ i interna.
    - Tot el tràfic ha de passar pel firewall.
- **DMZ amb dos firewalls**:
    - Dos firewalls separen les xarxes externa, DMZ i interna.
    - Major seguretat, especialment si els firewalls són de diferents fabricants.

### IDS i IPS:
- **IDS (Sistema de Detecció d'Intrusos)**:
    - Monitoritza el tràfic de la xarxa i genera alertes davant possibles atacs.
    - Tipus: Network IDS (NIDS) i Host IDS (HIDS).
- **IPS (Sistema de Prevenció d'Intrusos)**:
    - Similar al IDS, però també pot bloquejar el tràfic maliciós.
    - Més avançat i reactiu comparat amb els IDS.

### Ubicació dels IDS:
- **Darrere/davant del firewall**: Només detecta atacs externs.
- **En un port d'inspecció del switch (mirror port)**: Pot monitoritzar tot el tràfic, però pot generar molt tràfic en el IDS.
- **Usant un TAP (Test Access Point)**: Replica la comunicació per anàlisi sense afectar la xarxa original.

## Inventari i Monitorització del Tràfic de Xarxes
### Inventari d'Actius
Un administrador de xarxa ha de conèixer el sistema, documentant la xarxa per a la gestió i la seguretat. És essencial saber:
- On actualitzar el software.
- Detectar baixades de rendiment.
- Controlar l'activitat de la xarxa.

### Documentació de la Xarxa:
- **Disseny físic de la xarxa**: Ubicació de dispositius i cablejat en el plànol de l'edifici.
- **Disseny lògic de la xarxa**: Connexions entre dispositius, incloent configuració de xarxa (IP, nom d'host, serveis).
- **Esquema de direccionament IP**: Taula amb noms, adreces IP, màscara de xarxa, Gateway, DNS i MAC.
- **Còpies de seguretat de configuracions de dispositius**: Guardar configuració de routers, firewalls, switches.
- **Seguiment bàsic de la xarxa**: Documentar el funcionament actual per comparar en cas de problemes.

### Seguiment d'Actualitzacions:
- Actualitzar hardware, contractar personal, instal·lar software, etc., detectant anomalies i degradació del sistema.

### Inventari de la Xarxa
L'inventari permet:
- Saber què fan els usuaris.
- Conèixer programes instal·lats i actualitzacions.
- Avaluar característiques del hardware.
- Determinar si es necessita nou hardware.

### Programes d'Inventari:
- **Inventari d'actius**: Ordinadors, monitors, impressores.
- **Vista detallada d'actius, mapa lògic**.
- **Historial de modificacions**.
- **Administració de sistemes operatius i software**.
- **Gestió de components interns i connexions de xarxa**.

### Funcionament:
- Mode client/servidor amb un programa de gestió centralitzat i un agent informador en cada equip, o usant administració remota (SSH, SNMP).

### Exemples:
- **OCS Inventory**: Programa de codi obert per escanejar i inventariar dispositius.
- **GLPI**: Programa de gestió d'inventari de codi obert.

## Sniffers (Analitzadors de Protocols)
Els sniffers inspeccionen el contingut de trames en la xarxa, en mode interactiu (temps real) o no interactiu (anàlisi forense). Les targetes de xarxa en mode promiscu accepten totes les trames, no només les destinades a elles.

### Funcions:
- Visualització i filtratge de trames en temps real.
- Guardar i recuperar captures (pcap).
- Reconstrucció de sessions TCP.

### Utilitat:
- Educativa.
- Depuració d'aplicacions de xarxa.
- Anàlisi forense.
- Detecció de comportaments anòmals.
- Detectar configuracions incorrectes i atacs (DoS, ARP poisoning, MiTM).

### Exemples:
- **Tcpdump, Wireshark, Tshark**: Analitzadors de protocols.
- **Etherape, Ettercap, Bettercap, Kismet**: Monitorització i anàlisi de xarxa.

## Analitzadors de PCAP
Les eines de captura i anàlisi de paquets utilitzen el format "pcap" per guardar el tràfic.

### Exemples:
- **Tcpextract, Xplico, Network Miner, ChaosReader, Argus**: Eines per extreure i analitzar dades de captures pcap.

## Monitorització de Serveis i Servidors
A més de conèixer els dispositius en la xarxa, és vital saber el seu rendiment i estat.

### Exemples:
- **NTOP**: Monitoritza en temps real usuaris i programes que consumeixen més recursos.
- **Nagios**: Monitoritza serveis, mostra dades actives i notifica caigudes de serveis.
