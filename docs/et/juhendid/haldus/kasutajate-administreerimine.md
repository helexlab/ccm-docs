---
layout: default
title: "Kasutajate administreerimine"
parent: Haldusjuhendid
nav_order: 3
lang: et
permalink: /et/haldus/kasutajate-administreerimine/
---

# Kasutajate administreerimine

Selles juhendis selgitatakse, kuidas hallata CCM kasutajaid Keycloaki kaudu ning mis roll on GovSSO Mockil.  
Kasutajahaldust teevad ainult eraldi määratud CCM administraatorid. Neid ei pea olema palju.

---

## 1. CCM administraatori määramine

CCM administraator ei ole Keycloaki täisadmin, vaid kasutaja, kellele antakse kasutajahalduri õigused.  
Administraatori õigused määrab **SSO serveri administraator**.

Administraatori rollid tuleb lisada **realm-management** kliendi alt:

- `view-users`
- `query-groups`
- `manage-users`

### Rollide lisamine
1. Ava kasutaja Keycloakis  
2. Vali **Role mappings**  
3. Klõpsa **Assign role → Client roles**  
4. Vali klient **realm-management**  
5. Lisa rollid  

Pärast seda saab kasutaja hallata CCM kasutajaid (ainult olemasolevaid).
![Screenshot]({{ site.baseurl }}/assets/images/keycloak.png)

---

## 2. Admin-liidesesse sisselogimine

### Testkeskkond
Keycloak admin:  
`https://testsso.helex.dev/admin/ccm/console`

Testimisel kasutatakse **GovSSO Mock** identiteete.
- Loe rohkem: [Õigused]({{ '/et/haldus/oigused/' | relative_url }})

### Tootmiskeskkond
Keycloak admin:  
`https://ccm.askend.com/sso/admin/ccm/console`

---

## 3. Kasutajate loomine vs haldamine

### Väga oluline:
**CCM administraator Keycloakis EI SAA luua uusi GovSSO Mocki kasutajaid.**

GovSSO Mockis olevad identiteedid (nt EE38001085718, 49105186017 jne) on  
**SSO taseme identiteedid**, mida Keycloak ei loo ega halda.

Keycloak saab töötada ainult nendega, kes:
- on GovSSO Mockis juba olemas, ja  
- on vähemalt korra autentinud → Keycloak loob neile kasutaja kirje.

**Seega: CCM admin saab hallata õigusi, mitte uusi kasutajaid juurde luua.**

---

## 4. Kuidas administraator saab kasutajaid hallata?

Kasutajatele õigusi antakse **gruppide kaudu**. Grupis määratud rollid määravad ligipääsud.

### Variant A: kasutaja → grupp
1. Ava **Users**  
2. Vali kasutaja  
3. Ava **Groups**  
4. Lisa kasutaja vajalikku gruppi

### Variant B: grupp → Kasutaja
1. Ava **Groups**  
2. Vali grupp  
3. Ava **Members**  
4. Lisa grupile kasutajaid

Mõlemad viisid annavad sama tulemuse.

---

## 5. Lühikokkuvõte

- CCM administraator määratakse SSO admini poolt.  
- Admin logib sisse Keycloaki adminliidesesse (test/prod URL-id).  
- Adminile antakse rollid: `view-users`, `query-groups`, `manage-users`.  
- **Admin saab hallata ainult olemasolevaid kasutajaid**, mitte luua GovSSO Mocki uusi identiteete.  
- Kasutajate õigusi hallatakse gruppide kaudu.  

