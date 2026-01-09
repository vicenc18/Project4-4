# T02: DPR – Còpies de seguretat. Cas pràctic

## Breu descripció
En aquesta tasca es posa en pràctica la política de còpies de seguretat dissenyada prèviament per al client **Muntatges i Serveis Tècnics SL**, mitjançant guies tècniques i proves de concepte.

---

## Part 1: Còpia de seguretat equips Windows
- Excepció per a l’equip Windows del director.
- Esquema **3-2-1** amb:
  - Disc secundari local.
  - Cloud (Google Drive) amb **Duplicati**.
- VM Windows 11 amb dos discos.
- Còpies del perfil d’usuari:
  - Cada hora al disc local.
  - A les 18:00 al cloud.
- Proves de restauració local i des del cloud.

---

## Part 2: Còpia de seguretat servidor Linux
- VM **Ubuntu Server** amb segon disc de 10 GB.
- Ús de **Duplicity** per fer còpies de `/home`.
- Còpies completes i incrementals amb proves de restauració.
- Automatització amb **scripts** i **cron**:
  - Còpia completa: diumenges a les 23:00.
  - Còpies incrementals: dilluns a dissabte a les 23:00.
- La unitat de backup es munta i desmunta automàticament per seguretat.

---

## Materials de suport
- Duplicati  
- Duplicity (man page)  
- Programació de tasques amb cron

---

## Lliurament
- Carpeta al repositori amb:
  - `README.md`
  - Guia tècnica amb proves de concepte
- Enllaç lliurat al Moodle.

