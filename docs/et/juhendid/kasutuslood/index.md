---
layout: default
title: "Kasutuslood"
nav_order: 2
lang: et
has_children: true
permalink: /et/kasutuslood/
---
# Kasutuslood

Selle peatüki all on kirjeldatud süsteemsed kasutuslood ja -vood, põhifunktsionaalsused.

# Kasutuslugu 1
**Patsiendi suunamine teenusele, kahe nõustamise tegemine, lõpetamine.**
Teeme läbi olukorra, kus InterRAI küsimustikuga ega Heaoluplaani teenusega ei jätkata, vaid piirdutakse ainult Nõustamis(te)ga.
1. Sisene süsteemi kasutajaga, kellel on vähemalt spetsialisti (practitioner) roll.
2. Liigu lehele "Abivajajad"
3. Vajuta nupule "+Lisa"
4. Otsi/lisa patsient, vali programm koos vastutava tervisejuhiga (kes on samuti süsteemi kasutaja, spetsialisti rolliga), märgi, et on olemas Nõusolek, Salvesta.
5. Logi sisse Tervisejuhiga, kelle töölauale abivajaja registreeriti, ava vaade "Abivajajad" või "Minu patsiendid"
6. Ava Programmi kuva, kus on näha vahelehti "Patsiendi info", "Programm" ja "Ülesanded".
7. Programmi vaates on andmeplokid: "Abivajaja staatus", "Meeskond", "Nõusolekud", "Protseduurid", "Küsimustikud", "Manused".
8. Tervisejuhina ma võtan patsiendiga ühendust, avades "Patsiendi info" ning leides patsiendi kontaktandmed. Peale ühenduse saamist lepitakse kokku Esmase nõustamise aeg. Selleks loob tervisejuht nüüd Protseduuri.
9. Protseduuri loomiseks vajuta protseduuri plokis "+Lisa" ning täida väljad (märgi protseduur toimuma näiteks homseks) ja staatuseks vali "ettevalmistamisel", tulemiks "osaline" (sest pole veel toimunud).
10. Peale salvestamist vajuta tekkinud protseduurile. Kujutame ette, et on saabunud aeg ning protseduur saab tehtud. Vali korrektne staatus ja tulem ning salvesta.
11. Nüüd selgub, et on vaja järgmist protseduuri teise spetsialistiga. Selleks loo uus protseduur ning määra Teostajaks keegi teine (kellel on süsteemis kasutaja ja vähemalt spetsialisti roll).
12. Selleks, et teine spetsialist pääseks abivajaja kuvale ligi, tuleb ta lisada programmi meeskonda. Tervisejuhina vajuta Meeskonna plokis "+Lisa" -> spetsialist. Täida väljad ja salvesta. Pole tähtis, kas valida rolliks "meeskonnaliige" või "kaastöötaja". Protseduuride lisamise õigus on mõlemal.
13. Kui spetsialist on meeskonda lisatud, saab spetsialist sisse logida ning näeb abivajajate nimekirjas antud patsienti. Avades abivajaja kuva, saab spetsialist minna endale suunatud protseduuri täitma ja kommenteerima ja muutma.
14. Kui on vaja veel erinevaid nõustamisi läbi viia, saab seda teha samamoodi. Kui mõni nõustamine või protseduur nõuab kliiniliste andmete sisestamist, tuleb patsiendilt võtta nõusolek kliiniliste andmete sisestamiseks. Kui see on antud, saab Tervisejuht märkida "Nõusolek elektrooniliste andmete jagamiseks" = antud (seda saab teha Nõusolekute plokis, vajutades "..." peale)

