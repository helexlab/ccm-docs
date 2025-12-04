---
layout: default
title: "Protseduurid"
parent: Kasutuslood
nav_order: 6
lang: et
permalink: /et/kasutuslood/protseduur/
---
# Protseduurid

## Protseduuride nimekiri
1. Sisestatud protseduure näeb, kui vasakult ülevalt menüüst valida Hoolduskoordinatsioon -> **Protseduurid**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/procedure_list.png)
3. Tulemused on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet ühel lehel. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.
5. Tabelis näeb kasutaja neid protseduure, mille täitjaks ta on.

6. Tabeli tulbad:
- **Patsient** - Hüperlingina patsiendi täispikk nimi (Perekonnanimi, Eesnimi). Peale vajutades viiakse kasutaja protseduuri andmete vaatamise ja muutmise kuvale
- **Toimumisaeg** - Protseduuri toimumise kuupäev ja kellaaeg (võib olla minevikus ja tulevikus)
- **Protseduur** - valik protseduuride loendist
- **Staatus** - Protseduuri staatus (valik loendist)

7. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Patsiendi** järgi - otsitakse patsiendi nime järgi
- **Kategooria** järgi - otsitakse protseduuri kategooria järgi
- **Protseduuri** järgi - otsitakse protseduuri järgi
- **Staatuse** järgi - otsitakse protseduuri staatuse järgi
- **Perioodi** järgi - otsitakse protseduuri toimumisaja vahemiku (või alguse või lõpu) järgi

8. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
9. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
10. Vaikimisi on tabel sorteeritud sisestamise/muutmise järjekorras. Kõige varasemalt sisestatud patsiendid esimesena. Uued (muudetud) lisatakse tabeli lõppu.
11. Soovi korral saab sorteerida vabalt valitud tabeli tulba järgi.


## Uue protseduuri lisamine

1. Uue protseduuri sisestamiseks süsteemi (protseduuride kuvalt) tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "practitioner" ehk tavakasutaja roll
2. Avaneb Protseduuri andmete sisestamise vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/add_procedure.png)
- Esimene väli on **Patsiendi** sisestamiseks. Ekraani vasakust servast avaneb patsientide otsingu kuva võimalusega uut patsienti lisada, kui juba pole süsteemis olemas.
-- Otsimiseks tuleb sisestada vähemalt üks tähemärk ning vajutada ENTER-klahvi
-- Leitud tulemuste seast saab vajutada patsiendi kaardile ning ta lisatakse Patsiendi andmeväljale
-- Kohustuslik väli
- **Kategooria** väli on valik protseduuri kategooriatest
- **Protseduur** väli on valik loendist. Kohustuslik väli
- **Esinevuse aeg** - kuupäeva ja kellaaja valik. Võib olla nii minevikus kui tulevikus. Kohustuslik
- **Teostaja** - protseduuri läbiviija. Kohustuslik andmeväli. Teostaja saab olla süsteemi spetsialist
- **Staatus** - protseduuri staatus
- **Tulem** - Protseduuri tulem. Kohustuslik andmeväli (kui protseduur on toimumas alles tulevikus, saab valida näiteks "osaline")
- **Märkused** - vabatekstiline kommentaar

3. Andmete salvestamiseks tuleb all ääres vajutada nuppu **"Salvesta"**.


## Protseduuri lisamine abivajaja vaatest
1. Protseduure saab lisada ka registreeritud abivajaja kuvalt.
2. Selleks tuleb avada abivajaja vaade ning vajutada protseduuride plokis "+Lisa"
![Screenshot]({{ site.baseurl }}/assets/images/RS_procedure.png)
3. Avaneb samasuguste andmeväljadega vaade nagu kirjeldatud peatükis "Uue protseduuri lisamine"
- Ainukeseks vaheks, et patsiendi väli on peidetud, sest kasutaja juba on patsiendi vaates
4. Peale salvestamist kuvatakse protseduuri vastavas andmeplokis
![Screenshot]({{ site.baseurl }}/assets/images/procedure_block.png)
5. Kui abivajajale on tarvis teha mitu erinevat nõustamist erinevate inimeste poolt, siis Tervisejuht saab lisada spetsialisti abivajaja meeskonda
- Loe rohkem: [Meeskond]({{ '/et/kasutuslood/meeskond/' | relative_url }})
- Loodud protseduure saab teostaja (ja tervisejuht) vajadusel muuta ja täiendada.
6. Kui luuakse patsiendiga kontakti saamisel protseduur tulevikku esmaseks nõustamiseks, siis meeldetuletuseks saab Tervisejuht endale luua Tegevuse samale päevale kommentaariga, et "nõustamine"