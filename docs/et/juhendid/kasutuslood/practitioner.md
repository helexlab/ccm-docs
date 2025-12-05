---
layout: default
title: "Spetsialistid"
parent: Kasutuslood
nav_order: 4
lang: et
permalink: /et/kasutuslood/spetsialist/
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
-- Tuleb kirjeldada **Orgaisatsioon/asutus** (loe rohkem: [Organisatsioonid]({{ '/et/kasutuslood/asutus/' | relative_url }}))
-- **Roll** ehk millises rollis antud töötaja valitud organisatsioonis on
-- **Aadress** - asutuse aadress
-- **Suhtluskanalid** - telefon ja e-mail, läbi mille on võimalik spetsialistiga ühendust võtta. Kui lisatud, kuvatakse abivajajale väljatrükil
-- **Suhtlus** - suhtluskeeled
-- **Kättesaadavus** - E-R võimalik valida, millistel päevadel ja millistel kellaaegadel võib abivajaja antud spetsialistiga ühendust võtta. Näiteks E 09:00-16:00, K 12:00-17:00. Pole kohustuslik, aga kui on lisatud, kuvatakse abivajajale väljatrükil

3. Andmete salvestamiseks tuleb üleval paremal nurgas vajutada nuppu **"Salvesta"**.
4. Juba lisatud andmete/andmeplokkide kustutamiseks tuleb vajutada andmevälja/andmeploki juures olevat "X" nuppu.

---

# Tehniline spekk
## Spetsialisti otsing
Taaskasutatav komponent tervishoiutöötajate (Practitioner) otsimiseks.

**Sisendparameetrid**
- **_text_** – mitte-tühi tekst, mis asetatakse otsinguväljale.
- **_returnUrl_** – lähtekomponendi URL, kuhu kasutaja suunatakse pärast valikut.

Komponent avaneb ülekattena ekraani vasakusse serva ja võtab 300 px laiust.

**Atribuudid**
- **Päis** – tekst *“Practitioner search”*
- **Otsinguväli (Placeholder)** – Material Design stiilis sisestusväli ilma ääristeta.  
  - Initsialiseeritakse laekunud parameetriga **_text_**.  
  - Enter-klahv käivitab otsingu.

- **Tulemuse read** – iga otsingupaketi (search bundle) kirje kohta kuvatakse üks rida.
  - **Ikoon:** ring perekonnanime ja eesnime esitähtedega  
    - Sinine ring → *male*  
    - Roosa ring → *female*  
    - Must ring → sugu puudub / teadmata  

  - **Rida 1**
    - **Nimi:**  
      - Kuva `name.text`.  
      - Kui puudub, siis `name.family`, koma, ja `name.given` loetelu tühikutega eraldatult.
    - **Sugu ikoon:**  
      - Sinine mehe ikoon → *male*  
      - Roosa naise ikoon → *female*  
      - Muul juhul ei kuvata ikooni.

  - **Identifikaatorite read** (väiksem font)
    - Kuva `identifier.value`
    - Tooltip’is kuvada display väärtus:  
      https://fhir.ee/ValueSet/patient-identifier-domain  
      vastavalt `identifier.system` väärtusele

---

**Andmeallikas**

- Andmed tuuakse FHIR Practitioner endpointist:  
  **[FHIR-API-URL]/Practitioner**

- Tagastatakse ainult vajalikud väljad:
GET [base]/Practitioner?_elements=name,identifier,birthDate,gender

**Otsingureeglid**
- Kui **SEARCH_TEXT** algab numbriga → otsing identifikaatori järgi:
GET [base]/Practitioner?identifier="SEARCH_TEXT"

- Kui **SEARCH_TEXT** sisaldab koma → esimene osa on perekonnanimi (täpne vastavus), ülejäänu eesnimi(ed):
GET [base]/Practitioner?family:exact="SEARCH_TEXT_BEFORE_COMMA"&given="SEARCH_TEXT_AFTER_COMMA"

- Kui **SEARCH_TEXT** sisaldab tühikut → esimene sõna on perekonnanimi, ülejäänu eesnimi(ed):
GET [base]/Practitioner?family="SEARCH_TEXT_BEFORE_SPACE"&given="SEARCH_TEXT_AFTER_SPACE"

- Kui **SEARCH_TEXT** ei sisalda koma ega tühikut → filtreeritakse nime järgi:
GET [base]/Practitioner?name="SEARCH_TEXT"

- Kui **SEARCH_TEXT** sisaldab numbrit, kuid mitte alguses → kasutada *_filter* operatsiooni:
GET [base]/Practitioner?_filter=identifier eq "SEARCH_TEXT" or name eq "SEARCH_TEXT"

---

### Näited

