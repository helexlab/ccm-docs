---
layout: default
title: "Abivajajad"
parent: Kasutuslood
nav_order: 5
lang: et
permalink: /et/juhendid/kasutuslood/abivajajad/
---

# Abivajajate nimekiri
1. Suunatud/registreeritud abivajajaid näeb, kui vasakult ülevalt menüüst valida Hoolduskoordinatsioon -> **Abivajajad**.
2. Avaneb abivajajate nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/abivajaja_nimekiri.png)
3. Tulemused on kuvatud lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 tulemust ühel kuval. Seda valikut saab muuta, vajutades tabeli allääres olevale numbriväljale.
5. Tabelis kuvatakse registreeritud abivajajaid valitud tervisejuhtidele (iga tervisejuht näeb endale suunatud abivajajaid) või siis täisnimekirjana audiitorile.

6. Tabeli tulbad:
- **Identifikaator** - Kõigepealt kuvatakse unikaalne süsteemi poolt genereeritud identifikaator hüperlingina
- **Isik** - Kuvatakse patsiendi nimi "Perekonnanimi, Eesnimi"
- **Programm** - teekond, millesse patsient/abivajaja on registreeritud
- **Tervisejuht** - iga programmiga on seotud tervisejuht, kes tuleb patsiendi suunamisel programmi valida (valik tuleb teha, kui programmil on tervisejuhte rohkem kui üks).
- **Staatus** - Patsiendi staatus valitud programmis

7. Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Isiku nime** järgi - väljale vajutades avaneb ekraani vasakul pool patsientide otsingu riba. Otsida saab kas eesnime, perenime järgi või osaliselt (näiteks "kri" kuvab kõik "Kristid, Kristiinad, Kristjanid, jne)
- **Programmi** järgi - kõikide süsteemi sisestatud programmide (või nende kirjelduste, asukohtade, koodide, tervisejuhtide) järgi
- **Tervisejuhi** järgi, kus otsida saab süsteemi sisestatud spetsialistide seast. Võib ka filtreerida abivajad, kellel tervisejuht on määramata, linnutades selleks kasti **"määramata"**
- **Staatuse** järgi
- **Identifikaatori** ehk süsteemi poolt genereeritu unikaalse koodi järgi
- **Kuupäeva** järgi - Võrreldakse valitud kuupäeva selle vastu, millal abivajaja süsteemi ja programmi registreeriti. 

8. Filtreerimiseks tuleb sisestada otsitud väärtus ning vajutada nupule "Otsi" või klaviatuuril ENTER-klahvi
9. Filtri üleval ääres on võimalus kõik filtri valikud korraga tühistada, vajutades nupule **"Tühista kõik"**.
10. Vaikimisi on tabel sorteeritud sisestamise järjekorras. Sorteerimist saab muuta tabeli kõikide tulpade järgi.



# Uue abivajaja suunamine/registreerimine

1. Uue abivajaja sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- See nupp on kuvatud kasutajatele, kellel on "practitioner" ehk kõige tavalisem "kasutaja" roll
2. Avaneb Registreerimise vaade erinevate andmeplokkidega:
![Screenshot]({{ site.baseurl }}/assets/images/RS_reg.png)
- Kusjuures vaikimisi avatakse vasakul ekraani poolel patsiendi otsimise riba. Otsida saab kas eesnime, perenime järgi või osaliselt (näiteks "kri" kuvab kõik "Kristid, Kristiinad, Kristjanid, jne)
-- Otsingu lihtsustamiseks on visuaalselt meesterahvad siniselt, naisterahvad roosalt, teised mustalt kuvatud
-- Kui soovitud patsient on leitud, saab patsiendi "kaardile" vajutades ta välja valida
-- Kui soovitud patsienti ei leitud, saab süsteemi uue patsiendi sisestada, vajutades **+Lisa** nuppu üleval ääres.
- Järgmiseks tuleb valida **Programm**, millesse abivajaja registreerida. Sobiva programmi leiab, kui otsingusõnadesse sisestada asukoht või tervisejuht või aadress vm märksõna
- Peale programmi/raviteekonna valimist, täidetakse automaatselt programmi kaudu ära teenuse asukoht
- Ning "Tervisejuhi" valikuteks kuvatakse ainult vastava programmiga seotud tervisejuht(e)
-- Kui valikuid on rohkem kui 1, tuleb valida 1, kelle töölauale abivajaja suunatakse
- **Registreerimise aeg** on vaikimisi praegune kuupäev ja kellaaeg, mil see vaade avati
- **Nõusolek** on kohutsuslik. Ilma selle kasti linnutamiseta ei saa abivajajat süsteemi registreerida. Peale nõusoleku saamist ja kasti linnutamist võib, aga pole kohustuslik üles laadida nõusoleku digitaalne dokument. Oluline on, et patsient teab, et selle nõusolekuga annab ta õiguse valitud tervisejuhil endaga ühendust võtta.
- **Märkused** - Suunaja võib, aga ei pea sisestama tervisejuhile lisaks kommentaare.

Kui kõik vajalikud väljad on täidetud, saab abivajaja registreerida, vajutades üleval paremal nurgas asuvat **Salvesta** nuppu.

# Uue abivajaja vaade

1. Kui abivajajate nimekirjas vajutada ID peale, juhatatakse kasutaja abivajaja vaatesse
![Screenshot]({{ site.baseurl }}/assets/images/RS_view.png)
2. Vaikimisi avatakse "Programmi" vaade. Erinevaid vaateid saab näha ja valida üleval vasakul ääres.
- Kõige üleval on menüüriba nelja "kuubiku" ikooni all
- Sellele järgneb patsiendi nimi, valus, ID valitud süsteem ja väärtus
- Selle all on erinevad vaated/vahelehed
3. Programmi vaates on erinevad plokid.
4. Esimene plokk kirjeldab üldist informatsiooni valitud programmi kohta ning selle abivajaja praeguse kehtiva oleku kohta antud programmis
- Loe rohkem: [Oleku-mootor](/docs/et/juhendid/tehnilised/olekumootor/)
- Kõige esimene olek peale patsiendi registreerimist programmi, on "Kandidaat"
- Selles olekus on avatud vaated "Patsiendi info", "Programm", "Tegevused/Ülesanded"
5. Manuste plokis saab lisada olemasolevaid digitaalseid faile, näiteks märkamisleht, varasem heaoluplaan, jne.
- Manuste kohta loe rohkem: [Manused](/docs/et/juhendid/kasutuslood/manused/)
6. Meeskonna plokis saab Tervisejuht lisada ja muuta liikmeid
- Loe rohkem: [Meeskond](/docs/et/juhendid/kasutuslood/meeskond/)
6. Järgmiseks eesmärgiks on liikuda edasi järgmisesse "olekusse" ehk Tervisejuht peab võtma patsiendiga ühendust
7. Selleks liigub Tervisejuht "Patsiendi info" vaatesse, et näha patsiendi (või lähedase) telefoninumbrit
- Loe rohkem: [Patsient](/docs/et/juhendid/kasutuslood/patsient/)
8. Patsiendiga ühenduse saamisel lepitakse kokku esmase nõustamise aeg. Selleks Lisab Tervisejuht "Protseduuri"
- Loe rohkem: [Protseduurid](/docs/et/juhendid/kasutuslood/protseduur/)
9. Selleks, et tulevikus eesootav visiit meelest ei läheks, saab Tervisejuht endale luua "Ülesande"
- Loe rohkem: [Tegevused/Ülesanded](/docs/et/juhendid/kasutuslood/tegevused/)
10. Esmase nõustamise ajal täidetakse patsiendiga koos InterRAI küsimustik. Kohandatud InterRAI sisaldab endas mitmeid küsimusi terviseandmete kohta. Nende sisestamiseks on vaja patsiendilt küsida järgmine **Nõusolek**
- Selle nõusoleku lubamise või keeldumise peab Tervisejuht süsteemis manuaalselt lisama
- Loe rohkem: [Nõusolekud](/docs/et/juhendid/tehnilised/nousolekud/)
11. Kui nõustamise protseduur on valmis, saab selle sulgeda
- Loe rohkem: [Protseduurid](/docs/et/juhendid/kasutuslood/protseduur/)
12. InterRAI tulemuse tõlgenduse ja kommentaari lisamise järgselt (ja kui on patsiendilt nõusolek terviseandmete sisestamiseks), saab liikuda edasi Heaoluplaani avamise juurde
- Loe rohkem: [Küsimustikud](/docs/et/juhendid/kasutuslood/kysimustikud/)
- Loe rohkem: [Heaoluplaan](/docs/et/juhendid/kasutuslood/heaoluplaan/)
13. Erinevate nõusolekute ja protsessi sammude peale avanevad süsteemis kasutajale laiemad võimalused
- Näiteks esmase nõustamise protseduuril ning patsiendi nõusolekul saab hakata sisestama kliinilisi andmeid, ravimeid, jms
- Peale patsiendi hindamist ja küsimustiku tõlgendamist sobivaks, saab alustada Heaoluplaani loomisega
- Heaoluplaani ei saa avada, kui pole patsiendilt võetud järgmist nõusolekut