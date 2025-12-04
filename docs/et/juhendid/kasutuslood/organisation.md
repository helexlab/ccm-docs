---
layout: default
title: "Asutused"
parent: Kasutuslood
nav_order: 3
lang: et
permalink: /et/kasutuslood/asutus/
---
# Asutused

## Organisatsioonide nimekiri
1. Sisestatud organisatsioone näeb, kui vasakult ülevalt menüüst valida Haldus -> **Asutused**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/org_list.png)
3. Tulemused on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet ühel lehel. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.

5. Tabeli tulbad:
- **Nimi** - Hüperlingina asutuse täispikk nimi. Peale vajutades viiakse kasutaja asutuse andmete muutmise kuvale
- **Identifikaator** - Kõigepealt kuvatakse süsteemi kood ja siis identifikaatori sisestatud väärtus

6. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Nime järgi** - otsitakse asutuse nime alguse järgi (nt ei leita tulemusteks "Keila Sotsiaalkeskus" ja "Jõhvi Sotsiaalmaja", kui otsingusõna on "Sotsiaal". Vaste leitakse, kui kirjutatakse nime algus, nt "Jõh")
- **ID järgi**, kus väärtus peab olema sisestatud täispikkuses
7. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
8. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
9. Vaikimisi on tabel sorteeritud sisestamise/muutmise järjekorras. Kõige varasemalt sisestatud patsiendid esimesena. Uued (muudetud) lisatakse tabeli lõppu.

## Uue asutuse lisamine

1. Uue asutuse sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "ict" ehk administraatori roll
2. Avaneb Organisatsiooni andmete vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/add_org.png)
- Esimene plokk on **ID** sisestamiseks. Mugavaks kasutuseks on süsteemi valikuteks seadistatud "Eesti äriregistri kood", "KMKR number" ja "TAI tegevusloa number"
-- **Väärtuse** lahtrisse tuleb sisestada siis kas antud ID väärtus
-- **Kehtib kuni** väli tähendab väärtuse kehtivuse kuupäeva, kui seda on tarvis lisaks üles märkida
-- Ühele asutusele võib lisada mitu identifikaatorit (igast "süsteemist" ühe)
- Teine plokk on **Nimede** sisestamiseks.
-- Täispikk organisatsiooni nimi
-- Varjunimi või lühinimi (nt PERH)
- **Aktiivne** - organisatsiooni staatuse valik. Aktiivne, kui linnutatud, mitteaktiivne, kui tühi.

3. Andmete salvestamiseks tuleb all ääres vajutada nuppu **"Salvesta"**.
