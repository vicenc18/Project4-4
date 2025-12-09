# Guia servei NFS
---
## 1. lo primer que sera es updatejar el servidosr ho la maquina:  

Abans de tot haurem de posar la màquina al dia.  
```bash
sudo apt update && sudo apt upgrade -y
```
![captura de upgrade](IMG/captura.upgrade.png)

## reació d’un nou usuari

A la captura es mostra la creació de l’usuari dev01 mitjançant adduser.

🔧 Comanda utilitzada:
sudo adduser dev01

📋 Què fa aquesta comanda?

Crea l’usuari dev01.

Assigna automàticament un UID i un GID dins el rang d’usuaris locals.

Crea el directori personal /home/dev01.

Copia els fitxers inicials de /etc/skel.

Demana una contrasenya nova.

Permet afegir informació addicional (opcional).

Finalment, afegeix l’usuari al grup suplementari users (a Debian/Ubuntu).

📝 Resultat esperat:
Adding user `dev01' ...
Adding new group `dev01' ...
Adding new user `dev01' (1003) with group `dev01' (1003) ...
Creating home directory `/home/dev01' ...
...

📌 2. Creació de grups personalitzats

Després es creen dos grups addicionals per organitzar permisos:

devs → Grup de desenvolupadors

admin → Grup d’administradors

🔧 Comandes utilitzades:
sudo groupadd devs
sudo groupadd admin
