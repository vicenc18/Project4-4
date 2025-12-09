# Implementació d’un Servidor NFS en Entorns Linux
## Demo per al Client DevOptimize Solutions
## 🧩 Introducció

En aquest projecte abordem un requisit tècnic molt habitual entre els nostres clients: la centralització de dades en entorns Linux.

El nostre client, DevOptimize Solutions, és una startup de desenvolupament de programari que treballa exclusivament amb Linux. Actualment, pateixen un problema greu: el seu codi font i actius (documents de disseny, scripts, etc.) es troben dispersos en còpies locals entre diversos desenvolupadors.
Això genera conflictes de versió, pèrdua d’eficiència i dificultats en la gestió del treball.

Per resoldre aquesta situació, ens han contractat per implementar un servidor de fitxers centralitzat. Atès que tot l'entorn és Linux, la solució òptima i nativa és NFS (Network File System), concretament NFSv3.

## 🎯 Objectiu del Projecte

L’objectiu principal és crear una demostració funcional per mostrar al client:
Com es desplegarà la solució proposada.
Quines funcionalitats ofereix NFS.
Quines són les seves limitacions, especialment en entorns sense autenticació centralitzada.

## 🏗️ Requisits del Client

DevOptimize Solutions ha remarcat que:
No utilitzen un entorn d’autenticació centralitzada (LDAP, Kerberos, AD...).
No tenen previsió d’implementar-ne cap, per ara.
Per tant, els permisos i el control d’accés han de basar-se exclusivament en:
La configuració de /etc/exports al servidor NFS.
Els permisos POSIX del sistema de fitxers (chmod, chown, usuaris i grups).

## 🧪 Demostració a Realitzar

Per completar la demo, s’ha de crear:
## 🖥️ 1. Un servidor NFS (NFSv3)

Inclourà:
Configuració de directoris exportats.
Opcions de seguretat i permisos.
Ajustos en /etc/exports.

## 💻 2. Un client Linux

Aquest client:
Es connectarà i muntarà els recursos NFS.
Provarà l’accés segons permisos assignats.

## 👥 3. Usuaris i grups simulats

Per reflectir la realitat del client, caldrà:
Crear usuaris i grups locals equivalents als desenvolupadors.
Verificar com NFS gestiona permissos basats en UID/GID.
Mostrar el comportament d’accés restringit o permès.
