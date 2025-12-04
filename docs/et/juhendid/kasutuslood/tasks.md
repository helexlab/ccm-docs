---
layout: default
title: "Tegevused"
parent: Kasutuslood
nav_order: 9
lang: et
permalink: /et/kasutuslood/tegevused/
---
# Tegevused/Ülesanded

## Tegevuste nimekiri
1. Sisestatud tegevusi näeb, kui vasakult ülevalt menüüst valida Hoolduskoordinatsioon -> **Tegevused**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/task_list.png)
3. Tulemused on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet ühel lehel. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.
5. Tabelis näeb kasutaja neid tegevusi, mille täitjaks ta on või mida ta ise on loonud.

6. Tabeli tulbad:
- Loetud/lugemata uuendused - Silma ikoon tekib nende kirjete ette, mis on lisatud või milles on kellegi teise poolt tehtud muudatus. See ikoon püsib seni, kuni kasutaja ülesande avab ja muudatusi näeb.
- **Tegevus** - Hüperlingina ülesande ID ning Tegevuse Tüüp. Peale vajutades viiakse kasutaja tegevuse vaatamise ja muutmise kuvale
- **Kellega seotud** - Hüperlingina patsiendi täispikk nimi (Perekonnanimi, Eesnimi). Peale vajutades viiakse kasutaja patsiendi andmete vaatamise ja muutmise kuvale
- **Vastutaja** - Nimekiri vastutaja(te)st, keda on selle tegevusega seotud. Isik või isikud, kellelt oodatakse selle tegevuse läbiviimist. Kui valitakse mitu, tuleb täitjate seast valida üks, kes on selle ülesande "omanik" või peamine vastutaja. Tema nimi kuvatakse paksus kirjas. Peamine vastutaja on täpselt üks inimene. Kui täitjaid ongi ainult üks lisatud, siis tema = vastutaja ja seda lisavälja eraldi ei kuvata.
- **Autor** - Ülesande looja, orginaalne autor. Tegevuste nimekirjas kuvatakse kasutajale tegevusi, mille on kas tema loonud või mis on temale suunatud (täitja/vastutaja)
- **Tähtaeg** - Tegevuse teostamise tähtaeg. Kui tähtaeg = täna või on kuupäev minevikus, kuvatakse seda punases kirjas. Tähtaega saab kasutaja muuta ja seda ei pea üldse lisama (võib jätta tühjaks)
- **Staatus** - Ülesande/tegevuse staatus (erinevad staatused on kuvatud erineva värviga)

7. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **ID või kirjelduse** järgi - otsitakse tegevuse ID, nt 002 või ülesande sees salvestatud kirjelduse järgi (mida tabelis visuaalselt ei kuvata)
- **Tüübi** järgi - otsitakse tegevuse tüüpide loendist. Need kuvatakse tabelis kohe ID kõrval
- **Staatuse** järgi - otsitakse tegevuse staatuse järgi
- **Prioriteedi** järgi - otsitakse tegevuse prioriteedi järgi (kui valitud)
- Lisavõimalused otsida:
-- **Minu poolt loodud**, mis määrab "Suunaja" väljaks sisseloginud kasutaja
-- **Minu tegevused**, mis määrab "Täitja" väljaks sisseloginud kasutaja
-- **Tähtaeg täna või möödunud**, mis määrab perioodi lõppajaks tänase kuupäeva
- **Kellega seotud** - Praeguses lahenduses saab ülesandeid siduda ainult patsiendiga. Seepärast on see loend ainult ühe võimaliku väärtusega
- **Täitja** - Kui täitjaks (ülesande lahendajaks) on keegi teine peale sisseloginud kasutaja, siis kuvatakse tabelis ainult selliseid, kus autor=sisseloginud kasutaja
- **Suunaja** - ülesande loonud isik (autor). Kui valida keegi teine peale sisseloginud kasutaja, siis kuvatakse tabelis ainult selliseid, kus täitja=sisseloginud kasutaja
- **Periood** - Saab otsida tegevusi kindla perioodi seest. Võib ka määrata ainult alguse või lõppkuupäeva
- **Lugemata** - Kui linnutada "lugemata muudatused", kuvatakse kasutajale ainult need kirjed, mis on lisandunud või kus on toimunud muudatusi võrreldes eelmise korraga, kui kasutaja ülesannet vaatas. Kuvatakse kõik "silma" ikooniga kirjed.
- **Muudetud** - Saab otsida perioodi või ühe kuupäeva järgi, et filtreeritakse tegevusega tehtud muudatusi. Näiteks, näita mulle kõiki tegevusi, milles on toimunud muudatusi, alates eilsest.

8. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
9. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
10. Vaikimisi on tabel sorteeritud sisestamise/muutmise järjekorras. Kõige varasemalt sisestatud tegevused esimesena. Uued (muudetud) lisatakse tabeli lõppu.
11. Soovi korral saab sorteerida vabalt valitud tabeli tulba järgi (väljaarvatud "kellega seotud").


## Uue tegevuse lisamine Tegevuste nimekirjast
Tegevusi saab lisada kahest eraldi kohast: tegevuste nimekirjast ja abivajaja vaatest.
Kõigepealt kirjeldan tegevuse lisamist Tegevuste nimekirjast.
1. Uue tegevuse sisestamiseks süsteemi (tegevuste nimekirjast) tuleb vajutada paremal tabeli kohal olevat **"+Lisa tegevus"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "practitioner" ehk tavakasutaja roll
2. Avaneb Tegevuse andmete sisestamise vaade erinevate andmeväljadega:
![Screenshot]({{ site.baseurl }}/assets/images/task_from_list.png)
3. Tegevuse loomisel on vaikimisi Staatuseks "Planeerimisel". Peale tegevuse salvestamist avaneb valik järgmistest staatustest: Teostamisel, Teostatud, Katkestatud.
4. **Tüüp** on justkui tegevuse kategooria, mida saab valida etteantud väärtuste hulgast
5. **Kirjeldus** on vabatekstiline kirjeldus tegevuse sisu kohta. Saab kasutada eraldi sümboleid, et teksti kajastada paksus kirjas või kaldkirjas või punktidena. Peale kirjelduse lisamist tuleb vajutada linnukesele, et kirjeldus salvestada.
![Screenshot]({{ site.baseurl }}/assets/images/syntaks.png)
![Screenshot]({{ site.baseurl }}/assets/images/syntaks_tulemus.png)
6. Paremal pool on automaatselt valitud "kellega seotud" = Patsient. Käesolevas projektis teisi valikuid ei kasutata.
- Saab valida patsiendi süsteemist, kellega tegevust siduda (ei pea olema registreeritud abivajaja)
- Kui patsient puudub, saab tegevuse käigus patsiendi valimisel uue patsiendi süsteemi sisestada
- Loe lähemalt: [Patsient]({{ '/et/kasutuslood/patsient/' | relative_url }})
- Saab tegevuse lisada ka Patsienti valimata.
7. **Täitja** - igal tegevusel peab olema määratud vähemalt üks täitja. Kui on valitud täpselt 1, siis täitja=vastutaja.
8. Kui on valitud rohkem kui üks Täitja, kuvatakse lisaks **Vastutaja** väli, kus vaikimisi määratakse vastutajaks esimesena sisestatud Täitja. Kasutaja saab valikut muuta ja valida ükskõik kelle täitjate seast. See kasutaja on justkui peamine vastutaja või ülesande "omanik", kes peab tegevuse läbi viima.
9. Ülesandele saab määrata alguse aega, vahemikku ja/või tähtaega. Kui tähtaeg saab ületatud või on täna, värvub see tegevuste nimekirjas tähelepanu püüdmiseks punaseks.
10. Tegevustel on **Prioriteet**. Vaikimisi "Tavaline".

11. Andmete salvestamiseks tuleb üleval ääres vajutada nuppu **"Salvesta"**.
12. Peale salvestamist ei ole enam võimalik muuta väärtust väljal "Kellega seotud".
13. Peale tegevuse loomist ja salvestamist logitakse ja kuvatakse kõik muudatused plokis **Aktiivsus**.
- Lühikokkuvõtet esialgsest ülesande loomisest ja viimasest muudatusest saab kohe tegevust avades lugeda "Staatus" välja kohalt.
- "Aktiivsus" plokis on võimalik peale tegevuse esmast salvestamist lisada kommentaare. Seda välja saab näiteks kasutada vestluse pidamiseks ülesande looja ja täitja vahel. 


