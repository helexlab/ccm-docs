---
layout: default
title: "Oleku-mootor"
parent: Tehnilised juhendid
nav_order: 1
lang: et
permalink: /et/juhendid/tehnilised/olekumootor/
---

# Oleku-mootor
Oleku-mootor (state-machine) kirjeldab abivajaja liikumist erinevate sammude vahel Hoolduskoordinatsiooni programmis.  
Igal abivajajal on alati **üks aktiivne olek**, mis sõltub sellest, millised tegevused on tervisejuhi poolt tehtud ning millised nõusolekud on patsiendilt saadud.

---

# Oleku loetelu

CCM rakenduses kasutatakse järgmisi olekuid:

| Olek (EE)                 | TermX kood (EN) | Kirjeldus |
|---------------------------|------------------|-----------|
| **Kandidaat**             | candidate        | Patsient on programmi suunatud ja ootab tervisejuhi esmast kontakti. |
| **Esmasel hindamisel**    | in-screening     | Tervisejuht viib läbi esmase nõustamise (ja InterRAI hindamise). |
| **Teenusele sobiv**       | eligible         | Hindamise/küsimustiku tulemusel sobib patsient teenusele. |
| **Teenusele mittesobiv**  | ineligible       | Hindamise/küsimustiku tulemusel EI sobi patsient teenusele või ei vasta kriteeriumidele. |
| **Teenusel**              | on-study         | Patsiendile on avatud Heaoluplaan ja teenus on aktiivselt käimas. |
| **Teenusel (peatatud)**   | off-study        | Patsient on ajutiselt teenuselt maas (nt paus, peatamine, teenus lõpetatud). |
| **Loobunud**              | withdrawn        | Patsient loobus teenusel osalemisest või võttis nõusoleku tagasi. |

Rakenduses kuvatakse kogu olekute ajalugu kronoloogiliselt (Programi (abivajaja) vaates).

---

# Oleku muutumise tingimused

Oleku muutumisel on kaks peamist mõjutajat:

1. **Tervisejuhi tegevused** (nt protseduuri lisamine, küsimustiku täitmine, plaani avamine)  
2. **Nõusolekud**, mida patsient annab või tagasi võtab

Allpool on kirjeldatud täpne liikumisloogika.

---

## 1. Kandidaat → Esmasel hindamisel (candidate → in-screening)

### Muutuse vallandab:
- Tervisejuht võtab patsiendiga ühendust  
- Avatakse protseduur (nt Esmane nõustamine)

### Tingimused:
- Esimene nõusolek (“Nõusolek nõustamiseks”) olemas

---

## 2. Esmasel hindamisel → Teenusele sobiv (in-screening → eligible)

### Muutuse vallandab:
- InterRAI või muu tervisehindamise täitmine  
- Tervisejuht märgib tulemuseks sobivuse (küsimustikus)

### Tingimused:
- Teine nõusolek: “Nõusolek elektrooniliste terviseandmete jagamiseks” olemas  
- Kliiniliste andmete sisestamine lubatud

---

## 3. Esmasel hindamisel → Teenusele mittesobiv (in-screening → ineligible)

### Muutuse vallandab:
- Hindamise (küsimustiku) tulemus: patsient ei vasta teenuse kriteeriumitele  
- Või Tervisejuht otsustab, et teenust ei alustata

### Tingimused:
- Tervisejuht sisestab põhjuse (vaba tekstina küsimustiku märkustesse)

---

## 4. Teenusele sobiv → Teenusel (eligible → on-study)

### Muutuse vallandab:
- Tervisejuht avab Heaoluplaani

### Tingimused:
- Kolmas nõusolek (“Nõusolek Hoolduskoordinatsiooni teenusel osalemiseks”) on antud  
- Nõusoleku digitaalne dokument võib olla lisatud, kuid ei ole kohustuslik

---

## 5. Teenusel → Teenus peatatud (on-study → off-study)

### Muutuse vallandab:
- Patsient võtab tagasi kolmanda nõusoleku (Heaoluplaani nõusolek)  
- Patsient soovib pausi  
- Tervisejuht paneb teenuse ajutiselt ootele
- Teenus on (edukalt) lõpetatud

### Tingimused:
- Heaoluplaan jääb alles, kuid selle sisestamine peatatakse

Peatatud Heaoluplaani saab taasavada.
---

## 6. Teenusel → Loobunud (on-study → withdrawn)

### Muutuse vallandab:
- Patsient loobub teenusest 
- Või võtab tagasi teise nõusoleku (kliiniliste andmete sisestamine ja jälgimine) 

### Tingimused:
- Teenusega ei saa jätkata enne uut nõusolekut

---

## 7. Loobunud → Teenusel (withdrawn → on-study)

### Muutuse vallandab:
- Patsient taastab nõusoleku  
- Avatakse uus Heaoluplaan või taastatakse peatatud plaan

### Tingimused:
- Vajalikud nõusolekud taas olemas  
- Tervisejuht kinnitab jätkamise

Igast olemasolevast staatusest saab patsient keelduda oma terviseandmete jagamisest ehk igast olekust saab liikuda olekusse "Loobunud" (withdrawn).
Nõusoleku taastamisel jätkatakse sealt, kuhu pooleli jäädi.

---

# Olekute ajalugu

Iga olekumuutus lisatakse Programmi ajajoonele kuupäeva ja kellaajaga.  
Nimekirjas kuvatakse ka:

- asutus  
- asukoht (filiaal)  
- oleku nimetus  
- motivatsioon või kirjeldus (kui lisatud)  

Näide:

```
27.11.2025  Kandidaat
28.11.2025  Esmasel hindamisel
28.11.2025  Teenusele sobiv
28.11.2025  Teenusel
02.12.2025  Loobunud
02.12.2025  Teenusel
```
![Screenshot]({{ site.baseurl }}/assets/images/states.png)
---

# Kokkuvõte

Oleku-mootor määrab, millised funktsioonid ja ekraanid on abivajajale avatud.  
Süsteem tagab, et liikumine toimub ainult lubatud suundades ning alati vastavalt nõusolekutele ja tervisejuhi tegevustele.
