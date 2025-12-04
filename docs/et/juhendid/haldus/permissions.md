---
layout: default
title: "Õigused"
parent: Haldusjuhendid
nav_order: 2
lang: et
permalink: /et/haldus/oigused/
---

# Funktsionaalsusd ja õiguste maatriks

## Funktsionaalsused ja rollid

Teise ja kolmanda tulba vahel rakendub "VÕI", mis tähendab, et näiteks manuste vaatamiseks peab olema kas manuse lisaja/autor VÕI Heaoluplaani meeskonnaliige.

| Funktsionaalsus                                        | Kasutaja roll                 | Ressursi atribuudid   | HeaoluPlaani roll (kui rakendub) |
|--------------------------------------------------------|-------------------------------|------------------------|-------------------------------|
| Lisa uus patsient                                      | practitioner                  | N/A                    | N/A                           |
| Vaata patsiendi andmeid                                | practitioner, admin, auditor  | N/A                    | N/A                           |
| Muuda patsiendi andmeid                                | practitioner                  | N/A                    | N/A                           |
| Vaata enda loodud/sisestatud tegevusi                | practitioner                  | author, assignee       | N/A                           |
| Vaata sulle määratud tegevusi                        | practitioner                  | author, assignee       | N/A                           |
| Vaata kõiki tegevusi                                 | admin, auditor                | N/A                    | N/A                           |
| Lisa tegevusi                                        | practitioner                  | N/A                    | N/A                           |
| Muuda tegevusi                                       | practitioner, admin           | N/A                    | N/A                           |
| Vaata spetsialistide nimekirja                            | practitioner, admin, auditor  | N/A                    | N/A                           |
| Halda spetsialiste                                       | admin                         | N/A                    | N/A                           |
| Vaata organisatsioone                                  | practitioner, admin, auditor  | N/A                    | N/A                           |
| Halda organisatsioone                                  | admin                         | N/A                    | N/A                           |
| Vaata koodisüsteeme ja väärtuste komplekte             | practitioner, admin, auditor  | N/A                    | N/A                           |
| Vaata programme                                        | practitioner, admin, auditor  | N/A                    | N/A                           |
| Halda programme                                        | admin                         | N/A                    | N/A                           |
| Lisa/eemalda programmidega seotud kasutajaid/liikmeid | admin                        | N/A                    | N/A                           |
| Lisa abivajaja                                    | practitioner                  | N/A                    | N/A                           |
| Vaata aktiivset abivajajat                        | practitioner                  | N/A                    | member                        |
| Vaata aktiivset abivajajat                        | auditor                       | N/A                    | N/A                           |
| Vaata manuseid                                          | practitioner                  | author                 | member                        |
| Vaata manuseid                                          | auditor                      | N/A                    | N/A                           |
| Lisa/eemalda manuseid                                   | practitioner                  | author                 | collaborator                  |
| Vaata küsimustikke                                      | practitioner                  | author                 | member                        |
| Vaata küsimustikke                                      | auditor                      | N/A                    | N/A                           |
| Lisa/muuda küsimustikke                                 | practitioner                  | practitioner           | collaborator                  |
| Vaata protseduure                                      | practitioner                  | performer              | member                        |
| Vaata protseduure                                      | auditor                      | N/A                    | N/A                           |
| Lisa protseduure                                       | practitioner                  | N/A                    | N/A                           |
| Muuda protseduure                                      | practitioner                  | performer              | collaborator                  |
| Vaata ravimeid                                         | practitioner, auditor         | N/A                    | member                        |
| Lisa / muuda / kustuta ravimeid                        | practitioner                  | N/A                    | collaborator                  |
| Vaata kliinilist kokkuvõtet                            | practitioner, auditor         | N/A                    | member                        |
| Lisa / muuda / kustuta kliinilist kokkuvõtet           | practitioner                  | N/A                    | collaborator                  |
| Vaata eesmärke                                         | practitioner, auditor         | N/A                    | member                        |
| Lisa / muuda / kustuta eesmärke                        | practitioner                  | N/A                    | collaborator                  |
| Vaata juhiseid                                         | practitioner, auditor         | N/A                    | member                        |
| Lisa / muuda / kustuta juhiseid                        | practitioner                  | N/A                    | collaborator                  |
| Vaata väljatrükki                            | practitioner, auditor         | N/A                    | member                        |
| Ava heaoluplaan                                       | practitioner                  | N/A                    | care-manager                  |
| Vaata endaga seotud heaoluplaani                        | practitioner, auditor         | N/A                    | member                        |
| Muuda endaga seotud heaoluplaani                        | practitioner                  | N/A                    | collaborator                  |
| Vaata kõiki heaoluplaane                              | practitioner, auditor         | N/A                    | member                        |
| Vaata heaoluplaani meeskonna liikmeid                        | practitioner, auditor         | N/A                    | member                        |
| Halda heaoluplaani meeskonna liikmeid                        | practitioner                  | N/A                    | care-manager                  |
| Halda meeskonnaliikmete õigusi                         | practitioner                  | N/A                    | care-manager                  |
| Sulge heaoluplaan                                      | practitioner                  | N/A                    | care-manager                  |
| Vaata suletud heaoluplaane                            | practitioner                  | N/A                    | care-manager                  |
| Vaata suletud heaoluplaane                            | auditor                      | N/A                    | N/A                           |
| Vaata nõusolekuid                                      | practitioner, auditor         | N/A                    | member                        |
| Halda nõusolekuid                                      | practitioner                  | N/A                    | care-manager                  |


