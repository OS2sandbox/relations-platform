# OS2 Relationsplatform - behovsafdækning

**Status:** Arbejdsdokument - behovskonsolidering pågår  
**Opdateret:** 20. oktober 2026  
**Grundlag:** 19 indsendte usecases i [projektets GitHub Issues](https://github.com/OS2sandbox/relations-platform/issues)  
**Arbejdsprincipper:** [README](../README.md)

## 1. Formål og anvendelse

Dette dokument samler og fortolker de behov, som er indsendt til OS2 Relationsplatform via GitHub. Det er et fælles grundlag for arbejdsgruppens behovsafklaring og for senere udvælgelse og afprøvning af eksisterende systemer.

- **Oprindelige usecases** bevares i deres GitHub-issues. De er kilden til, hvad bidragyderne faktisk har beskrevet.
- **Konsolideringen her** samler beslægtede behov og gør tværgående sammenhænge og uafklarede spørgsmål tydelige.
- **Afgrænsninger** er dokumenterede arbejdsbeslutninger; **fortolkninger, forslag og spørgsmål** er endnu ikke godkendte krav.
- Den gældende analyse vedligeholdes her i GitHub. Eventuelle Excel- og Word-arbejdsfiler er midlertidige analyseredskaber, ikke parallel dokumentation.
- Væsentlige ændringer gennemgås via Pull Requests, jf. projektets arbejdsprincipper.

Projektets mål er at sammensætte en hensigtsmæssig platform af eksisterende open source-løsninger, ikke at udvikle en ny platform fra bunden. Det er **ikke** besluttet, om behovene skal løses i ét system eller flere samvirkende systemer.

## 2. Samlet behovsbillede og afgrænsning

De 19 usecases er foreløbigt samlet i syv selvstændige behovsområder. Fase 1 omfatter fem områder og 16 usecases. To områder (tre usecases) er relevante, men udskudt til særskilt afklaring.

| Område | Behovsområde | Oprindelige usecases | Afgrænsning |
| --- | --- | --- | --- |
| 1 | Kontaktpersoner, roller og målgrupper | [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18), [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | Fase 1 - uddybes her |
| 2 | Relationshistorik, dialog og opfølgning | [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17) | Fase 1 - endnu ikke konsolideret |
| 3 | Organisationer, produkter og projekter | [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29) | Fase 1 - endnu ikke konsolideret |
| 4 | Kommunikation og onboarding | [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27) | Fase 1 - endnu ikke konsolideret |
| 5 | Hjemmeside og arrangementer | [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22) | Fase 1 - endnu ikke konsolideret |
| 6 | Økonomi, fakturering og regnskab | [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23) | Senere fase - kræver behovsafklaring |
| 7 | Teknisk videndeling og integrationer | [#30](https://github.com/OS2sandbox/relations-platform/issues/30) | Senere fase - kræver behovsafklaring |

**Aftalt afgrænsning:** Hjemmeside er et selvstændigt behovsområde i fase 1. Arrangementer hænger særligt sammen med hjemmesiden, fordi de annonceres der. Økonomi og teknisk videndeling anerkendes og fastholdes som selvstændige områder, men indgår ikke i fase 1.

**Bemærk:** Områderne er en analyseinddeling, ikke et forslag til opdeling af systemer eller databaser.

## 3. Område 1 - Kontaktpersoner, roller og målgrupper

**Status: Første konsolidering til drøftelse, ikke godkendte krav.**

### 3.1 Oprindelige usecases

| Issue | Indsenders behov, kort gengivet | Hovedvinkel |
| --- | --- | --- |
| [#11](https://github.com/OS2sandbox/relations-platform/issues/11) | Finde kontaktpersoner ud fra produkt og rolle for at kunne invitere relevante kommuner til et arrangement. | Udvælge målgruppe |
| [#13](https://github.com/OS2sandbox/relations-platform/issues/13) | Samle opdaterede kontaktpersoner og interesserede på et produkt ét fælles sted frem for spredte lister og kanaler. | Fælles kontaktgrundlag |
| [#18](https://github.com/OS2sandbox/relations-platform/issues/18) | Give den enkelte mulighed for at vedligeholde egne relevante oplysninger og modtage lejlighedsvise påmindelser; skabe motivation gennem relevant information og invitationer. | Ajourføring og selvbetjening |
| [#28](https://github.com/OS2sandbox/relations-platform/issues/28) | Kunne finde alle relevante personer med kommunikationsopgaver, også ud over den primære produktkoordinator. | Roller og tværgående målgrupper |

De fire beskrivelser er ikke fire konkurrerende forslag til løsning. De belyser forskellige anvendelser af et fælles grundlag for personer og deres relationer til OS2-fællesskabet.

### 3.2 Fælles behov - foreløbig konsolidering

Identifikatorerne K-01 til K-05 viderefører den første analyse. Et behov kan også hænge sammen med issues fra andre områder; det ændrer ikke deres placering i oversigten.

#### K-01 - Fælles, ajourført kontaktgrundlag

Sekretariatet og produktforvaltere har behov for at kunne finde og vedligeholde relevante kontaktoplysninger i et fælles, pålideligt arbejdsgrundlag. Behovet udspringer af, at oplysninger i dag er spredt mellem blandt andet mails, Teams, fildrev, Heyloyalty og Nextcloud.

**Kilder:** [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#18](https://github.com/OS2sandbox/relations-platform/issues/18).  
**Afklaring:** Hvilke oplysninger er nødvendige? Hvem er ansvarlig for datakvalitet, og hvordan undgås dobbeltregistrering?

#### K-02 - Personers tilknytning til organisationer og produkter

Det skal være muligt at se, hvilke organisationer og OS2-produkter eller -projekter en person har en relevant tilknytning til. Den samme person kan optræde i flere sammenhænge. En adskillelse af person, tilknytning og rolle er en **arbejdshypotese**, der skal afprøves - ikke en besluttet datamodel.

**Kilder:** [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#18](https://github.com/OS2sandbox/relations-platform/issues/18), [#21](https://github.com/OS2sandbox/relations-platform/issues/21).  
**Afklaring:** Hvad udgør en tilknytning? Kan en person have flere samtidig, og hvem kan vedligeholde dem?

#### K-03 - Roller og ansvar

Brugere har behov for at kunne identificere personer med bestemte funktioner og ansvar. Især kommunikationsopgaver kan være fordelt på flere personer, som ikke nødvendigvis er registreret som primære produktkoordinatorer.

**Kilder:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#27](https://github.com/OS2sandbox/relations-platform/issues/27), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Afklaring:** Hvilke roller skal være kendte på tværs af OS2? Hvordan registreres og ændres ansvar, og hvem har kompetencen til at gøre det?

#### K-04 - Udvælgelse af relevante målgrupper

Brugere har behov for at finde de rette personer ud fra eksempelvis produkt og rolle, herunder deltagere til arrangementer eller personer med kommunikationsopgaver. Det underliggende behov er at kunne sammensætte en relevant målgruppe; om selve udsendelsen skal ske i relationsplatformen, er ikke afklaret.

**Kilder:** [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#13](https://github.com/OS2sandbox/relations-platform/issues/13), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).  
**Afklaring:** Skal man alene kunne søge og eksportere modtagere, eller også udsende invitationer og meddelelser? Hvordan indgår samspillet med hjemmeside og arrangementer?

#### K-05 - Selvbetjening og løbende ajourføring

Kontaktpersoner har behov for selv at kunne ajourføre relevante oplysninger. Med jævne mellemrum kan en påmindelse gøre opmærksom på behovet for kontrol. Nytten for den enkelte er blandt andet at modtage relevant kommunikation og invitationer.

**Kilder:** [#18](https://github.com/OS2sandbox/relations-platform/issues/18).  
**Afklaring:** Hvad kan den enkelte ændre selv, og hvad kræver kontrol? Hvordan håndteres personer, som forlader deres organisation eller skifter ansvar?

### 3.3 Tværgående sammenhænge

- **Produkter og organisationer:** Oplysninger om produktansvarlige, kontaktpersoner, tilsluttede og interesserede skal kunne anvendes i sammenhæng. Se [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21).
- **Kommunikation og onboarding:** Kontaktoplysninger og roller har betydning ved ansvarsskifte og for at finde alle personer med kommunikationsopgaver. Se [#27](https://github.com/OS2sandbox/relations-platform/issues/27), [#28](https://github.com/OS2sandbox/relations-platform/issues/28).
- **Hjemmeside og arrangementer:** Udvælgelse af målgrupper til arrangementer hænger sammen med annoncering på OS2web, men behøver ikke ligge i samme tekniske løsning. Se [#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#22](https://github.com/OS2sandbox/relations-platform/issues/22).
- **Relationshistorik:** Det skal senere afklares, hvordan tidligere kontakt og dialog knyttes til en person, et emne eller et forløb. Se [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16).

### 3.4 Overlap, som konsolideringen skal håndtere

Kontaktlister ([#13](https://github.com/OS2sandbox/relations-platform/issues/13)), personernes egne oplysninger ([#18](https://github.com/OS2sandbox/relations-platform/issues/18)) og søgning efter målgrupper ([#11](https://github.com/OS2sandbox/relations-platform/issues/11), [#28](https://github.com/OS2sandbox/relations-platform/issues/28)) er indbyrdes afhængige, men ikke identiske. Således kan K-01 være et fælles grundlag for K-04 og K-05, mens K-03 beskriver de rolleoplysninger, der gør kontaktgrundlaget anvendeligt. Formålet er at undgå dobbeltkrav uden at fjerne konkrete anvendelsessituationer fra kilderne.

### 3.5 Åbne spørgsmål til arbejdsgruppen

1. **Person og tilknytninger:** Skal én person kunne optræde på tværs af flere produkter og organisationer med forskellige roller, og hvad betyder det for vedligeholdelsen?
2. **Rolleoplysninger:** Hvilke forskellige roller og typer ansvar er faktisk nødvendige for sekretariatet og produktforvalterne?
3. **Ajourføring:** Hvilke oplysninger skal kunne selvbetjenes, hvem må godkende ændringer, og hvordan kan oplysninger forblive aktuelle ved personaleudskiftning?
4. **Målgrupper:** Skal brugeren alene kunne finde modtagere, eller også foretage udsendelse/tilmelding/opfølgning herfra?
5. **Adgang og indblik:** Hvem skal have adgang til hvilke oplysninger? Det skal afklares, før konkrete systemer vurderes.

**Foreslået første afklaring:** Afprøv behovet for, at samme person kan have flere roller og produkttilknytninger, uden at konkludere på en konkret datamodel eller et bestemt system.

## 4. Øvrige behovsområder - status

Områderne nedenfor er foreløbigt grupperet, men endnu ikke konsolideret på samme niveau som område 1:

- **Relationshistorik, dialog og opfølgning:** [#15](https://github.com/OS2sandbox/relations-platform/issues/15), [#16](https://github.com/OS2sandbox/relations-platform/issues/16), [#17](https://github.com/OS2sandbox/relations-platform/issues/17). Kontaktforløb, emner og opfølgningsbehov.
- **Organisationer, produkter og projekter:** [#20](https://github.com/OS2sandbox/relations-platform/issues/20), [#21](https://github.com/OS2sandbox/relations-platform/issues/21), [#29](https://github.com/OS2sandbox/relations-platform/issues/29). Stamoplysninger, tilslutninger, ansvarlige og tilgængeligt produkt-overblik.
- **Kommunikation og onboarding:** [#24](https://github.com/OS2sandbox/relations-platform/issues/24), [#25](https://github.com/OS2sandbox/relations-platform/issues/25), [#26](https://github.com/OS2sandbox/relations-platform/issues/26), [#27](https://github.com/OS2sandbox/relations-platform/issues/27). Tidlig orientering, opgavefordeling, planlægning og besked ved skift af ansvarlige.
- **Hjemmeside og arrangementer:** [#14](https://github.com/OS2sandbox/relations-platform/issues/14), [#22](https://github.com/OS2sandbox/relations-platform/issues/22). Redigering af produktindhold og oprettelse/annoncering af arrangementer på OS2web.

Til senere afklaring (ikke fase 1):

- **Økonomi, fakturering og regnskab:** [#19](https://github.com/OS2sandbox/relations-platform/issues/19), [#23](https://github.com/OS2sandbox/relations-platform/issues/23). Kræver selvstændig afklaring af arbejdsgange og mulige datakilder.
- **Teknisk videndeling og integrationer:** [#30](https://github.com/OS2sandbox/relations-platform/issues/30). Kræver selvstændig afklaring af omfang og kobling til produktinformation.

## 5. Beslutninger, arbejdshypoteser og ændringshistorik

| Dato | Type | Indhold | Status |
| --- | --- | --- | --- |
| 20.10.2026 | Afgrænsning i arbejdsdialogen | Fase 1 omfatter de fem første behovsområder. Hjemmeside er selvstændigt med kobling til arrangementer. | Aftalt som arbejdsafgrænsning |
| 20.10.2026 | Afgrænsning i arbejdsdialogen | Økonomi og teknisk videndeling fastholdes som selvstændige områder, men indgår ikke i fase 1. | Aftalt som arbejdsafgrænsning |
| 20.10.2026 | Arbejdshypotese | K-01 til K-05 er en mulig konsolidering af kontaktområdet. Person, rolle og tilknytning kan være nyttige begrebsmæssige skel. | Til drøftelse, ikke besluttet |

**Videre arbejdsproces:** Drøft og præcisér de åbne spørgsmål, ret dette dokument via Pull Request, og fortsæt derefter med næste behovsområde. De oprindelige usecases ændres ikke automatisk af konsolideringen. Dokumentet skal kunne efterprøves gennem links til deres GitHub-issues.
