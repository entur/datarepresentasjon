# Prinsipper for deling av data

Dette dokumentet inneholder samarbeidets prinsipper for deling av data, som representerer samarbeidets felles enighet om hvilke rammer som skal ligge til grunn for videre arbeid med mer detaljerte standarder og anbefalinger. Disse prinsippene er derfor etablert for å sikre en felles enighet i samarbeidet på konseptuelt eller overordnet nivå.

Prinsippene vil innledningsvis revideres kvartalsvis i regi av prosjektet basert på samarbeidets innspill. 

## G. Generelle prinsipper

| Punkt | Tema | Prinsipp |
| ------- | ------- | ------- |
| G.1 | Forpliktelse | Virksomhetene bør etterstrebe å følge prinsippene som er beskrevet her, og detaljert ut som en del av samarbeidet. Der man må avvike fra prinsippene, skal det ikke være et hinder eller begrensning for å dele data. |
| G.2 | Målgruppe | Arbeidet som gjøres innen tilrettelegging for deling av data skal ha konsumentene i fokus, med mål om at flest mulig skal kunne finne, innhente, forstå og ta i bruk datasett. Samtidig skal arbeidet ta hensyn til de involverte virksomhetenes kapasitet og evne til å implementere den tilretteleggingen det legges opp til. |
| G.3 | Datasett | Det skal jobbes mot at all data som kan ha relevans utenfor egen virksomhet skal deles, fortrinnsvis som åpne data. For data som er begrenset av GDPR- eller konkurransehensyn, eller av andre grunner ikke er klare for å deles, skal informasjonen om dataene deles. |

## DA. Design- og arkitekturprinsipper

| Punkt | Tema | Prinsipp |
| ------- | ------- | ------- |
| DA.1 | Autonomi | Hver virksomhet står fritt i valget av interne komponenter, teknologi, standarder og delingsmekanismer. Samarbeidet kan tilrettelegge for enklere deling eller bruk ved å lage standardkomponenter for et utvalg teknologier, delingsmekanismer eller ligndende. |
| DA.2 | Tilgangsstyring | Der virksomhetene ønsker å dele tilgangsstyrt data, må utveksling av tilgangsstyring støtte ~~openapi-spec som prosjektet skal lage~~. Virksomhetene som får tilgang til uthenting av tilgangsstyrt data må sikre uthentingsmekanismene og eventuelt uthentet data i egen infrastruktur i henhold til juridiske avtaler. Samarbeidet støtter opp under deling av tilgangsstyrt data ved å tilby eksempler på implementasjon og sdk'er som kan taes i bruk for uthenting.|
| DA.3 | Intern data og ekstern data  | Virksomhetene bør dele opp internt slik at data som deles er adskilt fra intern data. På denne måten kan dataelementene utvikle seg uavhengig av hverandre og sikre kompatibilitet eksternt, uten hverken å eksponere eller låse ned interne data. |
| DA.4 | Datakatalog | Virksomhetene må informere om nye etablerte datasett som skal deles og tilgjengeliggjøre korrekt metadata for datakatalog. Samarbeidet bør tilby mekanismer som gjør dette på en så enkel og automatisert måte som mulig. |


## S. Standardisering

| Punkt | Tema | Prinsipp |
| ------- | ------- | ------- |
| S.1 | Fellestrekk | Gjennom standardiseringen skal det etableres tydelige og relevante fellestrekk på tvers av datasett fra ulike tilbydere for å gjøre det enklere å forstå datasett, og ta i bruk datasett på tvers av tilbydere. |
| S.2 | Datadata | Samarbeidet skal jobbe mot at innholdet i alle datasett skal følge en datastandard, fortrinnsvis etablerte standarder dataene naturlig hører til. For data som faller utenom dette skal det jobbes mot at innholdet følger en minimumsstandard samarbeidet etablerer med utgangspunkt i anerkjente nasjonale eller internasjonale standarder. (datoer, koordinater, SI-enheter) |
| S.3 | Distribusjoner | Samarbeidet skal jobbe mot at datasett deles gjennom like distribusjoner for like datasett. Samarbeidet kan definere noen distribusjoner eller formater som har tilgjengeliggjort mer automasjon. |
| S.4 | Tilgangsnivåer | Vurdering av tilgangsnivå skal følge en enhetlig praksis for samarbeidet der målet er at lik data vurderes likt på tvers av virksomhetene. Ved forskjellige vurderinger skal virksomhetene søke å finne en felles praksis. |
| S.5 | Beskrivelser | Samarbeidet skal jobbe mot at informasjonen som gis med et datasett skal være enhetlig strukturert, og sikre at forskjellige roller på konsumentsiden får nødvendig informasjon til å la seg inspirere av eller ta i bruk datasettet. Informasjonen som gis skal være tilstrekkelig til at datasettets innhold og kvalitet er kjent ved bruk. |
| S.6 | Koblinger | Samarbeidet skal jobbe for å knytte datasett tettere sammen, gjennom arbeid med informasjonsmodeller på tvers, felles begrepsbruk og dataopphav. |
| S.7 | Innhold | Samarbeidet skal jobbe mot at datasettene som deles skal gi så høy verdi som mulig for så mange som mulig, gjennom å tilrettelegge for tilpassede alternativer. |

