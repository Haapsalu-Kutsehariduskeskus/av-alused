<div class="small-grey-box">
  <div class="small-heading">Module 4: Physical Layer</div>
  - <a href="https://www.youtube.com/watch?v=AHV54tqhZU0&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=6">Physical Layer</a>

  <div class="small-heading">Module 5: Number Systems</div>
  - <a href="https://www.youtube.com/watch?v=RdoxJsWzFKc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=7">Number Systems</a>

  <div class="small-heading">Module 6: Data Link Layer</div>
  - <a href="https://www.youtube.com/watch?v=eK4s5TQm45c&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=8">Data Link Layer</a>
  
  <div class="small-heading">Module 7: Ethernet Switching</div>
  - <a href="https://www.youtube.com/watch?v=KWm7_vsfdE4&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=9">Ethernet Switching</a>

</div>

# Nädal 2: OSI mudeli mõistmine - Osa 1 (Füüsiline ja andmekiht)

### Sissejuhatus OSI mudelisse
OSI mudel (Open Systems Interconnection Model) on nagu kaart, mis aitab mõista, kuidas andmed liiguvad üle võrgu. See jagab protsessi seitsmeks kihiks, millest igaühel on oma ülesanne. Võite seda võrrelda meeskonnaga, kus iga mängija täidab konkreetset rolli. OSI mudelist sai peamine mudel, mida ettevõtted järgivad toodete ja protokollide (reeglid, kuidas võrgud töötavad) loomisel.


Selles sessioonis keskendume kahele kihile:
1. **Füüsiline kiht**
2. **Andmekiht**

### 1. Füüsiline kiht: Võrgu aluspõhi

- **Mida teeb füüsiline kiht?**
  - See on kiht, kus toimub kõik füüsiline. See käsitleb riistvara—kaablid, juhtmed ja signaalid, mis kannavad andmeid ühest seadmest teise.

  **Näited:** Kaablid, pistikud, elektrilised pinged, füüsilised võrgutopoloogiad.
  **Selles kihis olulised kontseptsioonid:** RS-232, RJ45, V.34, 100BASE-TX, SDH, DSL, 802.11.
  
  **Füüsiline kiht lihtsustatult:** Lihtsustatult öeldes vastutab see kiht andmete (nullide ja ühtede) edastamise eest kaablite kaudu, kasutades elektrilisi signaale (keerdpaarid) või valgust (optilised kaablid).

- **Edastuskandjate mõistmine:**
  - **Edastuskandjad** on füüsilised rajad, mööda mida andmed liiguvad. Neid on erinevat tüüpi, igaühel on oma tugevused ja nõrkused:
    - **Vaskkaablid:** Need on nagu andmete teed juhtmega võrgus.
      - **Varjestamata keerdpaar (UTP) kaabel:** Kõige levinum võrgu kaabli tüüp, mida kasutatakse paljudes kodudes ja kontorites. See on valmistatud keerdpaari juhtmetest, et vähendada häireid teistest signaalidest.
    - **Fiiberoptilised kaablid:** Need kasutavad andmete edastamiseks elektri asemel valgust, võimaldades ülikiiret ja kauglevi kommunikatsiooni.
      - **Eelised:** Kiirem ja usaldusväärsem kui vask, kuid kallim.
    - **Juhtmevaba meedia:** Siia kuuluvad Wi-Fi ja Bluetooth. See on nagu andmete saatmine läbi õhu ilma füüsiliste kaabliteta.
      - **Eelised:** Ei vaja kaableid; seadmeid on lihtsam liigutada.
      - **Väljakutsed:** Võivad mõjutada seinad ja muud takistused, mis põhjustavad aeglasemat kiirust või katkestatud ühendusi.

![Füüsiline kiht](/lectures/images/physical_layer.png)

- **Binaar- ja kuueteistkümnendjärgu mõistmine:**
  - Arvutid suhtlevad binaarkoodis (1-d ja 0-d). Iga andmeühik, olgu see tekstisõnum või YouTube'i video, on jaotatud binaariks.
  - **Binaari näide:** Number 2 binaaris on `10`.
  - Mõnikord esitatakse andmeid ka kuueteistkümnendsüsteemis (base-16), mis on inimeste jaoks lihtsam lugeda kui pikad binaarjadad.
  - **Kuueteistkümnendsüsteemi näide:** Binaararv `1010` on kuueteistkümnendsüsteemis `A`.

  ![Binaar](/lectures/images/binary.png)

### 2. Andmekihi kaadri struktuur

OSI mudeli alumine kiht pakub teenuseid ülemisele kihile. See tähendab, et alumised kihid tegelevad üldisemate asjadega, samas kui ülemised kihid tegelevad spetsiifilisemate probleemidega. Võib öelda, et alumine kiht loob aluse ülemisele kihile. Näiteks esimene kiht, füüsiline kiht, vastutab bittide (väikseimad andmeüksused) liikumise eest kanalikihti, mis tegeleb juba edasi nende andmete edastamisega. Kanalikiht ei pea enam muretsema bittide kujutamise pärast, sest füüsiline kiht on selle töö ära teinud.

Kui andmed liiguvad arvutiprogrammist võrku, läbivad need OSI mudeli kihid ükshaaval. See tähendab, et iga kiht lisab andmetele oma spetsiaalse info, mida nimetatakse päiseks. Näiteks rakenduskiht valmistab andmed ette, kodeerides need sobivasse vormi. Siis lisab seansikiht info seansi kohta ja saadab need transpordikihile, mis jagab andmed vajadusel väiksemateks osadeks ja lisab päisesse aadressid. Järgmisena võtab võrgu kiht andmed vastu, pakib need kokku ja saadab füüsilisele kihile, mis muundab andmed signaalideks ja saadab need füüsilist teed pidi kohale.

Kui andmed jõuavad sihtkohta, võtavad kihid need vastu vastupidises järjekorras, iga kiht eemaldab oma päise, kuni andmed jõuavad rakenduseni. Selle protsessi käigus nimetatakse andmeid protokolli andmeüksuseks (PDU).

OSI mudeli kasutamisest on mitmeid eeliseid, näiteks:

	•	Keerukuse vähenemine.
	•	Tehnoloogiate koostalitlusvõime tagamine.
	•	Kiirem areng ja standardiseerimine.
	•	Õppimise lihtsustamine.

Ülemise kihi andmed muutuvad siis, kui need liiguvad läbi teiste kihtide, ja igal kihil on oma roll andmete töötlemisel.











- **Ethernet ja MAC-aadressid:**
  - **Ethernet** on kõige levinum tehnoloogia, mida kasutatakse juhtmega võrkudes. See määratleb, kuidas andmeid kaablite kaudu edastatakse.
  - **MAC-aadress:** Igal võrguseadmel on unikaalne identifikaator, mida nimetatakse MAC-aadressiks. See on nagu postiaadress, mis tagab, et andmed jõuavad õigesse kohta.

 ![MAC-aadress](/lectures/images/mac.png)
