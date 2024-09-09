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

Sidevõrkudes kasutatakse füüsiliste ja loogiliste struktuuride loomiseks erinevaid sideüksusi. Saadaval on kolme gruppi sideüksusi:

**Passiivsed üksused**

assiivsed üksused on sidevõrgu ühenduspunktid, mis ei muuda sisendisse saabuva signaali parameetreid. See üksuste grupp sisaldab:

Ühenduspistikud (Jack couplers) on passiivsed üksused, mida kasutatakse võrgukaabli pikendamiseks.
 ![Ühenduspistiku pesad](/lectures/images/jackcouplers.png)
  Seinapistik (wall plate) on ühenduspaneel ühe tööjaama jaoks, millel on tavaliselt üks või kaks porti. Portidesse on võimalik asetada pesasid RJ-45 või RJ-11 tüüpi otsadele.

Juhtmepaneel (Patch panel) on ühendus- ja jaotuspunkt kaablite korraldamiseks.

Passiivne kontsentraator/jaotur (passive concentrator/hub) (Joonis 3.5, paremal) on keskne ühenduskolmik, mille abil luuakse ühendus hulga tööjaamade vahel. See ei sisalda elektroonilisi komponente ega vaja seega elektritoidet. Suvalisse porti saabuv sisendsignaal edastatakse kõigisse teistesse portidesse.
 ![Passivne jaotur](/lectures/images/patchpanel.png)
 
 **Aktiivsed seadmed**

Aktiivsed seadmed võimendavad ja muudavad signaale, et need saaksid liikuda pikematel vahemaadel või erinevatel kaablitel.

- **Ülekandemeediumi konverterid** (näiteks adapterid): Need seadmed ühendavad kaks erinevat tüüpi kaableid, näiteks ühendavad UTP-kaablivõrgu valguskaablivõrguga.

- **Repiiter**: 
  - See töötab füüsilisel tasandil ja aitab signaale võimendada, et need jõuaksid kaugemale.
  - Repiiter ei vali, milliseid signaale võimendada – see taastab nii kasulikud andmed kui ka müra.
  - Seda kasutatakse kahe sama tüüpi võrgusegmendi ühendamiseks ja signaalide tugevdamiseks.

- **Hub (jaotur)**:
  - See on seade, millel on mitu sisendit ja mis ühendab tööjaamad (arvutid) omavahel.
  - **Olulised omadused:**
    - See ühendab mitu tööjaama ja moodustab neist ühe võrgu.
    - Hube kasutatakse UTP-kaablivõrkudes.
    - Hub ei salvesta andmeid, nii et andmevahetuskiirus võib olla madalam.
    - Kui port on rikkis, võib hub selle välja lülitada.
    - Kõik ühendatud pordid on võrdse prioriteediga ja hub ei suuda kohandada kiirust, kui seadmed töötavad erinevatel kiirustel.

![Jaotur](/lectures/images/hub.png)

**Seadmed võrgu, segmentide ja alamvõrkude struktureerimiseks**

Seadmeid nagu sillad, switchid, ruuterid ja lüüsid kasutatakse sidevõrkude loogiliseks struktureerimiseks (Joonis 3.6).

**Sild (bridge)**
Sild jagab võrgu loogilisteks segmentideks. Sõnumid edastatakse ühest segmendist teise üle silla pordi, kui vastuvõtja unikaalne võrguaadress (MAC) kuulub vastavasse segmenti. Silla tegevus toimub järgmiste sammude kaudu:

1. Andmepaketi vastuvõtmisel kontrollitakse lähteaadressi ja sihtaadressi.
2. Kui sihtaadressi ei ole tabelis, edastatakse pakett kõikidesse segmentidesse ning lisatakse sihtaadress tabelisse.
3. Sild edastab paketi vastavale segmendile, kui sihtaadress on tabelis.
4. Kui lähteaadress ja sihtaadress on samas segmendis, ei edastata paketti teise segmenti.

