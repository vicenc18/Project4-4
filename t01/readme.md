# Fase 1: Treball individual
Ha l'hora de proritzar la importancia ho el orde en que compiar/guardar les dades dels 10 equips hauria de ser:
1. El servidor:
   En el servidor es on estroben totes les dades dels usuaris debut aixo es vital fer una copia de seguretat
2. Base de dades:
   És molt nesesari mantenir una copia de la base de dades dels clients ja que a qui es guarden tot el tema de comptabilitat  pagaments,diners,nomines,etc.. i tambe les dades dels clients.
3. Carpetes Personals dels Usuaris:
   Si esl veritat que no es tant important com el dos primer pero tambe es nesesari fer una copia ja que es on el usuaris tenen la feina diaria

---




Aquestes dades **canvien constantment** i són les més sensibles de tota l’empresa.  
S'hi registren operacions diàries, tràmits comptables, dades de clients i informació que **no es pot perdre**.  
Per això, tant el **RTO** (temps màxim per recuperar-les) com el **RPO** (quantitat màxima de dades que es poden perdre) són **molt estrictes**:

-RTO < 4 hores 
  RPO < 4 hores

Per complir aquests requisits, es defineix un calendari de còpies molt freqüent i fiable.


### Tipus de còpia aplicat

Còpia incremental cada 4 hores**  
  Només es guarden els canvis realitzats des de la darrera còpia.  
  Això permet tenir còpies molt actualitzades sense ocupar massa espai.

  Còpia completa diària (durant la nit)**  
  Aquesta còpia inclou *tota* la base de dades.  
  Serveix com a punt de restauració estable i coherent per si cal restaurar tot el sistema.


### Calendari proposat

#### Còpies incrementals (cada 4 hores):
 06:00  
 10:00  
 14:00  
 18:00  
 22:00  

#### Còpia completa diària:
02:00 de la matinada

Aquesta hora és ideal perquè hi ha menys activitat al servidor i la còpia no afecta el rendiment durant les hores de treball.


### Justificació detallada

Les còpies incrementals cada 4 hores garanteixen que, en cas d’error o fallada, la pèrdua màxima de dades sigui inferior al RPO fixat (4 hores).  
  Això assegura que la informació de comptabilitat i clients es mantingui pràcticament intacta.

La còpia completa diària permet disposar sempre d’un punt de restauració fiable.  
  En cas que es corrompi una incremental o sigui necessari restaurar tota la base de dades, aquesta còpia completa facilita un procés de recuperació **més ràpid i senzill**.

La combinació de **incrementals freqüents + completa diària** minimitza l’espai d’emmagatzematge necessari i alhora compleix tots els requisits de seguretat i recuperació del sistema.
---

## Mitjans i Ubicació (Regla 3-2-1)

### Mitjans recomanats
NAS local:  
  Per emmagatzemar les còpies **diàries i incrementals**. És ràpid i permet una recuperació immediata.

  Núvol (Cloud):  
  Per guardar les còpies **setmanals o mensuals** fora de les instal·lacions. Protegeix davant robatoris, incendis o desastres.

  Disc dur extern:  
  Per les còpies **mensuals d’arxiu**, mantingut desconnectat per evitar riscos de ransomware.

---

### Ubicació (seguint la regla 3-2-1)

1a còpia — NAS local (on-site):  
  Conté les còpies incrementals i les còpies completes diàries.

2a còpia — Disc extern (on-site separat):  
  Còpies completes setmanals o mensuals, guardades en un espai segur o físicament separat del servidor.

3a còpia — Cloud (off-site):  
  Còpia completa mensual per garantir que les dades es poden recuperar encara que tota la infraestructura local falli.

---

   
