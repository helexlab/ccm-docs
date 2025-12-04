---
layout: default
title: "Patsiendid"
parent: Kasutuslood
nav_order: 1
lang: et
permalink: /et/kasutuslood/patsient/
---
# Patsiendid
**Patsient** on süsteemi administratiivne üksus (isik), kelle kohta talletatakse kontaktandmed, nimed, identifikaatorid ja muu demograafiline info.  
Patsiendi lisamine ei tähenda veel programmis osalemist.  
Patsiendist saab **abivajaja (Research Subject)** alles siis, kui ta registreeritakse mõnda programmi/raviteekonda.

---

## Patsientide nimekiri
1. Sisestatud patsientide nimekirja näeb menüüst (vasakult ülevalt) **Haldus -> Patsiendid**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/patsiendi_nimekiri.png)
3. Tulemusi kuvatakse lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet, seda saab muuta, vajutades tabeli allääres olevale numbriväljale.

### Tabeli tulbad
- **Nimi** - Hüperlink kujul "Perekonnanimi, Eesnimi". Peale vajutades avaneb patsiendi andmete muutmise kuva
- **Identifikaator** - identifikaatori tüüp ja sisestatud väärtus
- **Sugu** - valitud sugu, kui see määratakse

### Filtrid
Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Nime järgi** - sisestades eesnime, perenome või osa nimest
- **Soo järgi**
- **ID järgi**, identifikaator peab olema täispikkuses
5. Filtri rakendamiseks tuleb vajutada nupule "Otsi" või ENTER.
6. Kõik rakendatud filtrid saab korraga eemaldada, vajutades **"Tühista kõik"**.
7. Vaikimisi on tabel sorteeritud loomise/muutmise aja järgi. Kõige varasemalt sisestatud kirjed esimesena. Uued lisatakse tabeli lõppu.

---

## Uue patsiendi lisamine

1. Uue patsiendi sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- Nupp on nähtav kasutajatele rolliga "practitioner" (kõige tavalisem "kasutaja")
2. Avaneb Patsiendi andmete vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/patsiendi_andmed.png)
- Esimene plokk on **ID** sisestamiseks. Mugavaks kasutuseks on süsteemi valikuteks seadistatud "Eesti isikukood" ja "Vene passi number"
-- **Väärtuse** lahtrisse tuleb sisestada siis kas antud isikukood või passi number
-- **Kehtib kuni** väli tähendab dokumendi kehtivuse kuupäeva, kui seda on tarvis lisaks üles märkida
- Teine plokk on **Nimede** sisestamiseks, kusjuures eesnimesid võib lisada rohkem kui ühe korra
- Kolmas plokk on administratiivsed andmed, kus saab märkida patsiendi **sugu** (loendist), **sünniaega** ning **keeli**, mida patsiendiga suheldes kasutada
- Neljas plokk on kättesaadavuse kohta, kuhu saab sisestada **telefoninumbri**, **e-maili**, jms. ning nende väärtused.
-- Telefoninumbri sisestamine on oluline tervisejuhile patsiendiga kontakti loomiseks.
- **Aadressi** välja (hetkel loend tõlkimata ja Eesti = Estonia) sisestamisel, valides Eesti, kasutatakse  aadresside registrit
- Seotud isikute plokis saab lisada patsiendi lähedaste infot
-- **Nimi**
-- **Suhe patsiendiga**
-- **Suhtluskanal** ehk mobiilside
-- **Aadress**

3. Andmete salvestamiseks tuleb üleval paremal nurgas vajutada nuppu **"Salvesta"**.