# Kasutuslugu 2
**Patsiendiga on vaja jätkata, läbi viia InterRAI küsimustik, panna tulemused kirja.**
1. Kasutuslugu 1 tuleb läbida nii palju, et vähemalt üks protseduur on vaja ära lõpetada ning InterRAI jaoks on vaja saada patsiendilt Nõusolek elektrooniliste andmete jagamiseks.
2. Kui need on tehtud, avanevad päises lisavaated: Ravimid, Kliinilised andmed, Eesmärgid, Juhised.
3. InterRAI küsimustik ei ole digitaliseeritud, kuigi erinevates vaadetes on võimalik mitmeid tulemusi kirja panna (diagnoosid, ravimid, jne). Kui küsimustik on täidetud ja tulemus teada, peab protsessis edasi liikumiseks vajutama Programmi vaates "+Lisa" küsimustik.
4. Avaneb lihtne vaade vabatekstilise "Kirjelduse" lahtriga ning tulemuse valikuga:
- Sobib osalemiseks programmis
- Ei sobi osalemiseks programmis
5. Olenevalt tulemusest muutub protsess. Kui patsient ei sobi Hoolduskoordinatsiooni teenust saama, siis edasi ei liiguta. Abivajaja olek muutub "mittesobivaks".
6. Kui "Sobib osalemiseks programmis", siis muutub abivajaja oleks "sobivaks" ning järgmise sammuna saab Tervisejuht avada Heaoluplaani.

# Kasutuslugu 3
**Heaoluplaani koostamine ja sulgemine**
1. Peale Kasutuslugu 2, kui InterRAI tulemusena selgub, et Hoolduskoordinatsiooniga peaks jätkama, saab Tervisejuht avada Heaoluplaani, vajutades "+Lisa" Heaoluplaani plokis.
2. Tervisejuht täidab väljad ja salvestab. Patsiendilt võetakse kolmas nõusolek kinnitamaks, et ta teab ja nõustub teenust saama.
3. Heaoluplaani salvestamisel luuakse Aktiivne Heaoluplaan. Selles vaates on sarnased vahelehed nagu abivajaja vaates (kliinilised andmed, ravimid, eesmärgid..), kuid paistavad esialgu tühjad. Kui liikuda võimaluste "heaoluplaani ravimid" ja "kõik ravimid" vahel, tulevad varasemalt sisestatud andmed nähtavale. Varasemalt abivajaja vaates sisestatud andmeid saab Heaoluplaani üle tõsta.
4. Heaoluplaani võib lisada ka uued andmed. Kõik, mida Heaoluplaani "vahelehtedele" lisatakse ja mis on välja trükkimiseks mõeldud, saab vaadata vahelehelt "Väljatrükk".
5. Heaoluplaani avades saab Tervisejuht komplekteerida meeskonna. Meeskonnaliikmetele saab anda kas vaatamise (meeskonnaliige) või andmete muutmise õiguse (kaastöötaja). Tervisejuht saab meeskonnaliikmeid alati muuta, lisada, eemaldada ja õigusi vahetada. Tervisejuht saab vahetada ka Tervisejuhti. Kõigepealt peaks ta end lisama laiendatud õigustega meeskonnaliikmeks ehk "kaastöötajaks" ning seejärel valima uue tervisejuhi ja enda sellelt positsioonilt tühistama.
6. Heaoluplaani tegevuskava saab luua vahelehelt "Ülesanded". Heaoluplaani saab üle tuua ka ülesandeid/tegevusi, mis oli lisatud abivajaja vaates. Kõiki Heaoluplaani aktiivseid tegevusi kuvatakse hiljem väljatrükil.
7. Heaoluplaani võib sulgeda kolmel põhjusel:
- Eesmärgid saavad saavutatud ja Heaoluplaani saab märkida "Lõpetatuks"
- Heaoluplaan lõpetatakse mingil muul põhjusel ja saab märkida "Suletuks"
- Patsient võtab tagasi nõusoleku terviseandmete vaatamiseks ja sisestamiseks. Selle peale peab Tervisejuht sulgema ka Heaoluplaani, sest Heaoluplaani komponendid sisaldavad terviseandmeid, millele enam ligi ei pääse.
8. Kui patsient annab uuesti nõusoleku või soovib jätkata, saab suletud/lõpetatud Heaoluplaani taasavada.

# Vastavus arendusnõuetele (Lisa 2 järgi)

