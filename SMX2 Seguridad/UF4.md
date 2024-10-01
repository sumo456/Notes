# SEGURETAT ACTIVA: MALWARE

## ATACS CONTRA DADES I APLICACIONS: EL MALWARE
El malware és un tipus de software que té com a finalitat infiltrar-se o danyar un ordinador sense el consentiment del seu propietari.

### Tipus de Malware:
- **Virus**: Microprograma que té la capacitat de replicar-se a si mateix i propagar-se infectant altres software.
- **Gusano**: No depenen d'arxius portadors per contaminar sistemes. Realitzen còpies de si mateixos en la memòria RAM a la màxima velocitat possible.
- **Troiano**: Software nociu amb aparença de programa legítim.
- **Backdoor**: Software que permet accés al sistema del ordinador ignorant el procediment normal d'autenticació.
- **Bomba lògica**: Objectiu destruir les dades d'un ordinador o causar altres mals de consideració quan es compleixen certes condicions.
- **Spyware**: Software que recull i envia informació.
- **Adware**: Mostra publicitat.
- **Ransomware**: Programa que restringeix l'accés als arxius d'un ordinador.
- **Hoaxes**: Missatges enganyosos que es difonen massivament per internet.
- **Rootkit**: Software inserit en un ordinador després d'obtenir control en un sistema.

## OBJECTIUS DEL MALWARE
- Monitoritzar i espiar usuaris.
- Robar informació.
- Robar identitat i credencials.
- Destruir dades dels dispositius connectats i accessibilitats.
- Aconseguir el control dels equips de forma remota o local.
- Robar diners i extorsionar als usuaris.

## DEFECTES DE SEGURETAT DEL SOFTWARE
- **Errors de programació**: Programació de les aplicacions de forma no segura.

## CONFIGURACIÓ ERRÒNIA DEL SISTEMA
- **Instal·lació sense configuració**.
- **Instal·lació de serveis sense configuració**.
- **Sistemes sense limitacions**.

## DISSENY INSEGUR O ERRORS D'USUARIS
- Arrencar des de dispositius infectats per malware.
- Càrrega automàtica de codi HTML infectat en navegadors.
- Execució de software que arriba via pendrive.

## CODI O USUARIS AMB MÉS PRIVILEGIS DE LA COMPTE
- Limitació de drets i quotes.
- Utilitzar usuaris sense privilegis sempre.
- Utilitzar sudo o run as momentàniament.
- Mai fer chmod 777 o donar control total a sistemes de fitxers.

## ÚS DEL MATEIX SISTEMA OPERATIU
- Utilitzar el mateix sistema operatiu en tots els equips.

## ANTI-MALWARE
Dissenyat per detectar i eliminar, si és possible, amenaces.

### Firmes de virus i malware
- Empreses recullen mostres de malware i les analitzen en busca de patrons.

### Heurística
- Analitzar el comportament dels programes per detectar malware nou o desconegut.

### Sandbox
- Mecanisme de seguretat per executar software per separat.

### Registrar hash de fitxers
- Aquesta tècnica consisteix en generar una base de dades amb el hash de tots els fitxers del sistema.

---

# CRIPTOGRAFIA

## Models de Cifrat
### Cifrat Simètric
- Mètode utilitzat des dels inicis de la criptografia. Només s'utilitza una clau per xifrar i desxifrar.

### Cifrat Asimètric
- Mètode que va aparèixer durant la Segona Guerra Mundial. Utilitza dues claus, una pública i una privada.

## Cifrat Simètric
Els sistemes clàssics de cifrat no són prou robustos per als ordinadors actuals. En molt poc temps es pot obtenir la clau per força bruta. 

### Algoritmes clàssics
- Scytala
- César / ROT-13
- Substitució
- Vigenère

### Algoritmes actuals
- DES
- 3DES
- RC5
- AES
- Blowfish
- IDEA

#### Avantatges:
- Assegurar la confidencialitat.
- Rapidesa de xifrat i desxifrat.
- Utilització en comunicacions interactives.

#### Desavantatges:
- Problemes d'intercanvi de claus.
- No assegura autenticació ni integritat.
- Necessita una clau per cada parella d'entitats.

## Cifrat Asimètric
### Ús
- Cifrat amb clau pública per assegurar la confidencialitat.
- Cifrat amb clau privada per assegurar l'autenticació.

#### Avantatges:
- Ofereix confidencialitat i autenticació.
- Utilitzat per intercanvi de claus simètriques de forma segura.

#### Desavantatges:
- Més lent i claus més llargues.
- Missatges xifrats ocupen més espai.

### Algoritmes actuals:
- Diffie-Hellman
- RSA
- DSA
- ElGamal
- Criptografia de corba el·líptica

## Funcions de Hash
Generen un valor de mida fixa i són irreversibles. Utilitzats per assegurar la integritat de les dades.

### Exemples:
- MD5
- SHA-1
- SHA-2

### Ús pràctic:
- Validar integritat de fitxers.
- Guardar contrasenyes de manera segura.
- Firma digital.

## Cifrat Híbrid
- **Asimètric** per enviar la clau secreta.
- **Simètric** per xifrar les dades.
- Clau de sessió utilitzada només durant la sessió. Interceptar-la no servirà per a una altra sessió.
