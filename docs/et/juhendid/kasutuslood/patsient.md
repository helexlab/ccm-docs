---
layout: default
title: "Patsiendid"
parent: Kasutuslood
nav_order: 1
lang: et
permalink: /et/kasutuslood/patsient/
---
# Patsiendid
**Patsient** on süsteemi administratiivne üksus (isik), kelle kohta talletatakse kontaktandmed, nimed, identifikaatorid ja muu demograafiline info.  
Patsiendi lisamine ei tähenda veel programmis osalemist.  
Patsiendist saab **abivajaja (Research Subject)** alles siis, kui ta registreeritakse mõnda programmi/raviteekonda.

---

## Patsientide nimekiri
1. Sisestatud patsientide nimekirja näeb menüüst (vasakult ülevalt) **Haldus -> Patsiendid**.
2. Avaneb nimekiri tabeli kujul.
![Screenshot]({{ site.baseurl }}/assets/images/patsiendi_nimekiri.png)
3. Tulemusi kuvatakse lehekülgede kaupa.
4. Vaikimisi kuvatakse kuni 20 kirjet, seda saab muuta, vajutades tabeli allääres olevale numbriväljale.

### Tabeli tulbad
- **Nimi** - Hüperlink kujul "Perekonnanimi, Eesnimi". Peale vajutades avaneb patsiendi andmete muutmise kuva
- **Identifikaator** - identifikaatori tüüp ja sisestatud väärtus
- **Sugu** - valitud sugu, kui see määratakse

### Filtrid
Tabeli kohal paremal üleval nurgas on kuvatud filtri ikoon, millele vajutades avaneb filter võimalustega kitsendada otsingut nimekirjas:
- **Nime järgi** - sisestades eesnime, perenome või osa nimest
- **Soo järgi**
- **ID järgi**, identifikaator peab olema täispikkuses
5. Filtri rakendamiseks tuleb vajutada nupule "Otsi" või ENTER.
6. Kõik rakendatud filtrid saab korraga eemaldada, vajutades **"Tühista kõik"**.
7. Vaikimisi on tabel sorteeritud loomise/muutmise aja järgi. Kõige varasemalt sisestatud kirjed esimesena. Uued lisatakse tabeli lõppu.

---

## Uue patsiendi lisamine

1. Uue patsiendi sisestamiseks süsteemi tuleb vajutada paremal tabeli kohal olevat **"+Lisa"** nuppu
- Nupp on nähtav kasutajatele rolliga "practitioner" (kõige tavalisem "kasutaja")
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

---

# Tehniline spekk
## Patsientide nimekiri
Patsientide nimekiri toimib tsentraliseeritud ja reaalajas uueneva registrina kõigist teenusel olevatest patsientidest, võimaldades spetsialistidel tõhusalt hallata patsientide demograafilisi jm kontaktandmeid.

### Data
Kasutatakse tabelivaadet koos lehekülgede kaupa kuvamisega.

