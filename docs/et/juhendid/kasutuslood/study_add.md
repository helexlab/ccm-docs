---
layout: default
title: "Programm"
parent: Kasutuslood
nav_order: 2
lang: et
permalink: /et/juhendid/kasutuslood/programm/
---
# Programmide/raviteekondade lisamine süsteemi

## Programmide nimekiri
1. Sisestatud programe näeb, kui vasakult ülevalt menüüst valida Haldus -> **Programmid**.
2. Avaneb programmide nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/study_table.png)
3. Programmid on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 programmi ühel kuval. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.

5. Tabeli tulbad:
- **Kood** - Hüperlingina programmi süsteemne unikaalne kood, millele vajutades viiakse kasutaja programmi andmete muutmise kuvale
- **Nimi** - Programmi inimloetav nimi süsteemi valitud keeles
- **Staatus** - programmi staatus süsteemis. "Aktiivne" on roheline, "Kehtetu" punane, "Mustand" kollane, "Teadmata" hall

6. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Koodi** järgi - tuleb sisestada täispikk süsteemne kood
- **Nime** järgi - võib sisestada osalise või täispika programmi inimloetava nime
- **Spetsialisti** järgi - otsingu lahter süsteemi sisestatud spetsialistide nimekirjast. Otsinguks tuleb sisestada vähemalt kaks tähemärki
- **Staatuse** järgi

7. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
8. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
9. Vaikimisi on tabel sorteeritud sisestamise järjekorras, aga soovi korral saab kasutaja sorteerida koodi järgi tähestikulises jrk või staatuste järgi.

## Uue programmi/raviteekonna lisamine

1. Uue programmi sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "practitioner" ehk kõige tavalisem "kasutaja" roll
2. Avaneb Programmi andmete vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/add_study.png)
- Esimene väli on **Kood**, mis on kohustuslik ja peab olema süsteemis unikaalne.
- **Nimi** koos tõlgetega, kus vähemalt ühes keeles nime sisestamine on kohustuslik. Uue keele saab valida, vajutades **"Lisa tõlge"**
- **Kirjeldus** - Siia saab vabatekstiliselt lisada täpsustusi antud programmi kohta. Näiteks kirjeldada tänavaid, muid omapärasid, jne.
- **Teenuse asukoht** - siin on täpsem valik asukohtadest, et abivajaja sisestajal oleks lihtsam navigeerida ja leida õige programm. Saab lisada rohkem kui ühe teenuse asukoha.
- **Järjestus** - selle valiku antud lahenduses saame vajadusel peita, hetkel tuleks valida "CCM default sequence"
- **Staatus** - programmi/raviteekonna staatus. Saab vajadusel pärast muuta
- **Osapooled** - Selleks, et abivajaja sisestajal süsteemi oleks võimalik abivajaja koheselt suunata tervisejuhti töölauale, tuleks programmi sisestamisel ära defineerida vähemalt roll **vastutav tervisejuht**. Selleks on otsingu väli süsteemi spetsialistidest. Saab valida rohkem kui ühe (mõnel programmil võib olla mitu). Lisaks saab soovi korral defineerida baas-meeskonna välja **meeskonnaliige** kaudu. See ei ole selles sammus kohustuslik, aga muudab hilisemas sammus, heaoluplaani luues, meeskonnaliikmete valiku tervisejuhi jaoks lihtsamaks.

3. Andmete salvestamiseks tuleb üleval paremal nurgas vajutada nuppu **"Salvesta"**.
