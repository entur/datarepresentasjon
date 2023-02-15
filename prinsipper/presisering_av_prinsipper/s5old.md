# S.5 - Beskrivelser

## Prinsipptekst

> Samarbeidet skal jobbe mot at informasjonen som gis med et ~~datasett~~ dataprodukt skal være enhetlig strukturert, og sikre at forskjellige roller på konsumentsiden får nødvendig informasjon til å la seg inspirere av eller *gå videre med å* ta i bruk dataprodukt. ~~Informasjonen som gis skal være tilstrekkelig til at datasettets innhold og kvalitet er kjent ved bruk.~~ Informasjonen som gies som metadata skal kommunisere tydelig hvem som er dataeier, nyttige kvalitetsdimensjoner og relevante beskrivelsesfelter.

## Ordliste

Dataprodukt er bestå av en eller flere ressurs, feks autopass_passeringer. En ressurs representerer et del av dataproduktet, feks autopass_passeringer_passeringspunkter og autopass_passeringer_bilpassering. En distribusjon kan være en tabell, en fil, en strøm, et api som representerer ressursen likt på tvers av distribusjoner. 

Tilgangsstyring og dataeierskap skjer på dataprodukt-nivå.

## Presiseringer

### "informasjonen [..] skal være enhetlig strukturert"
Med enhetlig strukturert informasjon menes at dokumentasjonen og beskrivelsene som gis inneholder de samme informasjonselementene og er strukturert på samme måte, uavhengig av tilbyder. Videre at innholdet i hvert informasjonselement beskriver de samme tingene. 

### "forskjellige roller på konsumentsiden"
Med forskjellige roller menes eksempelvis utviklere, dataingeniører, analytikere, ledelse, mm. 

### "Informasjonen som gies som metadata skal kommunisere tydelig hvem som er dataeier"

Eierskap på dataproduktet skal være en person

- Markering "Esksprimenell" eller "Stabil" og hva det betyr
- Kontaktperson eller epost til griuppe
- Normer å svare på henvendelser innen 3 virkedager på epost 

### "Informasjonen som gies som metadata skal kommunisere tydelig [..] relevante beskrivelsesfelter"

Vi anbefaler at man publiserer informasjon om kolonner, datatyper i ressurssen. I tillegg ønsker vi at det publiseres en eller flere [eksempeldata i playground](https://github.com/entur/sd-playground) pr ressurs. Dersom dataproduktet ikke er åpent tilgjengelig, forventer vi noen eksempelrader, enten med ekte eller syntetisk data.

For tilgang til playground ta kontakt med prosjektet. 

Relevante beskrivelsesfelter på dataproduktnivå er [..]

Relevante beskrivelsesfelter på ressursnivå er [..]


#### Domenekunnskap 

Prosjektet ser et behov for å kunne dokumentere og beskrive domenekunnskap som er viktig for å forså og bruke informasjonen på riktig måte. Dette er ikke en del av prinsippene pt, men vi anbefaler en at tekstlig beskrivelse bør legges til for å dekke opp dette hullet. Her mener vi at det ikke er nyttig å se etter fellestrekk på tvers ettersom det er eksplisitt domenekkunnskap som sitter hos tilbyder. 


### Informasjonen som gies som metadata skal kommunisere [..] nyttige kvalitetsdimensjoner
Målet er å gi en omtrentlig forståelse av datakvaliteten i dataproduktet, slik at roller på konsumentsiden kan vurdere om de vil gå videre for å få tilgang til dataen. Følgede dimensjoner bør beskrives tekstlig eller kvantitativt;

- Aktualitet (Tidsdifferanse): Beskriver tiden det tar fra hendelsen som genererer informasjonen inntreffer, til informasjonen er tilgjengelig i datasettet.

- Egendefinert
  - For data innenfor APC-domenet har vi sett at følgende dimensjon er nyttig
    - Dekningsgrad på APC-utstyr
    - Antatt nøyaktighet på sensorer (for eksempel om påstigninger plukkes lettere opp enn avstigninger ) 

Prosjektet tar ikke som mål å levere på operativ datakvalitet for kontinuerlig overvåking ettersom prosjektet ikke har tilgang på datasettene som skal evalueres. Dette kan endre seg i fremtidem til at tilbydere anbefales å publisere jevnlige datakvalitetsmålinger sammen med metadata om et datasett. 

- Dimensjoner på hvilke ressurssnivå