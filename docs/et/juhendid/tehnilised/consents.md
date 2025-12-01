---
layout: default
title: "Nõusolekud"
parent: Tehnilised juhendid
nav_order: 2
lang: et
permalink: /et/juhendid/tehnilised/nousolekud/
---
# Nõusolekud

Hoolduskoordinatsiooni projektis tegeleme kolme nõusolekuga

## Esimene nõusolek
1. Esimene nõusolek tuleb saada protsessi päris alguses, abivajaja registreerimisel.
- 439853000 - Consent given for counceling ehk Nõusolek nõustamiseks
2. Uue abivajaja registreerimisvormil on Nõusoleku andmeväli, mis on kohustuslikuks elemendiks abivajaja registreerimisel.
![Screenshot]({{ site.baseurl }}/assets/images/reg_consent.png)
3. Ilma nõusolekuta ei saa/tohi uut abivajajat registreerida.
4. Esimene nõusolek käib selle kohta, et patsiendile seletatakse, mis on Hoolduskoordinatsiooni teenus ja kes on Tervisejuht ning seda, et nõusolekut andes saab Tervisejuht ligipääsu patsiendi kontaktandmetele ning võtab lähiajal patsiendiga ühendust.
5. Kui nõusolekut ei anta, jääb protsess kohe esimeses sammus pooleli, edasi minna ei saa.
6. Kui nõusolek antakse, tekib suunajal võimalus lisada digitaalne nõusolekuvorm. See on võimalus, mitte kohustus. Oluline on, et kusagil eksisteerib päriselt patsiendi allkiri ning seda on vajadusel võimalik kätte saada.
7. Kui nõusolek on olemas ja abivajaja registreeritakse programmi, kuvatakse esmane nõusolek "lubatud" seisus automaatselt.
![Screenshot]({{ site.baseurl }}/assets/images/consents.png)
8. Vajadusel saab patsient hiljem oma nõusoleku "tagasi kutsuda", kuid esimene nõusolek käib ainult selle kohta, et Tervisejuht võib ühendust võtta. Kui see on tehtud, siis see tulemus ei muuda midagi.

## Teine nõusolek
1. Teine nõusolek tuleb Tervisejuhil küsida ja sisestada manuaalselt, kui patsient on nõustamisel ning jõutakse üheskoos sinnamaale, et on tarvis sisestada delikaatseid terviseandmeid (InterRAI küsimustiku raames, näiteks)
- 425691002 - Consent given for electronic record sharing ehk Nõusolek elektrooniliste andmete jagamiseks
2. Abivajaja registreerimisel programmi kuvatakse seda nõusolekut esialgu ilma tulemuseta (sest sellega pole veel ei nõustutud ega keeldutud)
3. Kui nõustamise/InterRAI käigus jõutakse vastavasse etappi, siis saab Tervisejuht märkida, kas nõusolek anti või mitte.
- Selleks saab "?" Nõusolek elektrooniliste andmete jagamiseks kõrval vajutada ikoonile "..." ning valida vastav tulemus (Nõustu/Keeldu)
![Screenshot]({{ site.baseurl }}/assets/images/consents.png)
4. Olenevalt tulemusest muutub abivajaja olek
- Loe rohkem: [Oleku-mootor]({{ '/et/juhendid/tehnilised/olekumootor/' | relative_url }})
5. See nõusolek annab õiguse sisestada (ja vaadata sisestatud) kliinilisi (tervise)andmeid
- Ravimid
- Diagnoosid
- jne
6. Patsient võib igal hetkel uuesti keelduda, mille peale tuleb muuta nõusoleku staatust
- See omakorda muudab Olekut ning kliiniliste andmete vaated peidetakse
7. Samamoodi võib patsient igal hetkel uuesti nõus olla ning siis "taastatakse" keelule eelnenud seis ja jätkatakse tööga.

## Kolmas nõusolek
1. Kolmas nõusolek sarnaneb esimesega selles osas, et see nõusolek tekitatakse süsteemi poolt automaatselt.
2. Kolmas nõusolek käib Heaoluplaani loomise kohta. Selleks peab Tervisejuht patsiendile seletama, mis see on, mis see tähendab, jne. Selle nõusolekuga saab patsiend nõustuda/keelduda Heaoluplaani avamisel.
3. Tervisejuhil on Heaoluplaani avamisel (registreerimisvormiga sarnaselt) andmeväli, kus linnutada nõusoleku olemasolul kastike.
- Lisaks tekib võimalus nõusolek digitaalsel kujul üles laadida.
![Screenshot]({{ site.baseurl }}/assets/images/careplan_c.png)
4. Kui nõusolekut ei anta (keeldutakse), siis Heaoluplaani avada ei tohi.
5. Iga Heaoluplaani kohta küsitakse uus nõusolek.
6. Kui Heaoluplaani avamisega on nõustutud, aga nõusolek võtakse hiljem uuesti ära (patsiendil on see õigus), siis muutub Olek ning Heaoluplaan tuleb Sulgeda (vastava staatuse ja kommentaariga)
7. Patsient võib igal hetkel nõusoleku tagasi anda ning siis saab Heaoluplaani taasavada.
8. Kui Heaoluplaani käigus otsustab patsient keelduda teisest nõusolekust (kliiniliste andmete sisestamine ja vaatamine), siis ei saa samuti Heaoluplaaniga jätkata (sisaldab terviseandmeid).