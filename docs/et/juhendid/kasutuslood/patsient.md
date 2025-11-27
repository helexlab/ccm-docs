---
layout: default
title: "Patsiendid"
parent: Kasutuslood
nav_order: 1
lang: et
permalink: /et/juhendid/kasutuslood/patsient/
---
# Patsiendi/abivajaja lisamine süsteemi

## Patsientide nimekiri
1. Sisestatud patsiente näeb, kui vasakult ülevalt menüüst valida Haldus -> **Patsiendid**.
2. Avaneb patsientide nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/patsiendi_nimekiri.png)
3. Patsiendid on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 patsienti ühel kuval. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.

5. Tabeli tulbad:
- **Nimi** - Hüperlingina patsiendi "Perekonnanimi, Eesnimi". Peale vajutades viiakse kasutaja patsiendi andmete muutmise kuvale
- **Identifikaator** - Kõigepealt kuvatakse süsteemi kood ja siis identifikaatori sisestatud väärtus
- **Sugu** - kui valitud, siis kuvatakse patsiendi sugu

6. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Nime järgi** - kas eesnimi, perenimi või mõlemad (komaga eraldatud)
- **Soo järgi**
- **ID järgi**, kus väärtus peab olema sisestatud täispikkuses
7. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
8. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
9. Vaikimisi on tabel sorteeritud sisestamise/muutmise järjekorras. Kõige varasemalt sisestatud patsiendid esimesena. Uued (muudetud) lisatakse tabeli lõppu.

## Uue patsiendi lisamine

1. Uue patsiendi sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "practitioner" ehk kõige tavalisem "kasutaja" roll
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
