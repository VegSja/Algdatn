#todo 

# CIRCUIT-SAT
**Instans**: En krets med logiske proter og en utverdi
**Spørsmål**: Kan utverdien bli 1?

![[Pasted image 20211201160452.png]]

- Lager på en måte en simulering av en verifiksasjonsalgoritme med kretsen
	- Output: Svar til verifikasjonsalgoritmen
	- Input: Graf og sti (instans og sertifikat)
		- Kan låse grafen (ved å bare sette 1 her)
		- Sender bare inn sertifikatet
			- Finnes det da en utverdi 1?
				- Samme som å si: *Finnes det et sertifikat/sti som gjør at verifikasjonsalgoritmen sier ja*
					- Svaret er bare ja om svaret på breslutningsproblemet er ja
					- Om vi løser dette problemet har vi også løst hvilket som helst annet problem som har en verifikasjonsalgoritme
						- Må derfor være NP komplett



## References