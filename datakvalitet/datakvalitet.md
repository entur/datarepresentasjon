# Datakvalitet

Dette dokumentet beskriver hvilke kvalitetsmål samarbeidet sammen er kommet frem til basert på føringer gitt i DQV-AP-NO, og videre basert på samarbeidets oppfatning av nødvendig eller relevant kvalitetsinformasjon. 


## Beskrivelse av DQV-AP-NO

Norsk applikasjonsprofil av DQV ([DQV-AP-NO](https://data.norge.no/specification/dqv-ap-no)) beskriver hvordan klasser og egenskaper i spesifikasjonen skal brukes for eksempel for datasett, i samsvar med Standard for beskrivelse av datasett, datatjenester og datakataloger ([DCAT-AP-NO](https://data.norge.no/specification/dcat-ap-no)).

DQV har videre en [veileder](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet) for kvantifiserbar kvalitet. Denne er brukt som grunnlag for å etablere de kvantifiserbare kvalitetsmålene beskrevet under. 

Begrepene imputering, enheter og egenskaper brukes i DQV, og tas inn her. 
- Imputering - det å sette inn verdi for en egenskap hvis den mangler eller er ubrukbar ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_imputering))
- Enheter - typisk en rad i en tabell i et datasett ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_enhet))
- Egenskaper - typisk en kolonne i en tabell i et datasett ([DQV definisjon](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_egenskap))


## Beskrivelse av kvalitetsdimensjoner og deldimensjoner

En sammenfattet beskrivelse av dimensjonene er gitt her, mens detaljerte beskrivelser finnes på linkene som peker til [DQV-AP-NO](https://data.norge.no/specification/dqv-ap-no). 

- [Fullstendighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjonen_fullstendighet)
    - Omhandler manglende, overflødige eller imputerte verdier i datasettet. 
        - Underdekning
            - Data som mangler i et datasett
        - Overdekning
            - Data som er med men som ikke skulle være med i et datasett
        - Imputering
            - Å sette inn verdi for en egenskap hvis den mangler eller er ubrukbar
- [Aktualitet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjonen_aktualitet)
    - Beskriver tiden det tar fra hendelsen som genererer informasjonen inntreffer, til informasjonen er tilgjengelig i datasettet.
        - Tidsdifferanse
            - Ferskhet av data uttrykt som differansen mellom to tidspunkter
- [Konsistens](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjonen_konsistens)
    - Beskriver avvik i konsistens mellom egenskaper innad i datasettet. 
    - Eksempelvis et tog der tidspunkt for avreise fra stasjon er tidligere enn tidspunkt for ankomst til samme stasjon.
        - Konsistens innad i datasett
            - Graden av konsistens mellom egenskapene i datasettet
- [Nøyaktighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjonen_n%C3%B8yaktighet "Not working")
    - Beskriver om informasjonen korrekt representerer virkeligheten.
    - Eksempelvis der antall passasjerer på et tog er negativt. 
        - Identifikatorriktighet
            - Graden av at enhetene i datasettet her riktige identifikatorer
        - Klassifikasjonsriktighet
            - Riktigheten til klassifiseringen av enheter eller deres egenskaper sammenlignet med sanne verdier
- Egendefinerte
    - Totale antall enheter
        - Mål på korrekt antall enheter tilgjengelig fra tilbyder
        - Brukes for:
            - å kunne beregne kvalitetsmål som andel av datasettets totale størrelse
            - at konsumenter skal kunne verifisere at de innhenter korrekt antall enheter
    - Duplikater
        - Beskriver antallet enheter i datasettet som er duplikater
            - enten faktiske duplikater der samme enhet er gjengitt flere ganger
            - eller enheter som i praksis er duplikater der informasjonen er den samme, men som eksempelvis har forskjellige id


## Kvalitetsmål

Følgenede verdier er vurdert som relevante å måle som grunnlag for å beskrive et datasetts kvalitetsstatus. 

| Kvalitetsdimensjon | Kvalitetsdeldimensjon | Kvalitetsmål | Kommentarer |
| ------- | ------- | ------- | ------- |
| [Fullstendighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjon_fullstendighet) | [Underdekning](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_underdekning "asd") | [Antall enheter med manglende verdi for en gitt egenskap](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsm%C3%A5l_antall_enheter_med_manglende_verdi_for_en_gitt_egenskap "Not working") | - brukes for alle egenskaper, men må ta hensyn til at det for enkelte egenskaper kan være tillatt med tomme enheter |
| | [Overdekning](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_overdekning) | [Antall overflødige enheter](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsm%C3%A5l_antall_overfl%C3%B8dige_enheter "Not working") | - brukes for alle egenskaper  der det er tillatt med tomme enheter innenfor egenskapen <br /> - der det finnes overflødige verdier bør det fremgå av datasettet hvilke verdier dette gjelder |
| | [Imputering](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_imputering) | [Antall enheter i datasettet med imputert verdi for en gitt egenskap](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsm%C3%A5l_antall_enheter_med_imputert_verdi_for_en_gitt_egenskap "Not working") | - brukes kun der det benyttes imputering innenfor egenskapen <br /> - der det finnes imputert informasjon bør det fremgå av datasettet hvilken informasjon dette gjelder |
| [Aktualitet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjon_aktualitet) | [Tidsdifferanse](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_tidsdifferanse) | [Samlet tidsdifferanse](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsm%C3%A5l_samlet_tidsdifferanse "Not working") - tid mellom når datasettet kan tas i bruk og den hendelsen eller fenomenet datasettet beskriver inntreffer | - beskrives normalt for datasettet generelt |
| [Konsistens](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjon_konsistens) | [Konsistens innad i datasettet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_konsistens_innad_i_datasett) | Antall enheter med inkonsistene verdier på tvers av sammenhengende egenskaper. | - utvalg av egenskaper som skal vurderes i sammenheng avhenger i stor grad av kjennskap til datasettet og domenekunnskap |
| [Nøyaktighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdimensjon_n%C3%B8yaktighet "Not working") | [Identifikatorriktighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_identifikatorriktighet) |  |  |
|  | [Klassifikasjonsriktighet](https://data.norge.no/guide/veileder-kvantifiserbar-kvalitet#_kvalitetsdeldimensjon_klassifikasjonsriktighet) | Antall enheter der informasjonen ikke representerer virkeligheten. | - brukes kun der det er mulig å avgrense hva som er virkeligheten <br /> - der det finnes unøyaktig informasjon bør det fremgå av datasettet hvilken informasjon dette gjelder |
| Egendefinerte | Totale antall enheter | Totalt antall enheter - i datasettet og innenfor logiske grupperinger. | - logiske grupperinger kan eksempelvis være per dag, per rute, eller lignende |
|  | Duplikater | Antall enheter som er duplikater. | - der det finnes duplikater bør det fremgå av datasettet hvilke enheter dette gjelder |



## Gjennomføring

For levende datasett anbefales det at kvalitetsanalyser gjennomføres regelmessig for å kunne følge med på eventuelle endringer i kvalitet over tid.
- for eksempel daglige, ukentlige eller månedlige kvalitetsanalyser

For statiske datasett gjennomføres kvalitetsanalyser i forbindelse med tilgjengeliggjøring, og ved eventuelle endringer i datasettet. 

## Presentasjon av kvalitetsresultater

Oppsett for presentasjon av kvalitetsresultater er beskrevet i REF. Kvalitetsmålene som er beskrevet over legger til rette for å presentere både absolutte antall, og andeler av en total eller et utvalg. Videre også som kvalitetsutvikling over tid for levende datasett. 