## Rollide koondtabel

| Roll            | Kirjeldus | Peamised õigused | Ligipääsu ulatus |
|-----------------|-----------|------------------|------------------|
| **Practitioner** (spetsialist) | Süsteemi ligipääsuga ja kasutajaga tervishoiutöötaja, kes täidab hoolduskoordinatsiooniga seotud tööülesandeid. | Patsientide vaatamine ja muutmine, isikuga seotud tegevuste haldamine, küsimustike ja protseduuride lisamine, raviplaanide loomine ja muutmine, kliiniliste kirjete lisamine, juhised, eesmärgid, ravimid. | Lai ligipääs kõigile aktiivsetele patsiendijuhtumitele; võib luua ja muuta enda või oma rolliga seotud ressursse. |
| **Admin** (haldur) | Süsteemiadministraator, kes haldab kasutajaid, uuringuid ja organisatsiooniüksusi. | Praktikute haldamine, organisatsioonide haldamine, uuringutiimide haldamine, kõigi ressursside (v.a. kliinilised andmed) vaatamine. | Kõrgtaseme halduslik ligipääs. Ei tee kliinilisi sisestusi. |
| **Auditor** (auditeerija) | Kontrollib süsteemi, kuid ei tee muudatusi. | Kõigi kliiniliste ja haldusressursside vaatamine (read-only). | Ainult lugemisõigus, ei muuda midagi. |
| **Member** (meeskonnaliige) | Heaoluplaani või programmi tiimiliige, kellel on vaatamisõigus. | Patsiendi info vaatamine, manuste ja dokumentide vaatamine, suhtluse ja kliiniliste kokkuvõtete vaatamine. | Read-only ligipääs heaolu-meeskonna kontekstis. |
| **Collaborator** (laiendatud õigustega meeskonnaliige) | Laiendatud õigustega meeskonnaliige, kes saab muuta ja lisada sisu, lisaks vaatamisele. | Manuste lisamine, kliiniliste kirjete muutmine, ülesannete muutmine, küsimustike muutmine, protseduuride ja muu sisu muutmine. | Võib muuta ja lisada sisu, kuid ei juhi heaolu-meeskonda ega ava/sulge plaane. |
| **Care-manager** (tervisejuht) | Heaoluplaani eest vastutaja ja meeskonna juht. | Heaoluplaanide loomine ja sulgemine, meeskonna liikmete lisamine/eemaldamine, õiguste haldus, nõusolekute haldamine. | Kõrgeim roll heaoluplaani ulatuses; vastutab meeskonna ja töövoo eest. Omab nii "member" kui "collaborator" õigusi. |


# Süsteemi kasutajad ja õigused

1. DEV-keskkonda on seadistatud mock-kasutajad:
- Jaak-Kristjan Jõeorg (EE38001085718) - audiitor, adminn
- Mari-Liis Männik (EE47101010033) - adminn, spetsialist
- Igor Žaikovski (EE37101010021) - audiitor, spetsialist
- Stephen King (helex123) - adminn, audiitor, spetsialist
- Helen Linn (49105186017) - audiitori roll
- Igor Bossenko (37302102711) - adminni roll
- Aleksei Lissitsin (38412152232) - spetsialisti roll