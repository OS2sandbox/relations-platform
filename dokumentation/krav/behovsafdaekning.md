---
layout: default
title: Behovsafdækning
parent: Behov og krav
grand_parent: Dokumentation
nav_order: 1
---
# OS2 Relationsplatform – behovsafdækning

**Status:** Løbende behovskonsolidering og afklaring. Principperne nedenfor er afklaret i arbejdsdialogen og dokumenteres her som grundlag for den videre behandling i projektet.  
**Opdateret:** 2. november 2026  
**Grundlag:** 21 indsendte usecases (19 oprindelige samt [#32](https://github.com/OS2sandbox/relations-platform/issues/32) og [#33](https://github.com/OS2sandbox/relations-platform/issues/33) fra 20. oktober) i [projektets GitHub Issues](https://github.com/OS2sandbox/relations-platform/issues)  
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

De første 19 usecases blev samlet i syv behovsområder. Efterfølgende er [#32](https://github.com/OS2sandbox/relations-platform/issues/32) om tilslutningsaftaler og [#33](https://github.com/OS2sandbox/relations-platform/issues/33) om myndigheders tilslutnings- og økonomioverblik indkommet. De behandles inden for de eksisterende områder. Under analysen er **brugerkonti og adgangsstyring** identificeret som et ottende, tværgående behovsområde uden et oprindeligt usecase-issue.

| Nr. | Behovsområde | GitHub-issues | Fase |
| --- | --- | --- | --- |
| 1 | Kontaktpersoner, roller og målgrupper | [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18), [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | 1 |
| 2 | Relationshistorik, dialog og opfølgning | [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17) | 1 |
| 3 | Organisationer, produkter og projekter | [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29), [#32](https://github.com/OS2sandbox/relations-platform/issues/32), [#33](https://github.com/OS2sandbox/relations-platform/issues/33) (tilslutningsdelen) | 1 |
| 4 | Kommunikation og onboarding | [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27) | 1 |
| 5 | Hjemmeside og arrangementer | [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22) | 1 |
| 6 | Brugerkonti og adgangsstyring | Supplerende behov identificeret under analysen; intet oprindeligt issue | 1 |
| 7 | Økonomi, fakturering og regnskab | [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23), [#33](https://github.com/OS2sandbox/relations-platform/issues/33) (økonomidelen) | Senere afklaring |
| 8 | Teknisk videndeling og integrationer på tværs af OS2-produkter | [#30](https://github.com/OS2sandbox/relations-platform/issues/30) | Senere afklaring |

**Fase 1:** Seks behovsområder. Af de oprindelige 19 usecases hører 16 til fase 1, mens tre vedrører senere afklaring. Issue #32 indgår i fase 1; issue #33 indeholder både et fase 1-behov (internt overblik over produkttilslutninger) og behov til senere fase (kommunal selvbetjening og økonomi). Område 6 er supplerende og tælles ikke som et indsendt issue. Område 5 omfatter hjemmeside som selvstændig funktion med særlig kobling til arrangementer.

Områdeinddelingen er ikke en beslutning om antallet af tekniske systemer.

## 3. Tværgående principper og grundregistre

### 3.1 Platformens primære anvendelse

OS2 Relationsplatform skal primært være et **internt arbejdsredskab for OS2-sekretariatet og produktforvaltere** på tværs af OS2-produkter. Den skal ikke udvikles som en generel brugerportal for alle kommunale medarbejdere. Kontaktpersoner og andre relevante aktører skal dog kunne få afgrænset adgang til nødvendige selvbetjeningsfunktioner.

### 3.2 Fælles, relationelt forbundne registre

De fælles oplysninger skal logisk være organiseret i selvstændige registre med forbindelser mellem dem:

| Register | Hvad det beskriver |
| --- | --- |
| **Personer** | Ét fælles kontaktkort pr. person med relevante kontaktoplysninger. |
| **Organisationer** | Organisationer med fælles stamoplysninger; en persons afdeling/enhed kan registreres uden krav om fuldt organisationshierarki. |
| **Produkter og projekter** | OS2-produkter/-projekter og relevante stamoplysninger. |
| **Platformens systemer** | De konkrete it-systemer, der indgår i relationsplatformen, og deres funktioner, integrationer og kobling til adgangsstyring. |

En person kan have flere samtidige **organisations-, produkt- og rolletilknytninger** uden at optræde som flere selvstændige kontaktkort. Strukturerede kontaktfunktioner (fx teknisk eller faglig kontakt) knyttes til den konkrete sammenhæng mellem person, organisation og produkt; samme person kan have flere funktioner. Organisationsmedlemskab, formel produkttilslutning og faktisk anvendelse af et produkt er særskilte forhold. Relationer kan efter behov beskrives med rolle, status og gyldighedsperiode.

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

### 3.4 Decentral registrering og vedligeholdelse

Registrering og vedligeholdelse skal så vidt muligt kunne ske decentralt hos de relevante produktforvaltere. Adgang til at registrere må ikke som udgangspunkt være forbeholdt centrale funktioner. Samtidig skal fælles oplysninger beskyttes mod utilsigtede ændringer på tværs af produkter. Den detaljerede fordeling af registreringsrettigheder, dataansvar og administrative beføjelser afklares senere samlet.

### 3.5 Principper samlet

| ID | Princip | Status |
| --- | --- | --- |
| G-01 | Logisk fælles registre for personer, organisationer samt produkter/projekter. | Afklaret i arbejdsdialog |
| G-02 | Relationer forbinder registrene og kan rumme flere samtidige roller og tilknytninger. | Afklaret i arbejdsdialog |
| G-03 | En persons afdeling/organisatoriske enhed kan registreres som supplerende oplysning uden krav om fuldt organisationshierarki i fase 1. | Revideret 02.11.2026 |
| G-04 | Platformen kan sammensættes af flere selvstændige systemer. | Afklaret som udgangspunkt |
| G-05 | Afgrænset systemregister over de systemer, som indgår i selve platformen, er del af fase 1. | Afklaret i arbejdsdialog |
| G-06 | Brugeres identiteter og rettigheder skal kunne håndteres på tværs af platformens systemer. | Afklaret i arbejdsdialog |
| G-07 | Federeret adgang skal kunne understøttes; OS2rollekatalog vurderes som mulighed, ikke valgt løsning. | Princip afklaret; løsning åben |
| G-08 | Afhængigheder mellem systemer bør begrænses, så enkelte systemer kan udskiftes. | Retningsgivende; konkretisering åben |
| G-09 | OS2-medlemskab, formel produkttilslutning og faktisk produktanvendelse registreres som tre særskilte forhold. | Afklaret 02.11.2026 |
| G-10 | Registrering og vedligeholdelse muliggøres så decentralt som muligt; detaljeret ansvar og rettigheder afklares samlet senere. | Afklaret 02.11.2026 |
| G-11 | Projekter og produkter registreres i samme grundregister med livscyklusstatus og bevaret historik. | Afklaret 02.11.2026 |
| G-12 | Kontaktfunktioner registreres struktureret på relationen mellem person, organisation og produkt og bruges til søgning og målgrupper. | Afklaret 02.11.2026 |

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
**Afklaret:** Tre centrale registre med relationer; organisationshierarki er ikke et krav i fase 1. Afdeling/enhed kan registreres som supplerende oplysning, og kontaktfunktioner knyttes til personens relation til organisation og produkt.  
**Åbent:** Hvilke relationstyper og statuser kræves ved første ibrugtagning?

### K-03 – Roller og ansvar

Det skal være muligt at finde personer med en bestemt funktion eller et bestemt ansvar – også personer, der ikke er primære produktforvaltere, fx medarbejdere med kommunikationsopgaver. **Kontaktfunktioner registreres som strukturerede værdier på personens relation til organisation og produkt**, herunder mulighed for flere funktioner i samme produkt. Produktforvaltere skal kunne registrere relevante oplysninger decentralt. **Platformadministrator** har tværgående rettigheder. Detaljeret rolle- og ansvarsfordeling fastlægges senere samlet.

**Sporbarhed:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#27](https://github.com/OS2sandbox/relations-platform/issues/27), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Afklaret:** Skel mellem forretnings- og adgangsroller og mellem produktforvalter og platformadministrator.  
**Åbent:** Fælles katalog over roller, og hvordan tidsbegrænsede eller delte ansvar beskrives.

### K-04 – Søgbare målgrupper og kontaktlister

Kontaktpersoner skal kunne fremsøges på grundlag af deres relationer og strukturerede kontaktfunktioner, eksempelvis organisation, produkt, teknisk/faglig funktion, rolle eller interesse. Det skal gøre det muligt at finde relevante modtagere til invitationer og kommunikation, herunder personer med kommunikationsopgaver på tværs af produkter.

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

## 6. Organisationer, produkter og projekter

**Status:** Behovsområdet er gennemgået på principniveau. Detaljer om felter, statusværdier og rettigheder er fortsat åbne.  
**Usecases:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29), [#32](https://github.com/OS2sandbox/relations-platform/issues/32) og [#33](https://github.com/OS2sandbox/relations-platform/issues/33).

### OP-01 – Fælles register for produkter og projekter

Produkter og projekter registreres i samme grundregister. Et projekt kan overgå til et produkt uden at få et nyt grundkort, miste historik eller få brudt sine relationer. **Livscyklusstatus, formelt OS2-niveau og governancestatus** er tre forskellige oplysninger, der ikke må sammenblandes.

**Sporbarhed:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20).  
**Åbent:** De konkrete statusværdier, hvilke øvrige grunddata der er nødvendige, og regler for historik.

### OP-02 – Organisationers medlemskab, tilslutning og anvendelse

En organisations medlemskab af OS2 registreres særskilt fra dens formelle tilslutninger til OS2-produkter. Faktisk anvendelse af et produkt registreres som et tredje, uafhængigt forhold: En organisation kan anvende et produkt uden at være OS2-medlem eller formelt tilsluttet produktet. Interessetilkendegivelser kan tilsvarende registreres uden at blive forvekslet med en indgået tilslutning.

En formel **produkttilslutning** beskrives som en selvstændig relation mellem organisation og produkt med status, dato for tilslutning og eventuelt ophør, relevante kontakter samt reference til eventuel aftale. Overblik skal kunne vises begge veje: fra organisation til produkter og fra produkt til organisationer.

**Sporbarhed:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#33](https://github.com/OS2sandbox/relations-platform/issues/33).  
**Åbent:** Præcise statusværdier samt vedligeholdelse af fælles stamdata.

### OP-03 – Tilslutningsaftaler som dokumentreferencer

Underskrevne aftaler skal kunne fremsøges fra både den relevante organisation og det relevante produkt. **Dokumentet kan opbevares i et eksisterende dokumentlager**; relationsplatformen skal derfor kunne knytte en sikker reference eller et link til tilslutningen uden at kræve opbevaring af dokumentet i selve platformen. Adgang til aftaler skal følge relevante rettigheder.

**Sporbarhed:** [#32](https://github.com/OS2sandbox/relations-platform/issues/32).  
**Åbent:** Valg af dokumentlager, linkholdbarhed og konkret adgangskontrol.

### OP-04 – Overordnet governanceoverblik

For hvert produkt skal der kunne registreres aktuel governancestatus, dato for seneste vurdering, ansvarlig og link til underliggende dokumentation, fx selvevaluering i GitHub. Dokumentationen skal ikke kopieres ind som et parallelt governance-system. **Produktforvalteren vedligeholder disse oplysninger for sit produkt.**

**Sporbarhed:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20).  
**Åbent:** Statusbegreber og eventuel senere automatiseret opdatering.

### OP-05 – Overblik og adgang

I **fase 1** skal relevante interne brugere kunne fremsøge produkter, organisationer, kontaktpersoner, tilslutninger og anvendelse inden for deres rettigheder. Produktforvaltere skal kunne se oplysninger om egne produkter; Platformadministrator har tværgående administrative rettigheder. Muligheden for, at en organisation senere kan se **egne** produkttilslutninger, skal kunne tilføjes uden grundlæggende ændringer i data- og adgangsmodellen.

Selvbetjening for myndigheder, herunder samlet økonomioversigt over produktbidrag og øvrige forpligtelser fra [#33](https://github.com/OS2sandbox/relations-platform/issues/33), indgår **ikke** i fase 1. Internt overblik over tilslutninger indgår i fase 1; økonomi-/faktureringsfunktioner gør ikke.

**Sporbarhed:** [#29](https://github.com/OS2sandbox/relations-platform/issues/29), [#33](https://github.com/OS2sandbox/relations-platform/issues/33).  
**Åbent:** Præcis læseadgang for øvrige interne roller, fx koordinationsgruppemedlemmer.

### OP-06 – Decentral vedligeholdelse og kontaktfunktioner

Produktforvaltere skal så vidt muligt kunne registrere og ajourføre oplysninger om egne produkter, deres kontakter, anvendelse og relationer. Platformen skal ikke skabe en unødvendig central flaskehals. Fælles organisationsdata skal dog beskyttes mod uhensigtsmæssige ændringer, der påvirker andre produkter.

Kontaktens eventuelle afdeling kan registreres som supplerende oplysning, men et fuldt kommunalt organisationshierarki er **ikke et krav i fase 1**. Det centrale behov er at kunne klassificere en persons funktion i forhold til et produkt (fx teknisk kontakt eller faglig kontakt) og fremsøge målgrupper på den baggrund.

**Sporbarhed:** [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Åbent:** Samlet model for dataansvar, redigeringsrettigheder og godkendelser; behandles senere frem for at blive fastlåst for hver oplysning nu.

## 7. Øvrige behovsområder og videre arbejde

Følgende områder i fase 1 er endnu ikke konsolideret på samme detaljeringsniveau:

- **Relationshistorik, dialog og opfølgning:** [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17).
- **Kommunikation og onboarding:** [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27).
- **Hjemmeside og arrangementer:** [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22).

Senere behovsafklaring (ikke fase 1):

- **Økonomi, fakturering og regnskab:** [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23) og økonomidelen af [#33](https://github.com/OS2sandbox/relations-platform/issues/33).
- **Teknisk videndeling på tværs af OS2-produkter:** [#30](https://github.com/OS2sandbox/relations-platform/issues/30).

## 8. Afklaringer og beslutningsspor

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
| 20.10.2026 | Registre | Selvstændige, relationelt forbundne registre for personer, organisationer og produkter/projekter; kravet om organisationshierarki er efterfølgende revideret. |
| 20.10.2026 | Platformsystemer | Afgrænset register over platformens egne systemer i fase 1; forskelligt fra issue #30. |
| 20.10.2026 | Identitet og adgang | Sammenhængende/federeret adgang på tværs af systemer; OS2rollekatalog er en mulighed, ikke et systemvalg. |
| 02.11.2026 | Nye usecases | #32 og #33 indarbejdet; myndigheders egen tilslutnings-/økonomioversigt ligger senere, internt tilslutningsoverblik i fase 1. |
| 02.11.2026 | Produkter | Fælles register for projekter/produkter; livscyklus, OS2-niveau og governance adskilles. |
| 02.11.2026 | Governance | Overordnet status, dato, ansvarlig og dokumentlink; produktforvalteren vedligeholder egne oplysninger. |
| 02.11.2026 | Organisationer | OS2-medlemskab, produkttilslutning og faktisk anvendelse holdes adskilt. |
| 02.11.2026 | Aftaler | Underskrevne tilslutningsaftaler kan ligge i dokumentlager; platformen har søgbar reference. |
| 02.11.2026 | Tilslutninger | Selvstændig organisation-produkt-relation med status, datoer, kontakter og aftalelink. |
| 02.11.2026 | Decentral administration | Produktforvaltere skal kunne registrere og vedligeholde bredt inden for egne produkter; detaljefordeling af ansvar behandles senere. |
| 02.11.2026 | Organisationsoplysninger | Ingen obligatorisk organisationshierarki i fase 1; supplerende afdeling samt strukturerede produktvise kontaktfunktioner. |

**Næste trin:** Gennemgå relationshistorik, dialog og opfølgning og derefter de øvrige uafklarede behovsområder, fastholde nye afklaringer her og videreføre de tilstrækkeligt modne formuleringer til [kravspecifikation.md](kravspecifikation.md). Kravene prioriteres først, når det samlede billede for fase 1 er bedre belyst.
