---
layout: default
title: "Spetsialistid"
parent: Kasutuslood
nav_order: 4
lang: et
permalink: /et/juhendid/kasutuslood/spetsialist/
---
# Spetsialisti lisamine süsteemi

## Spetsialistide nimekiri
1. Sisestatud spetsialiste näeb, kui vasakult ülevalt menüüst valida Haldus -> **Spetsialistid**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/practitioner_list.png)
3. Tulemused on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet ühel kuval. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.

5. Tabeli tulbad:
- **Nimi** - Hüperlingina spetsialisti "Perekonnanimi, Eesnimi". Peale vajutades viiakse kasutaja andmete muutmise kuvale (õiguste olemasolul)
- **Identifikaator** - Kõigepealt kuvatakse süsteemi kood ja siis identifikaatori sisestatud väärtus
- **Sugu** - kui valitud, siis kuvatakse spetsialisti sugu

6. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Nime järgi** - kas eesnimi, perenimi või mõlemad (komaga eraldatud)
- **Soo järgi**
- **ID järgi**, kus väärtus peab olema sisestatud täispikkuses
7. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
8. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
9. Vaikimisi on tabel sorteeritud sisestamise/muutmise järjekorras. Kõige varasemalt sisestatud patsiendid esimesena. Uued (muudetud) lisatakse tabeli lõppu. Sorteerimist ei saa antud vaates muuta.

## Uue spetsialisti lisamine

1. Uue spetsialisti sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "ict" ehk administraatori/haldaja roll
2. Avaneb andmete vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/practitioner_add.png)
- Esimene plokk on **ID** sisestamiseks. Mugavaks kasutuseks on süsteemi valikuteks seadistatud "Eesti isikukood" ja "TAI ametlik tervishoiutöötaja ID"
-- **Väärtuse** lahtrisse tuleb sisestada siis kas antud isikukood või passi number
-- **Kehtib kuni** väli tähendab ID kehtivuse kuupäeva, kui seda on tarvis lisaks üles märkida
- Teine plokk on **Nimede ja administratiivsete andmete** sisestamiseks, kusjuures eesnimesid võib lisada rohkem kui ühe korra
-- **Sugu**
-- **Sünnipäev** - (pp.kk.aaaa) võimalusega kirjutada või kalendrist valida
- Kolmas plokk on **Rollide** kohta. Saab lisada mitu.
-- Tuleb kirjeldada **Orgaisatsioon/asutus** (loe rohkem: [Organisatsioonid]({{ '/et/juhendid/kasutuslood/asutus/' | relative_url }}))
-- **Roll** ehk millises rollis antud töötaja valitud organisatsioonis on
-- **Aadress** - asutuse aadress
-- **Suhtluskanalid** - telefon ja e-mail, läbi mille on võimalik spetsialistiga ühendust võtta. Kui lisatud, kuvatakse abivajajale väljatrükil
-- **Suhtlus** - suhtluskeeled
-- **Kättesaadavus** - E-R võimalik valida, millistel päevadel ja millistel kellaaegadel võib abivajaja antud spetsialistiga ühendust võtta. Näiteks E 09:00-16:00, K 12:00-17:00. Pole kohustuslik, aga kui on lisatud, kuvatakse abivajajale väljatrükil

3. Andmete salvestamiseks tuleb üleval paremal nurgas vajutada nuppu **"Salvesta"**.
4. Juba lisatud andmete/andmeplokkide kustutamiseks tuleb vajutada andmevälja/andmeploki juures olevat "X" nuppu.