## Tegevuse lisamine abivajaja (või Heaoluplaani) vaatest
1. Tegevusi saab lisada ka registreeritud abivajaja kuvalt.
2. Selleks tuleb avada abivajaja vaade ning vajutada päises "Ülesanded" vaadet
3. Avanenud vaatest saab vajutada üleval paremal asuvat "+Lisa" nuppu
![Screenshot]({{ site.baseurl }}/assets/images/RS_task.png)
4. Kuva paremal ääres avaneb samasuguste andmeväljadega vaade nagu kirjeldatud peatükis "Uue tegevuse lisamine Tegevuste nimekirjast"
5. Erinevused:
- Patsiendi väli on peidetud, sest kasutaja juba on patsiendi vaates
- Täitjaid saab valida ainult abivajaja meeskonnaliikmete seast
- Ei saa valida täitmise perioodi ega algusaega. Saab tegevusele määrata ainult tähtaja
- Kuvatakse tegevuse autor (sisseloginud kasutaja uue ülesande loomisel)
6. Peale salvestamist kuvatakse tegevust vastava abivajaja tegevuste nimekirjas.
7. Tegevuse peale vajutades avaneb vaatamise/muutmise kuva samuti ekraani paremalt poolt.
8. Abivajaja vaates loodud ja salvestatud tegevused moodustavad eraldi nimekirja nendest tegevustest, mis on loodud ja salvestatud üldises Tegevuste nimekirjas. 
- Peegeldamine toimib ainult ühtepidi: Kõik tegevused, mis luuakse abivajaja vaates, kuvatakse ka üldises nimekrjas.
- Tegevused, mis luuakse üldises nimekirjas, kuvatakse AINULT üldises nimekirjas (neid abivajaja ülesannete nimekirja tagasi ei peegeldata)
9. Abivajaja Ülesannete vaates on lisavõimalus ühe valikuga vaadata kas KÕIKI tegevusi või ainult aktiivseid tegevusi, linnutades või eemaldades linnukese **Aktiivne** kastist tabeli kohal (vaikimisi linnutatud).
10. Otsingu lahtrist saab otsida tegevuse ID järgi
11. Kõiki tegevusi, mis on lisatud abivajaja külge, saab üle kanda Heaoluplaani.
- Selleks tuleb "Programm" vaatest avada mõni aktiivne Heaoluplaan (vajutades sellele)
- Tuleb päisest valida "Ülesanded" vaade ning tabeli kohalt valida "Kõik tegevused" (vaikimisi valitud "Heaoluplaani tegevused")
- Soovitud tegevus(te)le saab peale vajutada (mitut valides tuleb all hoida SHIFT-klahvi või "command" klahvi (Maci puhul)). 
- Tegevuste valimisel tekib tabeli päisesse võimalus valitud tegevused märkida "Teostatuks" või "Lisada Heaoluplaanile"
-- Kui lisada Heaoluplaanile, siis nüüd näeb neid tegevusi mõlemas "vaates" ning väljatrükil kuvatakse ainult need tegevused, mis on Heaoluplaanile lisatud.
12. Heaoluplaanile saab otse ka tegevusi lisada, avades esmalt aktiivse Heaoluplaani, liikudes Ülesannete vaatesse ning vajutades nupule "+Lisa".
- Need tegevused peegeldatakse tagasi ka "Kõik tegevused" nimekirja ning Tegevuste üldnimekirja

## Tegevuste korraga muutmine
Kui vajutada tegevuste nimekirjas ühe kirje peale ja hoida all Ctrl (Windowsi arvuti) või Command (Mac) klahvi, saab mitme ülesandega korraga teha kahte võimalikku tegevust:

### Tegevuste märkimine "Teostatuks"
Valides üks kuni mitu kirjet, saab nad märkida korraga "Teostatud".
Selline nupp ja võimalus tekib nimekirja kohale, kus näidatakse arvuliselt, mitu kirjet on valitud.
![Screenshot]({{ site.baseurl }}/assets/images/bulk_done.png)
Seda tegevust rakendatakse kõikide tegevuste/kirjete peal, väljaarvatud staatuses "katkestatud". Staatusest "Katkestatud" ei ole võimalik liikuda olekusse "Teostatud".
Kui tegevus juba oli eelnevalt "teostatud", siis temaga ei juhtu midagi, olekut ei kirjutata uue ajatempliga üle.

### Tegevuste tõstmine Heaoluplaanile
Tegevusi saab sisestada tegevuste üldkuvalt, abivajaja "ülesannete" kuvalt ja heaoluplaani "ülesannete" kuvalt.
Kui tegevused on sisestatud abivajaja vaatest, siis saab neid tegevusi hiljem Heaoluplaani olemasolul "tõsta üle".
Selleks tuleb avada Heaoluplaan, liikuda "ülesanded" vaatesse ning tabeli kohalt valida "Kõik tegevused".
![Screenshot]({{ site.baseurl }}/assets/images/all_tasks.png)
Seejärel saab valida üks kuni mitu kirjet, mille peale tekib võimalus "Lisa Heaoluplaanile".
Kui valitud sai vale kirje, tuleb Ctrl/Command all hoida ning uuesti valitud kirjele vajutada, siis see valik tühistatakse. Kõikide valitud kirjete korraga tühistamiseks saab vajutada "X".
Peale lisamist saab liikuda vaatesse "Heaoluplaani tegevused". Nüüd on näha valitud kirjed mõlemas nimekirjas.