| Otsingutekst | Päring |
|--------------|--------|
| 49105180000 | `GET [base]/Practitioner?identifier=49105180000` |
| Doe, John | `GET [base]/Practitioner?family:exact=Doe&given=John` |
| Doe John | `GET [base]/Practitioner?family=Doe&given=John` |
| Doe | `GET [base]/Practitioner?name=Doe` |
| A1 | `GET [base]/Practitioner?_filter=identifier eq "A1" or name eq "A1"` |

---

**Tegevused**

- **Kliku tulemuse real** → tagastatakse valitud kirje:
  - **_fullUrl_**
  - **_display_**

---

## Spetsialisti haldus
Praktiku kaart annab ülevaate tervishoiutöötaja andmetest (rollid, organisatsioonid, kontaktandmed) ning võimaldab neid hallata.

### Andmed
Andmed tuuakse FHIR Practitoner endpointist:  
`[FHIR-API-URL]/Practitioner/$id`

FHIR spetsifikatsioon:  
https://hl7.org/fhir/practitioner.html

Praegune mudel põhineb profiilil:  
**EEBasePractitioner**  
https://fhir.ee/ig/ee-base/1.1.3/site/StructureDefinition-ee-practitioner.html

---

**Atribuudid**
**Identifikaatorid**
**Veerg 1**

- **Identifikaatorid** – massiiv `identifier` elementidest
  - **Olemasolevad elemendid**
    - `identifier.system` kuvatakse sildina.  
      - Kui väärtus leidub väärtustikus:  
        https://dev.termx.org/resources/value-sets/practitioner-identifier-domain/versions/1.0.0/summary  
        → kasutatakse kontseptsiooni *display* nime.  
      - Kui ei, kuvatakse algne `identifier.system` string.
    - `identifier.value` kuvatakse muutmatu tekstina.
    - Kustutamise jaoks lisatakse **„risti“ ikoon**.
  - **Uue identifikaatori lisamine**
    - Valikloend väärtustikust (välja arvatud juba olemasolevad).
    - Uue valiku korral luuakse uus rida sarnaselt olemasolevatele.
      - `identifier.value` → tekstisisestus.

**Nimed**
**Veerg 1**

- **Nimi (HumanName)**
  - **Perekonnanimi (Family)** – tekstiväli → `name.family` (kohustuslik)
  - **Eesnimed (Given)** – iga `name.given` väärtuse jaoks eraldi sisestusväli  
    - Uue praktiku puhul algselt üks väli  
    - Võib lisada mitu eesnime (kohustuslik)
- **Sugu (Gender)** – valik väärtustikust *administrative-gender*
- **Sünnikuupäev (Birthdate)** – kuupäevavalija

**Rollid**

Rollid tuuakse FHIR **PractitionerRole** ressurssidest.  
Olemas on **eelvaate (preview)** ja **redigeerimise (edit)** režiim.

---

### Eelvaade (Preview mode)

- **Organisatsioon:** `organization.text`  
  - Kui puudu → laadida FHIR Organization ressurss ja kuvada organisatsiooni nimi.
- **Roll:** väärtus väärtustikust  
  https://dev.termx.org/resources/value-sets/practitioner-role/versions/1.0.0/summary
- **Telecom**
  - **Mobiiltelefon:** `contact.telecom.value`, kus `system='phone'` ja `use='mobile'`
  - **E-post:** `contact.telecom.value`, kus `system='email'` ja `use='work'`
- **Keeled (Communication):** väärtused väärtustikust  
  https://dev.termx.org/resources/value-sets/languages/versions/6.0.0/summary
- **Kättesaadavus (Availability):** tööpäevad ja tööajad vastavalt FHIR Availability mudelile:  
  https://hl7.org/fhir/R5/metadatatypes.html#Availability

---

### Redigeerimine (Edit mode)

- **Organisatsioon:** automaatotsing FHIR Organization endpointist
- **Roll:** valik väärtustikust  
  https://dev.termx.org/resources/value-sets/practitioner-role/versions/1.0.0/summary
- **Aadress:** tekstiväli → `contact.address.text`
- **Telecom**
  - **Telefon:** tekstisisestus (`system='phone'`, `use='mobile'`)
  - **E-post:** tekstisisestus (`system='email'`, `use='work'`)
- **Keeled (Communication):** mitmikvalik väärtustikust  
  https://dev.termx.org/resources/value-sets/languages/versions/6.0.0/summary  
  - Kui võimalik, kuvatakse esimestena: **et**, **ru**, **en**; teised tähestiku järgi
- **Kättesaadavus (Availability)**
  - Nädalapäevade valikunupud (`availableTime.daysOfWeek`)
  - Algus- ja lõpuaeg (`availableTime.availableStartTime`, `availableTime.availableEndTime`)