## NT-1
**Vastutav Tervisejuht dokumenteerib nõustamist**
Loodud süsteemis saab Nõustamise tegevust dokumenteerida Protseduuri(de)na.
- Loe rohkem: [Protseduurid]({{ '/et/kasutuslood/protseduur/' | relative_url }})
Protseduuri meeldetuletuseks (kui see on tulevikus) võib Tervisejuht endale luua tegevuse/ülesande, mis värvub tähtaja saabumisel punaseks.
- Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})
Registreeritud abivajaja juurde saab alati juurde lisada ka manuseid.
- Loe rohkem: [Manused]({{ '/et/kasutuslood/manused/' | relative_url }})
Abivajaja registreerimisel programmi on kirjeldatud aeg, mil suunati ning suunaja/märkaja info.
- Loe rohkem: [Abivajaja]({{ '/et/kasutuslood/abivajajad/' | relative_url }})

## NT-2
**Tervisejuht hindab abivajajat koos patsiendiga (InterRAI)**
Hindamine teostatakse Nõustamise Protseduuri käigus. Kui sel ajal täidetakse ka (paberkujul) InterRAI küsimustik, saab selle tulemusi ja kommentaare üles märkida Küsimustiku plokki.
- Loe rohkem: [Küsimustikud]({{ '/et/kasutuslood/kysimustikud/' | relative_url }})
Kuna InterRAI sisaldab palju delikaatseid terviseandmeid, tuleb Nõustamise käigus patsiendilt küsida nõusolekut kliiniliste andmete sisestamiseks.
- Loe rohkem: [Nõusolekud]({{ '/et/tehnilised/nousolekud/' | relative_url }})
Nõusoleku olemasolul saab osasid andmeid, nt diagnoose, allergiaid, ravimeid juba otse süsteemi sisestada.

## NT-3 ja NT-7
**Nõusolekud**
Süsteemis on kasutusel 3 nõusolekut:
- Nõusolek Tervisejuhile suunamiseks ja ühenduse võtmiseks (märkamisleht)
- Nõusolek kliiniliste andmete sisestamiseks ja vaatamiseks
- Nõusolek Hoolduskoordinatsiooni teenuseks ja Heaoluplaani avamiseks
Nõusolekuid saab patsient igal hetkel tagasi võtta (ja uuesti anda).
- Loe rohkem: [Nõusolekud]({{ '/et/tehnilised/nousolekud/' | relative_url }})
Nõusoleku võtmise meeldetuletuseks võib spetsialist endale teha tegevuse/ülesande.
- Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})

## NT-4 ja NT-5
**Heaoluplaani ja meeskonna loomine**
Heaoluplaani loomise eelduseks on läbitud nõustamine, olemasolevad nõusolekud patsiendilt, InterRAI hindamine tulemusega "sobib teenuse saamiseks".
Kui kõik eeldused on täidetud, saab Tervisejuht avada Heaoluplaani ning selle järel moodustada meeskonna, kusjuures meeskonnaliikmeteks saavad olla ka patsient ise ja tema lähedased.
Loe rohkem: [Heaoluplaan]({{ '/et/kasutuslood/heaoluplaan/' | relative_url }})
Meeskonnaliikmetele (ja meeskonnaliikmed) saab teha erinevaid tegevusi/ülesandeid ehk moodustada tegevuskava.
Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})
Meeskonnaliikmeteks lisatud spetsialistid saavad Heaoluplaani komponentidele ja abivajajale ligipääsu.

## NT-6
**Heaoluplaani saab välja printida**
Iga Heaoluplaani juurde tekib võimalus näha printimise eelvaadet valitud keeles ning seejärel dokument välja printida koos kokkulepitud ja olemasolevate andmeväljadega.
- Loe rohkem: [Väljatrükk]({{ '/et/kasutuslood/printout/' | relative_url }})