Sildade peamine eesmärk on filtreerida segmentidevahelist liiklust, et vähendada ummikuid suuremates kohtvõrkudes. Sillad tegutsevad OSI võrgumudeli kanalikihis ja neid kasutatakse näiteks hubidega ehitatud võrkudes.

**Switch (kommutaator)**
Switch on uuema generatsiooni sild, mis võimaldab informatsiooni paralleelset töötlemist ja suurendab võrgu andmevahetuskiirust. Switch töötab järgmiselt:

1. Switchi saabumisel kontrollitakse paketti ja viidatakse tabelile, et kindlaks teha, kas vastuvõtja MAC aadress on kirjas.
2. Kui MAC aadress puudub, saadetakse pakett kõigisse portidesse, kuni sihtseadmelt saadakse vastus.
3. Seejärel tehakse kirje, mis näitab, milline väljundport sobitati konkreetse MAC aadressiga.
4. Kõik järgnevad sama aadressi paketid edastatakse otse vastavasse porti.

Switch eristab kolme tüüpi vastuvõtja aadresse:
- **Leviedastus (broadcast)**: Pakett saadetakse kõigisse portidesse.
- **Multiedastus (multicast)**: Pakett saadetakse eelnevalt kindlaks määratud portidesse.
- **Üksikedastus (unicast)**: Pakett saadetakse ainult ühte porti, mis tõstab võrgu turvalisust ja mahtu.

Switchid töötavad tavaliselt OSI mudeli teise kihi baasil, kuid kõrgema klassi kommutaatorid võivad töötada ka kolmanda ja neljanda kihi baasil.

Switchi spetsiifilised tunnused:
- Iga pordi jaoks on spetsiaalne protsessor sissetulevate andmepakettide töötlemiseks.
- Iga tööjaam saab edastada andmeid ilma teiste tööjaamadega konkureerimata.
- Kontrollib ühendatud seadmete MAC aadresse.
- Võimaldab tõlgendada andmepakette ühest standardist teise.
- Puhverdab andmeid enne vastuvõtja ühendusparameetrite tuvastamist.
- Suhtleb täisdupleks-režiimis, võimaldades samaaegset andmeedastust ja vastuvõttu.

**Ruuter**
Ruuter on eraldiseisev seade, mida kasutatakse infopakettide jaotamiseks erinevate võrkude või võrgusegmentide vahel. Erinevalt hubidest ja sildadest töötab ruuter OSI mudeli võrgukihis ja kasutab IP aadresse. Ruuter kasutab marsruutimistabelit, kuhu on salvestatud teiste ruuterite IP aadressid, et määrata parim tee andmepakettide edastamiseks.

Näide:
- Võrgus A asuvad seadmed A1 ja A2, võrgus B asuvad seadmed B1 ja B2. Kui andmed saadetakse A1-lt A2-le, ei edasta ruuter neid võrku B. Kui aga andmed saadetakse A1-lt B1-le, edastab ruuter need võrku B.

Ruuterid vähendavad võrguliiklust ja parandavad kohtvõrgu turvalisust.

**Lüüsid (gateways)**network
Lüüs ühendab kahte kohtvõrku või kohtvõrgu ja globaalse võrgu, mis kasutavad erinevaid protokolle ja ligipääsuprotseduure. Lüüs eristab ja tuvastab liiklust ning kasutatakse näiteks kohtvõrgu ühendamiseks globaalsesse võrku.

![Võrguseadmed](/lectures/images/netowrkdevices.png)

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
![OSI kihtide protokollide andmeüksuste nimetused](/lectures/images/osimudel.png)
![Iga kihis enda metaandmed](/lectures/images/metaandmed.png)










- **Ethernet ja MAC-aadressid:**
  - **Ethernet** on kõige levinum tehnoloogia, mida kasutatakse juhtmega võrkudes. See määratleb, kuidas andmeid kaablite kaudu edastatakse.
  - **MAC-aadress:** Igal võrguseadmel on unikaalne identifikaator, mida nimetatakse MAC-aadressiks. See on nagu postiaadress, mis tagab, et andmed jõuavad õigesse kohta.

 ![MAC-aadress](/lectures/images/mac.png)