Andmed tuuakse FHIR-teenusest: [FHIR-API-URL]/Patients.
FHIR spekk: [https://hl7.org/fhir/patient.html](https://hl7.org/fhir/patient.html)

### Filtrid

- Identifikaator - tekstisisestus. Kasuta otsinguparameetrit "?identifier=..."
- Nimi - tekstisisestus. Kasuta otsinguparameetrit "?name=..."
- Sugu - valikväli väärtustikust _administrative-gender_. Kasuta otsinguparameetrit "?gender=..."

### Atribuudid

- Identifikaator (25%). Kuvada _idenfier.value_ ja _identifier.system_ tooltipina. Link avab vaate "Patsientide haldamine".
- Nimi (60%). Kuvada _name.text_ kui olemas, muidu kasutada formaati: _name.family_, ", ", nimekiri _name.given_ elementidest, tühikuga eraldatud.
- Sugu (15%). Kuvada _administrative-gender_ väärtuse eestikeelne nimetus. Lisada nime ümber raam. Kasutada taustavärve: sinine code _man_ ja roosa _female_.

---

## Patsiendi otsing

See komponent on taaskasutatav moodul patsientide otsimiseks.

## Sisendparameetrid

- **_text_** – otsinguväljale sisestatud mitte-tühi tekst.
- **_returnUrl_** – komponendi algse vaate URL.
Komponent avaneb ekraani vasakule küljele ülekattena ning võtab laiust 300 px.

**Atribuudid**

- **Päis** – tekst "Patiendi otsing".
- **Otsinguväli** – Material Designi stiilis sisend (ilma ääristeta). Algväärtuseks võetakse sisendparameeter **_text_**. Enter-klahv käivitab otsingu.
- **Tulemuste read** – iga otsingutulemuse (search bundle entry) kohta kuvatakse eraldi rida.
  - **Ikoon:** ring, mis sisaldab perekonna- ja eesnime esitähti.  
    - Sinine ring, kui *gender=male*.  
    - Roosa ring, kui *gender=female*.  
    - Must ring, kui sugu pole määratud.
  - **Rida 1**
    - **Nimi:**  
      - Kasuta `name.text`.  
      - Kui `name.text` puudub, kuvatakse: `name.family`, koma, ning kõigi `name.given` väärtuste loetelu tühikutega eraldatult.
    - **Vanus:** arvutatakse aastad tänase kuupäeva ja `birthDate` erinevusena, kui `birthDate` on täidetud.  
      - Päevi näidatakse, kui *kuud ≤ 3*.  
      - Kuu näidatakse, kui *aastaid < 1*.  
      - Aastaid näidatakse, kui *aastaid > 0*.
    - **Sugu ikoon:**  
      - Sinine mehe ikoon, kui *male*, roosa naise ikoon, kui *female*, muul juhul puudub.
  - **Identifikaatorite read** – iga identifikaator kuvatakse eraldi real väiksema kirjastiiliga.
    - Kuva `identifier.value`.  
    - Tooltip'is näita väärtuseid https://fhir.ee/ValueSet/patient-identifier-domain põhjal `identifier.system` kohta leitavat *display*-väärtust.

---

**Andmeallikas**

- Andmed tuuakse FHIR-i Patient endpointist:  
  **[FHIR-API-URL]/Patient**
- Tagastatakse ainult vajalikud elemendid:
GET [base]/Patient?_elements=name,identifier,birthDate,gender

**Otsingureeglid**

- Kui **SEARCH_TEXT** algab numbriga → otsing identifikaatori järgi:
GET [base]/Patient?identifier="SEARCH_TEXT"

- Kui **SEARCH_TEXT** sisaldab koma → esimene sõna on täpne perekonnanimi, ülejäänu eesnimi(ed):
GET [base]/Patient?family:exact="SEARCH_TEXT_BEFORE_COMMA"&given="SEARCH_TEXT_AFTER_COMMA"

- Kui **SEARCH_TEXT** sisaldab tühikut → esimene sõna on perekonnanimi, teised eesnimi(ed):
GET [base]/Patient?family="SEARCH_TEXT_BEFORE_SPACE"&given="SEARCH_TEXT_AFTER_SPACE"

- Kui **SEARCH_TEXT** ei sisalda koma ega tühikut → filtreeritakse nime järgi:
GET [base]/Patient?name="SEARCH_TEXT"

- Kui **SEARCH_TEXT** sisaldab numbrit, kuid mitte alustuseks → kasutatakse *_filter* operatsiooni:
GET [base]/Patient?_filter=identifier eq "SEARCH_TEXT" or name eq "SEARCH_TEXT"

### Näited

| Otsingutekst | Päring |
|--------------|--------|
| 49105180000 | `GET [base]/Patient?identifier=49105180000` |
| Doe, John | `GET [base]/Patient?family:exact=Doe&given=John` |
| Doe John | `GET [base]/Patient?family=Doe&given=John` |
| Doe | `GET [base]/Patient?name=Doe` |
| A1 | `GET [base]/Patient?_filter=identifier eq "A1" or name eq "A1"` |

---

## Tegevused

- **Tulemuse reale vajutades** → tagastatakse valitud kirje **fullUrl** ja **display** väärtused.
- **Nupp "Lisa uus"** → suunab [MPI.02 Patient Management](page:mpi-02-patient-management) vaatesse, andes kaasa **_redirectUrl_** parameetri.

---

## Patsientide haldamine

Patsiendikaart pakub ülevaadet patsiendi demograafilistest andmetest, kontaktandmetest ning seotud isikutest, võimaldades neid hallata ühes vaates.

### Andmed

Andmed tuuakse FHIR-i teenusest:  `[FHIR-API-URL]/Patient/$id`  
FHIR-i üldspetsifikatsioon: https://hl7.org/fhir/patient.html  
Mudeli aluseks on **[EEBasePatient](https://fhir.ee/ig/ee-base/1.1.3/site/StructureDefinition-ee-patient.html)** profiil.

---

### Atribuudid

#### Identifikaatorid ja seotud isikud

**Veerg 1**
- Identifikaatorid - *Massiiv elementidest `identifier`.*
- Olemasolevad elemendid:
  - **Rida 1:** kasuta `identifier.system` väärtust sildina.  
    - Kui väärtus leidub väärtuste loendis https://fhir.ee/ValueSet/patient-identifier-domain, siis kuva kontseptsiooni nimi; vastasel juhul näita `identifier.system` väärtust.
  - **Rida 2:** kuvatakse `identifier.value` paksus kirjas muutmatu tekstina.
  - **Rida 2 paremal:** kuvatakse “kehtib kuni” (`Patient.identifier.period.end`), kui väärtus on olemas.
  - Lisada ikoon "X" identifikaatori kustutamiseks.

- Uue identifikaatori lisamine:
  - Valik väärtustest https://fhir.ee/ValueSet/patient-identifier-domain (välja arvatud juba kasutusel olevad).
  - Valiku järel lisatakse identifikaatori rida nagu olemasolevate puhul.
  - `identifier.value` on tekstisisestus.
  - `period.end` on kuupäevavalija (pole kohustuslik).

**Nimi**  
- **Perekonnanimi (Family):** tekstiväli → `name.family` (kohustuslik).  
- **Eesnimed (Given):** tekstiväljad iga `name.given` väärtuse kohta.  
  - Uue patsiendi puhul kuvatakse üks sisestusväli.  
  - Võib lisada mitu eesnime.

**Administratiivsed andmed**
- **Sugu (Gender):** valik väärtustest *administrative-gender*.  
- **Sünnikuupäev (Birthday):** kompleksne sisend koos aastate, kuude ja päevade valikuga.

- **Keeled (Languages):** mitmikvalik väärtuste loendist  
  https://dev.termx.org/resources/value-sets/languages/versions/6.0.0/summary 

---

**Veerg 2**
**Kontaktandmed (Telecom)**
- **Olemasolevad elemendid:**
  - Iga kirje kuvatakse eraldi real.
  - Paremale lisatakse „X“, mis võimaldab kirje kustutada.

- **Uue kirje lisamine:**
  - Vali *Telecom system* väärtustest [Contact Point System](http://hl7.org/fhir/ValueSet/contact-point-system)  
    ja *use* väärtustest [Contact Point Use](http://hl7.org/fhir/ValueSet/contact-point-use).
  - **Telefon:** tekstiväli → esimene `telecom` element, kus `system=phone` ja `use=mobile` või `use=home`..  
  - **Muu:** tekstiväli → esimene `telecom` element, kus `system=other` ja `use=...`.  
  - **E-mail:** tekstiväli → esimene `telecom` element, kus `system=email` ja `use=...`.

---

**Aadress**

- Üks sektsioon iga `address` kirje kohta.
- **Riik (Country):** valik väärtustest `http://hl7.org/fhir/ValueSet/iso3166-1-2`.  
  - Seotakse `address.country`.
- **Aadress (text):** tekstiala → `address.text`.  
  - Seotud Eesti aadressiregistriga, kui country=Eesti.

---

### Seotud isik (Related Person)

- **Olemasolevad kirjed:**
  - **Rida 1:** seotud isiku täisnimi, kohustuslik  
  - **Rida 2:** seos/suhe patsiendiga, valik väärtustest https://dev.termx.org/resources/value-sets/related-person/summary  
  - **Rida 3:** kontaktandmed  
  - **Rida 4:** aadress

