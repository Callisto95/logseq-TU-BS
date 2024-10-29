- Aufgabe 2 (Absorptionsgesetze)
	- seien $P,Q$ Aussagevariablen (AV): Zeige, dass gilt: $P\lor(P\land Q)\sim P\sim P\land(P\lor Q)$
	- via Aussagetabelle:
	- |$P$|$Q$|$P\land Q$|$P\lor(P\land Q)$|$P\lor Q$|$P\land(P\lor Q)$|
	  |--|--|--|--|--|--|
	  |1|1|1|1|1|1|
	  |1|0|0|1|1|1|
	  |0|1|0|0|1|0|
	  |0|1|0|0|0|0|
-
- Aufgabe 3 (Vorlesungsbemerkung 1.14)
	- jeder Junktor lässt sich äquivalent durch $\land$ und $\neg$ darstellen
	- $P_1,P_2,...,P_{n}$ feste Anzahl and AV's
	- $\#$ Junktor, der n AV einen Wert zuteilt
	-
	- $Q_1=P_1\land P_2\land...\land P_{n-1}\land P_{n}=\#$
	- $Q_2=P_1\land P_2\land...\land P_{n-1}\land\neg P_{n}=\#$
	- $Q_3=P_1\land P_2\land...\land\neg P_{n-1}\land P_{n}=\#$
	- $Q_4=P_1\land P_2\land...\land\neg P_{n-1}\land\neg P_{n}=\#$
		- $\#$ als undefinierter Junktor
	- => Verknüpfung der AV's durch $\land$ und $\neg$, sodass eine wahre Aussage entsteht
	- Kombination von $Q_{i},...,Q_{2^{n}}$ mit $\lor$
	- $\#\sim Q_1\lor...\lor Q_{2^{n}}\sim\neg\widetilde{Q_1}\land...\land\neg\widetilde{Q_{2^{n}}}$
	- -> Nutzung der *Morganschen Regel*: $\neg(P\land Q)\sim\neg P\lor\neg Q$
	- Dabei ist $Q_{i}=\widetilde{Q_{i}}$ wenn $\#$ in der i-ten Zeile falsch ist und $Q_{i}=\neg Q_{i}$ im anderen Fall
	- Daher $\#\sim\neg(\widetilde{Q_1}\land...\land\widetilde{Q_{2^{n}}})$
	-
-