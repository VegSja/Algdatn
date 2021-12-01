# Eksamen H2020

## Oppgave 1 - Huffmann
Huffmann algoritmen er en komprimeringsalgoritme som har som mål å minimere hvor mye plass en sekvens med bokstaver tar opp i minnet på en datamaskin. Algoritmen bruker en tabell som sier noe om hvor ofte hver bokstav forekommer i en tekststreng. Bruker dermed dette til å representere bokstavene som en binær streng. Disse binære kodene kan enten være av fast størrelse, eller variere. Med sistnevnte kan man kode bokstavene slik at bokstaver med høy forekomst har en mindre bit streng.

Vi ser bare på koder som ikke er en prefix for et annet kodeord, så kalte prefiks koder. Disse gjør det lettere å dekode koden senere, ettersom vi kan dele opp en binærstreng til de individuelle bokstavene. For å bidra i dekodingsprosessen representerer vi prefiks kodene med et binært tre. Hvor "0" betyr gå til venstre "1" betyr gå til høyre. Ved å finne simple path fra roten til løvnoden og notere hvilken retning man går kan man dermed dekode en huffmankode

For å bygge et sånt tre antar vi at vi har optimal substructure. Vi representerer alle bokstavene som noder som også inneholder data på hvor mange av gitte bokstav som eksisterer. Dermed tar vi grådige valg og setter alltid sammen trær som skaper lavest mulig sum på rot noden. Til slutt vil vi da ha en huffmankode i form av et tre


## Oppgave 2
Vi har primært 2 algoritmer for å velge hvilken kant vi skal ha over et snitt i en slik skog/tre
**Kruskals**: Sier at man skal velge grådig den kanten med lavest vekt over snittet så lenge dette ikke er med på å forme en sykel. Velger ved å traversere grafen for å finne ut om vi har sykler. 

Det er åpenbart at man må velge en kant som ikke skaper sykler, ettersom et MST er et tree, og kan derfor ikke inneholde sykler. Så hver gang man gjør et valg som ikke skaper sykler og man velger kanten med minst vekt, så vil invarianten at grafen er et subset av et MST være sann. Tilslutt vil vi dermed ha en MST

**Prims algoritme** : Sier at man skal velge den minste kanten som vil kobles til treet og at denne alltid er sikker. Kan implementeres med min-Prioritetskø.

Her er det mye samme tankegang som kruskals med at vi skal bevare invarianten for hvert valg. Ved å velge en kant som er med på å utvide treet hindrer vi dannelsen av løkker. Dette er derfor et trygt valg

Altså hovedforskjellen på disse algoritmene vil være at Kruskals kan forme skoger og koble de sammen tilslutt, mens Prims heller setter sammen et tre med en gang

## Oppgave 3

## Oppgave 4
Et binært søketree vil definitivt være raskere enn å måtte iterere over listen hver gang for å finne høyeste element. Da trenger hun kun å lage et binært søketre på starten av algoritmen (vil bare ta $\Theta(n*lg(n))$ tid. Problemet hennes vil være å finne fram til elementer her. Det vil ta $\Theta(lgn)$ tid for hvert element, så kjøretiden blir $O(2n*lgn)$. En måte som kunne minimert denne kjøretiden er å heller lage en max-heap ($O(n)$) og hente ut max elementene ved å poppe ut(fjerne An). Dette er heapsort. 

## Oppgave 5
Ettersom vi har 2 problemer maks per iterasjon, og disse to er begge avhengige av en løsning på forrige delinstans, vil jeg anslå at kjøretiden blir O(n)

Ser at det er flere overlappende subproblemer her som ikke trenger å løses mer enn en gang. Vi har også en optimal substruktur ved at ved å få optimale løsninger på delproblemene så vil vi kunne få en optimal løsning på problemet i en helhet. Dette er et problem som kan løses med dynamisk programmering, mer fast bestemt ville jeg brukt memoization. Det går ut på at man utfører delproblemene og lagrer resultatet, slik at hvis et annet delproblem er avhengig av denne løsning så kan den hente fram løsningen fra minnet istendefor å måtte kalkurere dette på nytt. Da får vi at for hver gang 2 delproblemer er avhengige av den tidligere delproblemet, så trenger man ikke å beregne denne på nytt. Da får man effektivt at man løser 1 problem, så 2, så 1 problem, så 2. Dette fører til at vi får asymptotisk samme tidskompleksitet men konstatnene minker.

## Oppgave 6
Quicksort baserer seg på valg av et pivot element. Quicksort benytter seg av prosessen PARTITION, som velger siste element i lista som pivot element. Deretter itrerer den over lista og plasserer elementer mindre enn pivot i `[0,i]` og større i `[i,j]`. Inkrementerer j og plasserer etter hva den støter på. Når dette er ferdig bytter pivotelementet plass med element på plass i+1. Da står pivot elementet på sin riktige plass. Deretter gjøres det samme rekursivt på lista til alle elementer står på riktig plass. 

Randomized quicksort velger rett og slett pivot element tilfeldig og bytter plass på siste element og pivotelementet før den kjører samme prosedyre som quicksort. Dette gjør at man gjennomsnittlig gjør like mange dårlige valg og gode valg. Dermed får man gjennomsnittlig kjøretid på $\Theta(nlgn)$

