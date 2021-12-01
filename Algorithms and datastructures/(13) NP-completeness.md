#TOC  

# (13) NP-completeness
*NP er klassen av ja-nei-problmer der ethvert ja-svar har et bevis som kan sjekkes i polynomisk tid. Alt i NP kan i polynomisk tid reduseres til såkalt komplette problemer i NP. Dermed kan ikke disse løses i polynomsik tid, med mindre alt i NP kan det.* 
## Reduksjon
- Vil beskrive problemers vanskegrad
	- Dvs. vise at problem kan løses/ikke kan løses i polynomisk tid
- Sammenligner problemer
	- Om et problem er minst like vansklig som et annet

Her er det viktig holde styr på hvilken retning man reduserer i. 

| Direction                                  | Implication           |
| ------------------------------------------ | --------------------- |
| $(A) = NP_{complete} \rightarrow B= NP$    | B is  $NP_{complete}$ |
| $(A) = NP \rightarrow (B) = NP_{complete}$ | Viser ingenting, alle NP-problmer kan reduseres til NP-complete                      |

### Diverse eksempler
#### Kistene
Vi har i dette eksempelet redusert problemet
"åpne A" til "åpne B" ettersom det ikke kan være vanskeligere å åpne A enn det er å åpne B
![[Pasted image 20211115150035.png]]

#### Finne en kort sti kortere enn k
Reduseres til å finne den korteste stien

**Lærer oss: ** *Besluting er ikke vanskeligere enn optimering (og lignende)*

### Viktige saker
![[Pasted image 20211115150519.png]]
*Nei, om A reduserer til et løsbart problem må A også være løsbart!*

---

![[Pasted image 20211115150631.png]]
*Akkurat som vi så må kiste eksempelet*

---

![[Pasted image 20211115150722.png]]
*Ettersom $\alpha \le \beta$, og vi snakker om eksponensiell, som er en nedre grense*
![[Pasted image 20211115150843.png]]


---

#### Hamilton krets eksempelet
- Hamilton krets er komplett NP-problem --> Ikke løst enda

**Spm**: *Er det mulig å finne ut om en graf har en vei som er lengre enn en gitt verdi?*
**Svar:** *Nei, fordi vi kan løse Hamiliton problemet om vi finner en slik algoritme*

- Kan redusere HAM-CYCLE til LONG-PATH i polynomisk tid
	- HAM-CYCLE kan ikke være vanskeligere
- Motsatt retning er ikke spesielt interessant

## Verifikasjon
- ==NP== (nondeterministically polynomial)
	- Problemer der en løsning kan verifiseres i polynomisk tid
		- **Betyr:** Om jeg får et ja-svar fra deg på en påstand, må jeg kunne verifisere i polynomisk tid deterministisk
- Co-NP: Motsatt fra NP, med sertifikat for nei-svar
- Det er lett å verifisere, kan være umulig å finne
## Kompletthet
- Vi har et univers av problemer og vi kan sammenligne dem
- Gir opphav til et sett maksimalt vanskelige problemer
- Kalles ==Komplette== for klassen NP under polynomiske reduksjoner

---
$NP_{komplett}(a) \rightarrow_{(redusere)} NP_{Lettere} (b)$

$\Rightarrow$ b må  være NP-komplett

---

==NP-hard==: Alt som er minst like vanskelige som alt i NP

## Encodings
**Concrete problem:** A problem whose instance set is the set of binary string

## NP-complete problems
[[CIRCUIT-SAT]]
[[SAT]]
[[3-CNF-SAT]]
[[CLIQUE]]
[[VERTEX-COVER]]
[[HAM-CYCLE]]
[[TSP]]
[[SUBSET-SUM]]


## Sammendrag ish
![[Pasted image 20211201162435.png]]
**Blå:** *p problemer*
**Snitt med Rød:** *npc problemer*
**Grønn:** *np problemer*