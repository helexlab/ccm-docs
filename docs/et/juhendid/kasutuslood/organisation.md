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

---

# Tehniline spekk
## Organisatsiooni otsing
Taaskasutatav komponent organisatsioonide otsimiseks.

**Sisendparameetrid**
- **_text_** – mitte-tühi tekst, mis sisestatakse otsinguväljale.

---

**UI**
- **Otsinguväli** – lihtne tekstisisestus, mille põhjal tehakse päring FHIR-i teenusele.

---

**Andmeallikas**
- Andmed tuuakse FHIR Organization endpointist:  
  **[FHIR-API-URL]/Organization**
- Tagastatakse ainult vajalikud elemendid:
GET [base]/Organization?_elements=name,identifier

**Otsingureeglid**
- Kui **SEARCH_TEXT** algab numbriga → otsing identifikaatori järgi:
GET [base]/Organization?identifier="SEARCH_TEXT"
- Kui **SEARCH_TEXT** sisaldab tähti → otsing nime järgi:
GET [base]/Organization?name="SEARCH_TEXT"
- Kui **SEARCH_TEXT** sisaldab nii numbreid kui tähti → kasutada *_filter* operatsiooni  
  *(Märkus: mitte kõik serverid ei pruugi seda toetada)*:
GET [base]/Organization?_filter=name eq "SEARCH_TEXT" or identifier eq "SEARCH_TEXT"


---

### Näited

| Otsingutekst | Päring |
|--------------|--------|
| 2405490 | `GET [base]/Organization?identifier=2405490` |
| Maria | `GET [base]/Organization?name=Maria` |

---

**Tegevused**

- **Kliku tulemuse real** → tagastab valitud kirje:
  - `_id_`
  - `_fullUrl_`
  - `_display_`

---

## Organisatsiooni haldus

Organisatsiooni kaart võimaldab hallata organisatsiooni identifikaatoreid, ametlikku nime, lühinime ning staatust.

**Andmed**

Andmed tuuakse FHIR-i Organization resource’i põhjal (täpne endpoint lisatakse süsteemi konfiguratsioonis).

**Atribuudid**
**Identifikaatorid**

*Massiiv `identifier` elementidest.*

- **Olemasolevad elemendid**
  - **Rida 1:** kuvatakse `identifier.system` nimi sildina.  
    - Kui väärtus leidub väärtustikus:  
      https://fhir.ee/ValueSet/organization-identifier-domain  
      siis kasutatakse väärtustiku *display* nime.  
    - Kui ei leidu, kuvatakse algne `identifier.system` väärtus.
  - **Rida 2:** kuvatakse `identifier.value` paksus kirjas muutmatu tekstina.
  - **Rida 2 paremal:** kuvatakse „kehtib kuni“ (`organization.identifier.period.end`), kui väärtus on olemas.
  - Lisada kustutamise ikoon **"rist"** identifikaatori eemaldamiseks.

- **Uue identifikaatori lisamine**
  - Valikloend väärtustikust:  
    https://fhir.ee/ValueSet/organization-identifier-domain  
    (kuvatakse ainult need, mida organisatsioonil veel ei ole).
  - Väärtustiku *concept name* kasutatakse sildina.
  - Kui kasutaja valib uue identifikaatori → lisatakse uus rida nagu olemasolevate puhul.
    - `identifier.value` – tekstisisestus
    - `identifier.period.end` – valik kuupäevavalijaga (pole kohustuslik)

---

**Nimi**
- **Täisnimi (Name)** – organisatsiooni ametlik nimi. Tekstisisestus.

**Alias**
- **Teine nimi / lühinimi (Alias)** – valikuline lühivorm organisatsiooni nimest.  
  - Võib kasutada kuvamisel või otsingus.

**Staatus**
- **Aktiivne / mitteaktiivne** – märkeruut (checkbox).  
  - Kui märgitud → organisatsioon on *active*.  
  - Kui märkimata → organisatsioon on *inactive*.


