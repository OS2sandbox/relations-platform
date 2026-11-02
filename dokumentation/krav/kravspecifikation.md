---
layout: default
title: Kravspecifikation
parent: Behov og krav
grand_parent: Dokumentation
nav_order: 2
---

# OS2 Relationsplatform – kravspecifikation (første udkast)

**Status:** Levende kravgrundlag, ikke endeligt godkendt eller prioriteret  
**Opdateret:** 2. november 2026  
**Grundlag:** [Behovsafdækning](behovsafdaekning.md) og de oprindelige [GitHub-issues](https://github.com/OS2sandbox/relations-platform/issues)

## 1. Formål og anvendelse

Dette dokument omsætter tilstrækkeligt afklarede behov og principper til **foreløbige krav til den samlede OS2 Relationsplatform**. Det er grundlaget for senere vurdering og afprøvning af eksisterende open source-systemer – ikke en bestilling af et bestemt system eller en bestemt teknisk arkitektur.

Et krav kan opfyldes af ét system eller af flere systemer i samspil. Nye krav føjes til, efterhånden som behovsområderne gennemgås. Oprindelige usecases forbliver i GitHub; se sporbarhedskolonnen.

**Skelnen:** Et *behov* beskriver formålet, et *princip* den aftalte retning, og et *krav* hvad platformen skal kunne understøtte. Kravene nedenfor er foreløbige formuleringer og skal senere gøres afprøvelige, herunder med konkrete vurderingskriterier.

## 2. Første kravudkast – grundregistre og kontaktstyring

| ID | Krav til platformen | Grundlag | Status |
| --- | --- | --- | --- |
| **KR-01** | Platformen skal understøtte fælles, relationelt forbundne oplysninger om personer, organisationer samt OS2-produkter/-projekter uden krav om én bestemt fysisk databaseløsning. | [G-01/G-02](behovsafdaekning.md#35-principper-samlet), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21) | Kravudkast |
| **KR-02** | Platformen skal understøtte ét fælles kontaktkort pr. person og flere samtidige organisations-, produkt- og rolletilknytninger til samme person. | [K-01](behovsafdaekning.md#k-01--fælles-kontaktgrundlag), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18) | Kravudkast |
| **KR-03** | Platformen skal kunne registrere en persons eventuelle afdeling eller organisatoriske enhed som supplerende oplysning, uden at det kræver et fuldt organisationshierarki. | [G-03](behovsafdaekning.md#35-principper-samlet), [OP-06](behovsafdaekning.md#op-06--decentral-vedligeholdelse-og-kontaktfunktioner) | Revideret 02.11.2026; hierarki udgår af fase 1 |
| **KR-04** | Platformen skal kunne registrere en formel produkttilslutning som en selvstændig relation mellem organisation og produkt med status, tilslutnings-/ophørsdatoer, relevante kontaktpersoner og dokumentreference. Relationen skal kunne fremsøges fra begge sider. | [OP-02](behovsafdaekning.md#op-02--organisationers-medlemskab-tilslutning-og-anvendelse), [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#32](https://github.com/OS2sandbox/relations-platform/issues/32) | Præciseret 02.11.2026; statuskatalog åbent |
| **KR-05** | Platformen skal kunne registrere og fremsøge flere personer med relevante forretningsroller og ansvarsområder i det samme produkt eller projekt. | [K-03](behovsafdaekning.md#k-03--roller-og-ansvar), [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | Kravudkast |
| **KR-06** | Brugere skal kunne finde målgrupper ved at kombinere oplysninger om person, organisation, produkt, rolle og struktureret kontaktfunktion. | [K-04](behovsafdaekning.md#k-04--søgbare-målgrupper-og-kontaktlister), [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | Præciseret 02.11.2026; udsendelse ikke afklaret |

## 3. Første kravudkast – selvbetjening og vedligeholdelse

| ID | Krav til platformen | Grundlag | Status |
| --- | --- | --- | --- |
| **KR-07** | Registrerede kontaktpersoner skal kunne kontrollere, bekræfte og ajourføre egne kontaktoplysninger via afgrænset selvbetjening, uden krav om adgang til platformens fulde interne funktioner. | [K-05](behovsafdaekning.md#k-05--selvbetjening-og-påmindelser), [#18](https://github.com/OS2sandbox/relations-platform/issues/18) | Kravudkast |
| **KR-08** | Kontaktpersoner skal kunne se og bekræfte egne roller og produkttilknytninger eller foreslå ændringer; forslag til ændringer skal kunne godkendes af relevant produktforvalter. | [K-05](behovsafdaekning.md#k-05--selvbetjening-og-påmindelser), [#18](https://github.com/OS2sandbox/relations-platform/issues/18) samt afklaring i arbejdsdialog | Kravudkast |
| **KR-09** | Platformen skal understøtte automatisk påmindelse om ajourføring med et fælles standardinterval (foreløbigt ét år) og mulighed for et andet interval pr. produkt, uden at én person modtager overlappende påmindelser fra flere produkter. | [K-05](behovsafdaekning.md#k-05--selvbetjening-og-påmindelser), [#18](https://github.com/OS2sandbox/relations-platform/issues/18) | Kravudkast; koordineringsregel åben |
| **KR-10** | Påmindelsen skal kunne vises, når personen i forvejen anvender platformen, og skal også kunne gives gennem en alternativ kanal, når personen ikke besøger platformen. Tidspunkt for seneste bekræftelse og manglende svar skal kunne følges. | [K-05](behovsafdaekning.md#k-05--selvbetjening-og-påmindelser), [#18](https://github.com/OS2sandbox/relations-platform/issues/18) samt afklaring i arbejdsdialog | Kravudkast; kanal og detaljer åbne |

## 4. Første kravudkast – brugere, adgang og systemer

Dette område er tilføjet under behovsafdækningen. Kravene er derfor **afledte behov** og har ikke særskilte indsendte GitHub-issues.

| ID | Krav til platformen | Grundlag | Status |
| --- | --- | --- | --- |
| **KR-11** | Platformen skal understøtte rollebaseret adgang med mulighed for rettigheder afgrænset til egne produkter og tværgående rettigheder for rollen **Platformadministrator**. | [Område 6](behovsafdaekning.md#5-brugerkonti-og-adgangsstyring--supplerende-behov), [#29](https://github.com/OS2sandbox/relations-platform/issues/29) (indblik for koordinationsgruppe) | Kravudkast; detaljerede rettigheder åbne |
| **KR-12** | Brugere skal kunne identificeres og autentificeres sammenhængende på tværs af platformens systemer, herunder med mulighed for federeret autentifikation; rettigheder skal kunne håndteres koordineret. | [G-06/G-07](behovsafdaekning.md#35-principper-samlet), [Område 6](behovsafdaekning.md#5-brugerkonti-og-adgangsstyring--supplerende-behov) | Kravudkast; teknisk løsning åben |
| **KR-13** | Adgang til systemer og funktioner skal kunne tildeles, ændres og tilbagekaldes på en administrerbar måde, også når én bruger arbejder i flere af platformens systemer. | [Område 6](behovsafdaekning.md#5-brugerkonti-og-adgangsstyring--supplerende-behov) | Kravudkast; proces og sporbarhed åbne |
| **KR-14** | Der skal kunne føres et samlet overblik over de systemer, der indgår i relationsplatformen, deres funktioner, integrationer og relation til fælles adgangsstyring. | [G-05](behovsafdaekning.md#35-principper-samlet), [Område 6](behovsafdaekning.md#5-brugerkonti-og-adgangsstyring--supplerende-behov) | Kravudkast; hvilke felter åbent |
| **KR-15** | Platformens systemer skal så vidt muligt kunne integreres og udskiftes, uden at fælles kontakt-, organisations- og produktdata eller brugernes adgang skal genopbygges fra bunden. | [G-04/G-08](behovsafdaekning.md#35-principper-samlet) | Retningsgivende krav – konkretisering nødvendig |

## 5. Kravudkast – organisationer, produkter og projekter

| ID | Krav til platformen | Grundlag | Status |
| --- | --- | --- | --- |
| **KR-16** | Strukturerede kontaktfunktioner skal kunne knyttes til relationen mellem person, organisation og produkt; flere funktioner for samme person og produkt skal understøttes. | [K-03](behovsafdaekning.md#k-03--roller-og-ansvar), [OP-06](behovsafdaekning.md#op-06--decentral-vedligeholdelse-og-kontaktfunktioner), [#11](https://github.com/OS2sandbox/relations-platform/issues/11) | Kravudkast |
| **KR-17** | Projekter og produkter skal kunne vedligeholdes i et fælles register, hvor et projekt kan blive til et produkt med bevarede relationer og historik. Livscyklusstatus og formelt OS2-niveau registreres særskilt. | [OP-01](behovsafdaekning.md#op-01--fælles-register-for-produkter-og-projekter), [#20](https://github.com/OS2sandbox/relations-platform/issues/20) | Kravudkast; statusværdier åbne |
| **KR-18** | Platformen skal vise produkters overordnede governancestatus, dato for seneste vurdering, ansvarlig produktforvalter og reference til underliggende dokumentation uden at kræve lagring af selve dokumentationen. | [OP-04](behovsafdaekning.md#op-04--overordnet-governanceoverblik), [#20](https://github.com/OS2sandbox/relations-platform/issues/20) | Kravudkast |
| **KR-19** | Platformen skal registrere OS2-medlemskab, formel produkttilslutning og faktisk produktanvendelse som særskilte oplysninger. En organisation skal kunne være bruger af et produkt uden medlemskab eller formel tilslutning. | [OP-02](behovsafdaekning.md#op-02--organisationers-medlemskab-tilslutning-og-anvendelse), [#21](https://github.com/OS2sandbox/relations-platform/issues/21) | Kravudkast |
| **KR-20** | Til en produkttilslutning skal kunne knyttes en reference til underskrevet aftale i et dokumentlager uden for relationsplatformen; aftalen skal kunne fremsøges via organisation og produkt under hensyn til adgangsrettigheder. | [OP-03](behovsafdaekning.md#op-03--tilslutningsaftaler-som-dokumentreferencer), [#32](https://github.com/OS2sandbox/relations-platform/issues/32) | Kravudkast; dokumentlager og adgangsmodel åbne |
| **KR-21** | Relevante interne brugere skal i fase 1 kunne få overblik over organisationers produkttilslutninger og produktets tilsluttede organisationer. Datamodellen og adgangsstyringen skal kunne udvides med en organisationsafgrænset visning for myndigheder senere. | [OP-05](behovsafdaekning.md#op-05--overblik-og-adgang), [#29](https://github.com/OS2sandbox/relations-platform/issues/29), [#33](https://github.com/OS2sandbox/relations-platform/issues/33) | Kravudkast; ekstern selvbetjening og økonomi ikke fase 1 |
| **KR-22** | Produktforvaltere skal som udgangspunkt kunne registrere og vedligeholde oplysninger om egne produkter, kontakter, aktiviteter og relationer uden at være afhængige af central registrering. Fælles data skal kunne beskyttes mod utilsigtede ændringer på tværs af produkter. | [G-10](behovsafdaekning.md#35-principper-samlet), [OP-06](behovsafdaekning.md#op-06--decentral-vedligeholdelse-og-kontaktfunktioner) | Kravudkast; detaljerede rettigheder og dataansvar åbne |

## 6. Bevidst ikke fastlagt endnu

- **Systemvalg:** OS2rollekatalog er en løsning, der kan undersøges, ikke en valgt komponent. Andre identitets- og rettighedsløsninger er ikke udelukket.
- **Fysisk arkitektur:** Hvilke registre og funktioner der ligger i hvilket system, er åbent.
- **Detaljeret rettighedsmatrix:** Præcis hvem der kan læse, oprette, ændre og slette oplysninger, skal beskrives senere.
- **Målgrupper og kommunikation:** Det er endnu ikke afklaret, om udsendelse af invitationer og beskeder sker i platformen eller i et tilknyttet system.
- **Påmindelser:** Samlet koordinering ved forskelligt interval mellem flere produkttilknytninger er endnu ikke fastlagt.
- **Andre fase 1-områder:** Krav til dialoghistorik, kommunikation, onboarding, hjemmeside og arrangementer tilføjes, når de er gennemgået på behovsniveau.
- **Organisationer og produkter:** Statuskataloger, datakvalitet, overordnet ansvar og individuel læse-/skriveadgang skal konkretiseres senere.
- **Myndigheders selvbetjening og økonomi:** Issue #33 fastholdes med behov om selvbetjening og økonomisk overblik i en senere fase; kun den interne tilslutningsoversigt indgår i fase 1.
- **Prioritering:** Ingen krav er endnu klassificeret som fx skal/bør eller prioriteret i forhold til hinanden.

## 7. Videre proces og sporbarhed

1. Konsolider næste behovsområde i [behovsafdækningen](behovsafdaekning.md), mens oprindelige usecases bevares.
2. Udled eller justér krav i dette dokument med stabile KR-ID'er og sporbarhed til behov og issue.
3. Afklar åbne spørgsmål, før krav bruges til at evaluere systemer som endeligt vurderingsgrundlag.
4. Gennemgå ændringer gennem projektets GitHub-proces. Når det samlede fase 1-billede er tilstrækkeligt belyst, kan krav prioriteres og omsættes til vurderingskriterier.
