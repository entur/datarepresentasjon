# Datakvalitet

Dette dokumentet beskriver hvilke kvalitetsmål samarbeidet sammen er kommet frem til basert på føringer gitt i DQV-AP-NO, og videre basert på samarbeidets oppfatning av nødvendig eller relevant kvalitetsinformasjon. 


## DQV-AP-NO

Norsk applikasjonsprofil av DQV ([DQV-AP-NO](https://data.norge.no/specification/dqv-ap-no)) beskriver hvordan klasser og egenskaper i spesifikasjonen skal brukes for eksempelvis for datasett, i samsvar med Standard for beskrivelse av datasett, datatjenester og datakataloger ([DCAT-AP-NO](https://data.norge.no/specification/dcat-ap-no)).

DQV har videre en [veileder](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet) for kvantifiserbar kvalitet. Denne er brukt som grunnlag for å etablere de kvantifiserbare kvalitetsmålene. 

Begrepene imputering, enheter og egenskaper brukes i DQV, og tas inn her. 
- Imputering - det å sette inn verdi for en egenskap hvis den mangler eller er ubrukbar ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_imputering))
- Enheter - typisk en rad i en tabell i et datasett ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_enhet))
- Egenskaper - typisk en kolonne i en tabell i et datasett ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_egenskap))


## Kvalitetsmål

### Kvalitetsmetrikker

Samarbeidet tar utgangspunkt i kvalitetsmetrikkene fra DQV for beskrivelse av kvalitet. 

#### Fullstendighet
Omhandler manglende, overflødig eller imputert informasjon i datasettet. 

##### Underdekning
- Måles: antall enheter med manglende informasjon for hver enkelt egenskap
    - brukes for alle egenskaper, men må ta hensyn til at det for enkelte egenskaper kan være tillatt med tomme enheter

##### Overdekning
- Måles: antall enheter med overflødig informasjon for hver enkelt egenskap
    - brukes kun der det er tillatt med tomme enheter innenfor egenskapen
    - der det finnes overflødig informasjon bør det fremgå av datasettet hvilken informasjon dette gjelder

##### Imputering
- Måles: antall enheter med imputert informasjon for hver enkelt egenskap
    - brukes kun der det benyttes imputering innenfor egenskapen
    - der det finnes imputert informasjon bør det fremgå av datasettet hvilken informasjon dette gjelder

#### Aktualitet
Beskriver tiden det tar fra hendelsen som genererer informasjonen inntreffer, til informasjonen er tilgjengelig i datasettet.

- Beskrives normalt for datasettet generelt. 

#### Konsistent
Beskriver avvik i konsistens mellom egenskaper innad i datasettet. 
- Eksempelvis et tog der tidspunkt for avreise fra stasjon er tidligere enn tidspunkt for ankomst til samme stasjon.
- Måles: antall enheter med inkonsistent informasjon på tvers av sammenhengende egenskaper
    - utvalg av egenskaper som skal vurderes i sammenheng avhenger i stor grad av kjennskap til datasettet og domenekunnskap

#### Nøyaktighet
Beskriver om informasjonen korrekt representerer virkeligheten.
- Eksempelvis der antall passasjerer på et tog er negativt. 
- Måles: antall enheter der informasjonen ikke representerer virkeligheten
    - brukes kun der det er mulig å avgrense hva som er virkeligheten
    - der det finnes unøyaktig informasjon bør det fremgå av datasettet hvilken informasjon dette gjelder


### Øvrige målepunkter

#### Totale enheter i datasettet
Det totale antallet enheter i datasettet bør måles
- for å kunne beregne kvalitetsmål som andel av datasettets totale størrelse
- for at konsumenter skal kunne verifisere at de innhenter korrekt antall enheter

- Måles: totalt antall enheter i datasettet og innenfor logiske grupperinger
    - logiske grupperinger kan eksempelvis være per dag, per rute, eller lignende. 

#### Duplikater
Beskriver antallet enheter i datasettet som er duplikater
- enten faktiske duplikater der samme enhet er gjengitt flere ganger
- eller enheter som i praksis er duplikater der informasjonen er den samme, men som eksempelvis har forskjellige id

- Måles: antall enheter som er duplikater
    - der det finnes duplikater bør det fremgå av datasettet hvilke enheter dette gjelder

### Gjennomføring

For levende datasett anbefales det at kvalitetsanalyser gjennomføres regelmessig for å kunne følge med på eventuelle endringer i kvalitet over tid.
- for eksempel daglige, ukentlige eller månedlige kvalitetsanalyser