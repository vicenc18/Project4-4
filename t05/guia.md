#   SSH — Guia Completa amb Evidències (Activitat T05)

## 1. Descripció de l’Activitat

El propòsit d’aquesta activitat és aprendre i documentar com establir connexions SSH entre clients i servidors en un entorn segur simulat amb màquines virtuals.

### Objectius principals:
- Crear un entorn amb 3 màquines virtuals:
  - **Client Windows**
  - **Servidor Linux amb SSH actiu**
- Realitzar connexions SSH des de Linux i Windows.
- Comprovar el funcionament del protocol.
- Registrar el procés amb captures de pantalla.
- Deixar un document que servirà de base per a futurs becaris de la consultora.

---

## 2. Entorn de Proves

| Màquina | Sistema | Rol |
|--------|---------|-----|
| Client Windows | Windows 10/11 | Origen de connexió SSH |
| Servidor Linux | Ubuntu / Debian | Destí de la connexió SSH |

### instalacio de shh al servidor 
El primer pas per permetre connexions remotes és assegurar que el servidor Linux tingui instal·lat el servei OpenSSH Server, que és el paquet responsable de rebre i gestionar connexions SSH entrants.
L’ordre següent instal·la el servidor SSH en sistemes basats en Ubuntu/Debian:
``` bash
sudo apt install ssh
```
![instalacio ssh](IMG/intallshh.png)
Per verificar que el servei SSH està en funcionament al servidor, s’utilitza la comanda:

### L'estat d' el ssh 
``` bash
sudo systemctl status ssh
```
![status ssh](IMG/status.ssh.png)
En aquest pas, ens connectem des del nostre equip Windows al servidor Linux utilitzant el client SSH incorporat a PowerShell o Windows Terminal.
## ens conectem al servidor per ssh 
``` bash
ssh usuari@IP servidor
```

![ssh conectar a windous](IMG/sshconectecio.png)

## Creem el segon usuari
Per afegir un nou usuari al servidor, utilitzem la comanda:
``` bash
sudo adduser nomdelusuari
```
![add user2](IMG/user2.png)

