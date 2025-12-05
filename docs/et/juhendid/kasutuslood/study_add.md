---
layout: default
title: "Programm"
parent: Kasutuslood
nav_order: 2
lang: et
permalink: /et/kasutuslood/programm/
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

---

# Tehniline spekk
Nimekiri toetatud teadusuuringutest, programmidest või raviteekondadest.

**Atribuudid**
- Kood
- Nimi
- Staatus (kuvatakse väärtused *https://hl7.org/fhir/valueset-publication-status.html*)

**Filtrid**
- Kood - tekstisisestus
- Nimi - tekstisisestus
- Praktiseerija/spetsialist - avab otsingu overlay komponendi
- Staatus - valik väärtustest *publication-status*

## BE-teenus
Andmebaasi tabel - `ccm.research_study`

**Sisemine API** `/ccm/research-studies`
- Kirjeldus - Loetelu toetatud teadusuuringutest
- Meetodid: `GET`
- Otsinguparameetrid:
  - `code`
  - `name`

`/ccm/research-studies/$id`
- Kirjeldus - uuringu detailvaade
- Meetodid - `GET`

**FHIR API**
FHIR-fassaad vastavalt spetsifikatsioonile:  
https://hl7.org/fhir/researchstudy.html  
kasutamiseks teekonnal `/int/research-studies*`.

### `/fhir/r5/ResearchStudy`
- **Kirjeldus:** Loetelu toetatud teadusuuringutest
- **Meetodid:** `GET`
- **Otsinguparameetrid:**
  - `identifier` – kaardistatud väljale **code**
  - `name` – kaardistatud väljale **name** (ükskõik mis keeles)

### `/fhir/r5/ResearchStudy/$id`
- **Kirjeldus:** Uuringu detailvaade
- **Meetodid:** `GET`

---

## Programm
Programmi vaates hallatakse teadusuuringuid, registreid või akadeemilisi programme.

**Atribuudid**
**Üldandmed**
- **Kood** - tekstisisestus. Peab olema unikaalne.
- **Nimetus** – mitmekeelne sisestus; vaikimisi kuvatakse ja valitakse esimesena **eesti keel**.
- **Kirjeldus** – tekstisisestus, kuhu saab lisada detailsema asukoha, tingimused või programmi parameetrid.
- **Teenuse asukoht (Service location)** – automaatotsing väärtustikust  
  https://dev.termx.org/resources/value-sets/ccm-service-location/summary
- **Numbriseeria (Sequence)** – valikloend.  
  Praegused valikud:
  - *CCM default sequence* - eelvalitud ja peidetud UIst
  - *Task number*
  - *Care Plan identifier sequence*

- **Staatus** – valikloend väärtustikust:  
  https://dev.termx.org/resources/value-sets/publication-status/summary

---

### Osapooled (Parties)

- **Programmi juht (Study chair)**
  - **Isik (Party)** – valitakse overlay-komponendiga  
    [Practitioner search](page:mdm-01-3-practitoner-search)

- **Kaastöötaja (Collaborator)**
  - **Isik (Party)** – sama otsingukomponent praktikute leidmiseks

- **Lisa roll (Add role)** – valik väärtustikust  
  https://dev.termx.org/resources/value-sets/research-study-party-role/versions/5.0.0/summary

---

**Tegevused**

- Kui viimase rolli/isiku väli on täidetud, lisatakse automaatselt uus tühi *Collaborator* (ja *Study chair*) sisestusväli.
- Nupp **Save** suunab komponendile  
  [RS.01.2 Research studies](page:rs-01-1-research-studies)

---

### BE
**Sisemised REST API teenused**
`POST /cmm/research-studies`
- **Party** – peab sisaldama absoluutset viidet praktikule (absolute reference).

---

**Andmebaas**

- **Tabel:** `cmm.research_subject`
- **Tabel:** `cmm.research_subject_party`
  - Programmi juht → `role = study-chair`
  - Kaastöötaja → `role = collaborator`
  - `period.low` → määratakse *current timestamptz*
  - Kui kasutaja klõpsab kustutusikoonil **X** → seada `period.high` väärtuseks *current timestamptz*

**Näide (sisemine mudel)**

```json
{
  "code": "123",
  "name": {"et": "Hoolduskoordinatsiooni programm (Ahtme)"},
  "location": [{
    "system": "https://fhir.ee/CodeSystem/ads-adr-id",
    "code": "2103553",
    "display": "Harju maakond, Tallinn"
  }],
  "sequence": "cmm-number",
  "status": "active",
  "party": [{
    "role": "study-chair",
    "name": "Linn, Helen",
    "reference": "https://your.fhir.server/fhir/Practitoner/456",
    "period": {
      "start": "2025-08-01"
    }
  }]
}

---

**FHIR API**
POST /fhir/r5/ResearchStudy
Vastab spetsifikatsioonile: https://hl7.org/fhir/researchstudy.html
- Teenuse asukoha puhul tuleb kasutada laiendit: https://fhir.ee/base/StructureDefinition/ee-ads-adr-id

{
  "resourceType": "ResearchStudy",
  "status": "active",
  "identifier": [
    {
      "system": "https://helex.org/sid/research-study",
      "value": "123"
    }
  ],
  "language": "et",
  "title": "Hoolduskoordinatsiooni programm (Ahtme)",
  "associatedParty": [{
    "role": {
      "coding": [{
        "system": "http://hl7.org/fhir/research-study-party-role",
        "code": "study-chair",
        "display": "Study chair"
      }]
    },
    "name": "Linn, Helen",
    "party": {
      "reference": "https://your.fhir.server/fhir/Practitoner/456",
      "type": "Practitioner"
    },
    "period": {
      "start": "2025-08-01"
    }
  }],
  "extension": [
    {
      "url": "https://fhir.ee/base/StructureDefinition/ee-ads-adr-id",
      "valueCoding": {
        "system": "https://fhir.ee/CodeSystem/ads-adr-id",
        "code": "2280361",
        "display": "Tallinn"
      }
    }
  ]
}
