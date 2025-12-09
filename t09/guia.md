# Guia servei NFS
---
## 1. lo primer que sera es updatejar el servidosr ho la maquina:  

Abans de tot haurem de posar la màquina al dia.  
```bash
sudo apt update && sudo apt upgrade -y
```
![captura de upgrade](IMG/captura.upgrade.png)

## 2 reació d’els nou usuari
A la captura es mostra la creació de l’usuari dev01 mitjançant adduser.

![creacio dels usuaris](IMG/creaciodelusuariadmin01.png)

Comanda utilitzada:
``` bash
sudo adduser nom del nou usuari
```
Què fa aquesta comanda?

- Crea l’usuari 

- Assigna automàticament un UID i un GID dins el rang d’usuaris locals.

- Crea el directori personal /home/nom del usuari.

- Copia els fitxers inicials de /etc/skel.

- Demana una contrasenya nova.

- Permet afegir informació addicional (opcional).

- Finalment, afegeix l’usuari al grup suplementari users (a Debian/Ubuntu).


...

2. Creació de grups personalitzats

Després es creen dos grups addicionals per organitzar permisos:

devs → Grup de desenvolupadors

![devs](IMG/creaciodelsgrups.png)

admin → Grup d’administradors

![admin](IMG/groupaddadmin01.png)

🔧 Comandes utilitzades:
sudo groupadd devs
sudo groupadd admin
