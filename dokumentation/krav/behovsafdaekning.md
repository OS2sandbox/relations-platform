# OS2 Relationsplatform – behovsafdækning

**Status:** Løbende behovskonsolidering og afklaring. Principperne nedenfor er afklaret i arbejdsdialogen og dokumenteres her som grundlag for den videre behandling i projektet.  
**Opdateret:** 20. oktober 2026  
**Grundlag:** 19 indsendte usecases i [projektets GitHub Issues](https://github.com/OS2sandbox/relations-platform/issues)  
**Relateret dokument:** [Kravspecifikation – første udkast](kravspecifikation.md)  
**Arbejdsprincipper:** [Dokumentationens README](../README.md)

## 1. Formål og arbejdsform

Dokumentet samler og konsoliderer de behov, der er indsendt til OS2 Relationsplatform, og de supplerende behov, som afdækkes under analysen. Det skal give arbejdsgruppen et sporbarligt grundlag for senere at vurdere og afprøve konkrete systemer.

- De oprindelige usecases bevares som GitHub-issues med kontakt til indsenderen.
- Beslægtede behov, sammenhænge, afklaringer og arbejdsbeslutninger dokumenteres her.
- Krav, der kan formuleres tilstrækkeligt præcist, samles særskilt i [kravspecifikation.md](kravspecifikation.md) og henviser tilbage hertil og til issues.
- Github-dokumenterne er den fælles dokumentation. Tidligere Word- og Excel-filer er arbejdsredskaber, ikke parallelle, gældende versioner.
- Ændringer til dokumentationen kan behandles gennem Pull Requests efter projektets GitHub-proces.

**Overordnet målsætning:** Undersøge, hvordan eksisterende open source-systemer kan sammensættes til én sammenhængende platform til OS2's administrative behov. Det er ikke afgjort, hvilke konkrete systemer der skal indgå, eller hvor data fysisk skal ligge.

## 2. Behovsområder og afgrænsning

De 19 oprindelige usecases er samlet i syv behovsområder. Under analysen er **brugerkonti og adgangsstyring** identificeret som et ottende, tværgående behovsområde uden et oprindeligt usecase-issue.

| Nr. | Behovsområde | GitHub-issues | Fase |
| --- | --- | --- | --- |
| 1 | Kontaktpersoner, roller og målgrupper | [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18), [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | 1 |
| 2 | Relationshistorik, dialog og opfølgning | [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17) | 1 |
| 3 | Organisationer, produkter og projekter | [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29) | 1 |
| 4 | Kommunikation og onboarding | [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27) | 1 |
| 5 | Hjemmeside og arrangementer | [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22) | 1 |
| 6 | Brugerkonti og adgangsstyring | Supplerende behov identificeret under analysen; intet oprindeligt issue | 1 |
| 7 | Økonomi, fakturering og regnskab | [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23) | Senere afklaring |
| 8 | Teknisk videndeling og integrationer på tværs af OS2-produkter | [#30](https://github.com/OS2sandbox/relations-platform/issues/30) | Senere afklaring |

**Fase 1:** Seks behovsområder; 16 af de 19 oprindelige usecases. **Senere afklaring:** To selvstændige områder; tre usecases. Område 6 er supplerende og tælles ikke som et nyt, indsendt issue. Område 5 omfatter hjemmeside som selvstændig funktion med særlig kobling til arrangementer, som annonceres på hjemmesiden.

Områdeinddelingen er ikke en beslutning om antallet af tekniske systemer.

## 3. Tværgående principper og grundregistre

### 3.1 Platformens primære anvendelse

OS2 Relationsplatform skal primært være et **internt arbejdsredskab for OS2-sekretariatet og produktforvaltere** på tværs af OS2-produkter. Den skal ikke udvikles som en generel brugerportal for alle kommunale medarbejdere. Kontaktpersoner og andre relevante aktører skal dog kunne få afgrænset adgang til nødvendige selvbetjeningsfunktioner.

### 3.2 Fælles, relationelt forbundne registre

De fælles oplysninger skal logisk være organiseret i selvstændige registre med forbindelser mellem dem:

| Register | Hvad det beskriver |
| --- | --- |
| **Personer** | Ét fælles kontaktkort pr. person med relevante kontaktoplysninger. |
| **Organisationer** | Organisationer samt deres underliggende enheder og hierarkier. |
| **Produkter og projekter** | OS2-produkter/-projekter og relevante stamoplysninger. |
| **Platformens systemer** | De konkrete it-systemer, der indgår i relationsplatformen, og deres funktioner, integrationer og kobling til adgangsstyring. |

En person kan have flere samtidige **organisations-, produkt- og rolletilknytninger** uden at optræde som flere selvstændige kontaktkort. Organisationer kan have relationer til flere produkter, fx som tilsluttet, interesseret eller leverandør. Relationer kan efter behov beskrives med rolle, status og gyldighedsperiode.

Registeret over *platformens egne systemer* er en del af fase 1. Det må ikke forveksles med det bredere katalog over samtlige OS2-produkters komponenter, API'er og integrationer i [issue #30](https://github.com/OS2sandbox/relations-platform/issues/30), som først afklares senere.

Disse begreber beskriver det fælles informationsbehov. De fastlægger **ikke** en bestemt databasestruktur, et centralt fysisk register eller et bestemt produkt.

### 3.3 Flere systemer – sammenhængende adgang

Platformen kan bestå af flere integrerede systemer. Brugerens identitet og adgang skal derfor kunne håndteres sammenhængende på tværs af systemerne, med mulighed for **federeret autentifikation og adgangsstyring**.

Der skelnes mellem:

- **Forretningsrolle:** Personens ansvar i OS2-fællesskabet, fx produktkoordinator eller koordinationsgruppemedlem.
- **Adgangsrolle:** Hvad personen må se, redigere og administrere i platformen.

Foreløbige adgangsroller:

| Adgangsrolle | Principiel adgang |
| --- | --- |
| **Kontaktperson** | Afgrænset selvbetjening vedrørende egne oplysninger og forslag til tilknytninger. |
| **Produktforvalter** | Administration af relevante kontakter, roller og produkttilknytninger inden for egne produkter. |
| **Platformadministrator** | Tværgående administration af oplysninger, brugere og rettigheder på tværs af platformen. |

Rettigheden til at administrere hele platformen følger rollen **Platformadministrator**, ikke automatisk et ansættelsesforhold i OS2-sekretariatet. En person kan have mere end én adgangsrolle.

**OS2rollekatalog er et relevant alternativ at undersøge**, men der er ikke truffet beslutning om løsning eller verificeret egnethed til brugere fra flere organisationer. Hvilken løsning der kan levere identitetsstyring, login og autorisation, skal afklares i systemvurderingen.

### 3.4 Principper samlet

| ID | Princip | Status |
| --- | --- | --- |
| G-01 | Logisk fælles registre for personer, organisationer samt produkter/projekter. | Afklaret i arbejdsdialog |
| G-02 | Relationer forbinder registrene og kan rumme flere samtidige roller og tilknytninger. | Afklaret i arbejdsdialog |
| G-03 | Organisationer kan beskrives hierarkisk med underliggende enheder. | Afklaret i arbejdsdialog |
| G-04 | Platformen kan sammensættes af flere selvstændige systemer. | Afklaret som udgangspunkt |
| G-05 | Afgrænset systemregister over de systemer, som indgår i selve platformen, er del af fase 1. | Afklaret i arbejdsdialog |
| G-06 | Brugeres identiteter og rettigheder skal kunne håndteres på tværs af platformens systemer. | Afklaret i arbejdsdialog |
| G-07 | Federeret adgang skal kunne understøttes; OS2rollekatalog vurderes som mulighed, ikke valgt løsning. | Princip afklaret; løsning åben |
| G-08 | Afhængigheder mellem systemer bør begrænses, så enkelte systemer kan udskiftes. | Retningsgivende; konkretisering åben |

## 4. Kontaktpersoner, roller og målgrupper

**Status:** Første behovsområde gennemgået på principniveau. Enkelte detaljer er fortsat åbne.  
**Usecases:** [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).

### K-01 – Fælles kontaktgrundlag

Kontaktoplysninger skal kunne findes og ajourføres i et fælles arbejdsgrundlag. **En person har ét fælles kontaktkort** og kan være tilknyttet flere organisationer, produkter og projekter uden dobbeltregistrering. Forskellige roller og relationer føjes til det samme kontaktkort.

**Sporbarhed:** [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18).  
**Afklaret:** Én fælles personregistrering; flere samtidige tilknytninger.  
**Åbent:** Hvilke kontaktfelter og historikoplysninger er nødvendige, og hvordan sammenføjes eksisterende dubletter?

### K-02 – Organisationer, produkter og relationer

Personers tilknytning til organisationer og OS2-produkter skal være synlig og kunne vedligeholdes. Organisationsoplysninger og produktoplysninger vedligeholdes i egne registre. Registreringer skal kunne knyttes sammen og anvendes på tværs.

**Sporbarhed:** [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21).  
**Afklaret:** Tre centrale registre; relationer mellem registrene; organisationshierarkier.  
**Åbent:** Hvilke relationstyper og statuser kræves ved første ibrugtagning?

### K-03 – Roller og ansvar

Det skal være muligt at finde personer med en bestemt funktion eller et bestemt ansvar – også personer, der ikke er primære produktforvaltere, fx medarbejdere med kommunikationsopgaver. Produktforvalteren kan vedligeholde og godkende roller og produkttilknytninger inden for egne produkter. **Platformadministrator** kan administrere på tværs.

**Sporbarhed:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#27](https://github.com/OS2sandbox/relations-platform/issues/27), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Afklaret:** Skel mellem forretnings- og adgangsroller og mellem produktforvalter og platformadministrator.  
**Åbent:** Fælles katalog over roller, og hvordan tidsbegrænsede eller delte ansvar beskrives.

### K-04 – Søgbare målgrupper og kontaktlister

Kontaktpersoner skal kunne fremsøges på grundlag af deres relationer, eksempelvis organisation, produkt, rolle eller interesse. Det skal gøre det muligt at finde relevante modtagere til invitationer og kommunikation, herunder personer med kommunikationsopgaver på tværs af produkter.

**Sporbarhed:** [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Åbent:** Skal målgrupper kunne gemmes/deles, eksporteres eller anvendes direkte til udsendelse via et andet system? Hvem kan se hvilke kontaktoplysninger?

### K-05 – Selvbetjening og påmindelser

Kontaktpersoner skal på en enkel måde kunne kontrollere, bekræfte og ændre egne kontaktoplysninger. De skal samtidig kunne se og **bekræfte eller foreslå ændringer til** egne roller og produkttilknytninger; sådanne ændringer **godkendes af den relevante produktforvalter**.

Ajourføringen organiseres efter følgende afklarede principper:

- Fælles standardinterval for kontrol, foreløbigt **én gang årligt**, med mulighed for at produktforvalteren vælger et andet interval.
- **Én samlet påmindelse pr. person på tværs af produkter**, så flere tilknytninger ikke giver gentagne henvendelser.
- Påmindelse vises gerne, når personen alligevel har et ærinde på platformen, så oplysningerne kan bekræftes eller rettes på stedet.
- Der skal også være mulighed for en alternativ påmindelse, fx pr. mail, når personen ikke besøger platformen inden for intervallet.
- Seneste bekræftelse/ajourføring skal kunne ses; produktforvalteren skal kunne identificere manglende tilbagemeldinger.

**Sporbarhed:** [#18](https://github.com/OS2sandbox/relations-platform/issues/18).  
**Afklaret:** Direkte vedligeholdelse af egne kontaktdata; forslag og godkendelse ved roller/tilknytninger; fælles, koordineret påmindelse.  
**Åbent:** Praktisk koordinering af forskellige intervaller på tværs af produkter; sikker selvbetjening uden fuld brugerkonto; håndtering af organisationstilknytning ved jobskifte.

## 5. Brugerkonti og adgangsstyring – supplerende behov

Dette behovsområde er identificeret under analysen og har **ikke et selvstændigt oprindeligt usecase-issue**. Det er med i fase 1, fordi en platform med flere systemer og flere brugergrupper behøver sammenhængende adgangsstyring.

Foreløbigt skal området omfatte: brugerkonti og tilknytning til personer; sikker autentifikation og mulighed for federeret login; adgangsroller og produktvis afgrænsning; administration, deaktivering og ændring af rettigheder; samt sammenhæng mellem platformens systemer og deres adgangskontrol.

Platformen er primært intern for OS2-sekretariatet og produktforvalterne. Kontaktpersoner skal alene have den afgrænsede selvbetjening, deres opgave kræver. **Et kontaktkort må ikke forudsætte en fuld systembrugerkonto.**

**Afklaring før systemvalg:** Hvordan kan identiteter fra forskellige organisationer genkendes og knyttes sikkert til et fælles kontaktkort? Hvilke systemer kan anvende en fælles identitet/autorisation? Er OS2rollekatalog velegnet til den tværorganisatoriske model? Hvad skal kunne registreres af administrative ændringer?

## 6. Øvrige behovsområder og videre arbejde

Følgende områder i fase 1 er endnu ikke konsolideret på samme detaljeringsniveau:

- **Relationshistorik, dialog og opfølgning:** [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17).
- **Organisationer, produkter og projekter:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29).
- **Kommunikation og onboarding:** [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27).
- **Hjemmeside og arrangementer:** [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22).

Senere behovsafklaring (ikke fase 1):

- **Økonomi, fakturering og regnskab:** [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23).
- **Teknisk videndeling på tværs af OS2-produkter:** [#30](https://github.com/OS2sandbox/relations-platform/issues/30).

## 7. Afklaringer og beslutningsspor

Tabellen opsummerer de principper, der er aftalt i arbejdsdialogen. Den erstatter ikke en senere fælles gennemgang i projektets arbejdsgruppe.

| Dato | Emne | Resultat |
| --- | --- | --- |
| 20.10.2026 | Omfang | Hjemmeside og arrangementer i fase 1; økonomi og bred teknisk videndeling udskudt. |
| 20.10.2026 | Supplerende område | Brugerkonti og adgangsstyring føjet til fase 1 uden nyt indsendt issue. |
| 20.10.2026 | Primære brugere | Platformen er først og fremmest internt værktøj for sekretariat og produktforvaltere. |
| 20.10.2026 | Fælles kontaktkort | Én person, flere samtidige roller og organisation-/produkttilknytninger. |
| 20.10.2026 | Vedligeholdelse | Kontaktpersoner ajourfører egne data; produktforvaltere administrerer og godkender tilknytninger for egne produkter. |
| 20.10.2026 | Administratorrolle | Tværgående administrative rettigheder følger rollen **Platformadministrator**, ikke organisatorisk tilhørsforhold. |
| 20.10.2026 | Påmindelser | Samlet påmindelse pr. person; årsinterval som standard, mulighed for andet interval og gerne situationsbestemt visning. |
| 20.10.2026 | Selvbetjening | Kontaktperson kan bekræfte eller foreslå ændringer til roller og produkttilknytninger; produktforvalter godkender. |
| 20.10.2026 | Registre | Selvstændige, relationelt forbundne registre for personer, organisationer og produkter/projekter; organisationshierarki. |
| 20.10.2026 | Platformsystemer | Afgrænset register over platformens egne systemer i fase 1; forskelligt fra issue #30. |
| 20.10.2026 | Identitet og adgang | Sammenhængende/federeret adgang på tværs af systemer; OS2rollekatalog er en mulighed, ikke et systemvalg. |

**Næste trin:** Uddybe de øvrige behovsområder, fastholde nye afklaringer her og videreføre de tilstrækkeligt modne formuleringer til [kravspecifikation.md](kravspecifikation.md). Kravene prioriteres først, når det samlede billede for fase 1 er bedre belyst.