## NT-8
**Tervisejuht näeb tervet tegevuskava ja saab piirata/laiendada meeskonnaliikmete õigusi**
Tervisejuhil on abivajaja ja Heaoluplaani vaates kõige suuremad õigused. Tema on isik, kellele abivajaja "töösse" suunatakse, kui ta on programmiga seotud ja tema on ainuke, kes saab Heaoluplaani avada ning meeskonda moodustada.
Meeskonna moodustamisel saab Tervisejuht valida, kas meeskonnaliikmel on ainult andmete vaatamise õigus või laiendatud õigus, kus saab andmeid muuta/lisada. Neid saab Tervisejuht igal hetkel muuta.
Kõik meeskonnaliikmed saavad teha endale ja teistele tegevusi/ülesandeid, määrata täitjaks üks kuni mitu spetsialisti, määrata staatusi ja prioriteete.
Tegevuse tähtaja saabudes (ja ületamisel) värvitakse tähtaeg punaseks.
Iga tegevuse sees saab valida tegevuse tüübi, lisada kirjelduse ja kommentaare (toimib nagu vestlusaken spetsialistide vahel) ning näeb kõiki varasemalt tehtud muudatusi.
Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})
Loe rohkem: [Meeskond]({{ '/et/kasutuslood/meeskond/' | relative_url }})

## NT-9 ja NT-11
**Tervisejuht hindab Heaoluplaani täitmist**
Kõige lihtsam viis erinevaid tegevusi teha ja hinnanguid anda, on koostada endale (või mõnele teisele spetsialistile) vastavasisuline tegevus/ülesanne.
Meeskonnatööks, koosolekuteks, teavitusteks, jm tegevusteks saab samamoodi kasutada tegevuste/ülesannete loomist. Tegevusi saab lisada Heaoluplaani sees ja selle väliselt.
Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})

## NT-10
**Tervisejuht saab heaoluplaani muuta ja kooskõlastada**
AKtiivset heaoluplaani saab alati muuta ja täiendada. Spetsiaalse seisu saab välja võtta kõige lihtsamalt läbi manuste, sest kindlatel hetkedel peale valideerimisi prinditakse Heaoluplaan patsiendile välja. Siis saab selle sama versiooni Heaoluplaani manuseks üles laadida.
Loe rohkem: [Manused]({{ '/et/kasutuslood/manused/' | relative_url }})
Kooskõlastusringideks ja valideerimisteks jm saab luua tegevusi.
Loe rohkem: [Tegevused]({{ '/et/kasutuslood/tegevused/' | relative_url }})

## NT-12 ja NT-14
**Heaoluplaani lõpetamine**
Aktiivset Heaoluplaani saab Tervisejuht lõpetada ja sulgeda. Sulgeda tuleb ka juhul, kui patsient on võtnud tagasi nõusoleku kliiniliste andmete sisestamiseks ja vaatamiseks.
Suletud/lõpetatud Heaoluplaani saab vajadusel taasavada.
Varasemalt suletud ja lõpetatud Heaoluplaane saab abivajaja vaatest näha, väljaarvatud kliinilisi andmeid, kui patsient ei ole seda nõusolekut (tagasi) andnud.
- Loe rohkem: [Heaoluplaan]({{ '/et/kasutuslood/heaoluplaan/' | relative_url }})

## NT-13
**Teenuse üleandmine**
Tervisejuht saab Tervisejuhti vajadusel vahetada igas protsessi sammus.
Nii abivajaja kui aktiivse Heaoluplaani vaates peab Tervisejuht end kõigepealt lisama täiendatud õigustega meeskonnaliikmeks (kaastöötaja). Seejärel lisama uue Tervisejuhi ning siis eemaldama end Tervisejuhi positsioonilt.
Tervisejuhti saab vahetada ka uue Heaoluplaani avamisel. Vaikimisi on täidetud hetkel sisseloginud Tervisejuhi andmed sinna rolli, aga seda saab soovi korral muuta.
- Loe rohkem: [Heaoluplaan]({{ '/et/kasutuslood/heaoluplaan/' | relative_url }})
- Loe rohkem: [Meeskond]({{ '/et/kasutuslood/meeskond/' | relative_url }})