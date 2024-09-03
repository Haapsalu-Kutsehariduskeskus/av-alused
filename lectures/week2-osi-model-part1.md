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
OSI mudel (Open Systems Interconnection Model) on nagu kaart, mis aitab mõista, kuidas andmed liiguvad üle võrgu. See jagab protsessi seitsmeks kihiks, millest igaühel on oma ülesanne. Võite seda võrrelda meeskonnaga, kus iga mängija täidab konkreetset rolli.

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

### 2. Andmekiht: Tagades, et andmed jõuavad sinna, kuhu vaja
- **Andmekihi eesmärk:**
  - See kiht tagab, et andmed liiguvad sujuvalt ühest seadmest teise. See tegeleb andmete pakkimisega nn kaadriteks ja kontrollib vigade esinemist edastuse ajal.

- **Võrgutopoloogiad:**
  - **Topoloogia** on nagu kaart, mis näitab, kuidas erinevad seadmed (näiteks arvutid, printerid ja serverid) on võrgus ühendatud.
    - **Buss-topoloogia:** Kõik seadmed jagavad ühte sideliini. See on lihtne, kuid võib aeglustuda, kui liiga palju seadmeid on ühendatud.
    - **Täht-topoloogia:** Kõik seadmed on ühendatud keskse jaoturiga. Kui jaotur ebaõnnestub, läheb kogu võrk maha.
    - **Ringtopoloogia:** Seadmed on ühendatud ringis. Andmed liiguvad ühes suunas, mis vähendab kokkupõrgete tõenäosust.
    - **Võrgusilm-topoloogia:** Iga seade on ühendatud iga teise seadmega. See on väga usaldusväärne, kuid nõuab palju kaableid ja ühendusi.

![Topoloogia](/lectures/images/topology.png)

- **Andmekihi kaadri struktuur:**
  - Enne võrgu kaudu saatmist jagatakse andmed **kaadriteks**. Kaader koosneb kolmest osast:
    - **Päis:** Sisaldab teavet nagu MAC-aadress (iga seadme unikaalne identifikaator).
    - **Sisu:** Tegelik saadetav teave (näiteks e-kiri või veebileht).
    - **Sabad:** Sisaldab veakontrolli teavet, et tagada andmete õige kohalejõudmine.

![Andmekihi kaader](/lectures/images/data_link.png)

- **Ethernet ja MAC-aadressid:**
  - **Ethernet** on kõige levinum tehnoloogia, mida kasutatakse juhtmega võrkudes. See määratleb, kuidas andmeid kaablite kaudu edastatakse.
  - **MAC-aadress:** Igal võrguseadmel on unikaalne identifikaator, mida nimetatakse MAC-aadressiks. See on nagu postiaadress, mis tagab, et andmed jõuavad õigesse kohta.

 ![MAC-aadress](/lectures/images/mac.png)
