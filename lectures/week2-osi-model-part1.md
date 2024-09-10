> [!TIP]
>[Physical Layer](https://www.youtube.com/watch?v=AHV54tqhZU0&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=6)
>[Number Systems](https://www.youtube.com/watch?v=RdoxJsWzFKc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=7)
>[Data Link Layer](https://www.youtube.com/watch?v=eK4s5TQm45c&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=8)
>[Ethernet Switching](https://www.youtube.com/watch?v=KWm7_vsfdE4&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=9)

# Nädal 2: OSI mudeli mõistmine - Osa 1 (Füüsiline ja kanalikiht)

### Sissejuhatus OSI mudelisse

OSI mudel (Open Systems Interconnection Model) on nagu kaart, mis aitab mõista, kuidas andmed liiguvad üle võrgu. See jagab protsessi seitsmeks kihiks, millest igaühel on oma ülesanne. Võite seda võrrelda meeskonnaga, kus iga mängija täidab konkreetset rolli. OSI mudelist sai peamine mudel, mida ettevõtted järgivad toodete ja protokollide loomisel.

Selles sessioonis keskendume kahele kihile:
1. **Füüsiline kiht**
2. **Kanalikiht**

---

### 1. Füüsiline kiht: Võrgu aluspõhi

- **Mida teeb füüsiline kiht?**
  - See on kiht, kus toimub kõik füüsiline. See käsitleb riistvara—kaablid, juhtmed ja signaalid, mis kannavad andmeid ühest seadmest teise.

  **Näited:** Kaablid, pistikud, elektrilised pinged, füüsilised võrgutopoloogiad.  
  **Olulised kontseptsioonid:** RS-232, RJ45, V.34, 100BASE-TX, SDH, DSL, 802.11.  
  **Lihtsustatult:** Vastutab andmete edastamise eest kaablite kaudu, kasutades elektrilisi signaale või valgust.

- **Edastuskandjate mõistmine:**
  - **Vaskkaablid:** Kõige levinum kaabel, mida kasutatakse paljudes kodudes ja kontorites.
    - **Varjestamata keerdpaar (UTP) kaabel:** Vähendab häireid teistest signaalidest.
  - **Fiiberoptilised kaablid:** Kasutavad elektri asemel valgust, võimaldades ülikiiret ja kauglevi kommunikatsiooni.
    - **Eelised:** Kiirem ja usaldusväärsem kui vask, kuid kallim.
  - **Juhtmevaba meedia:** Wi-Fi ja Bluetooth võimaldavad andmeid edastada ilma füüsiliste kaabliteta.
    - **Väljakutsed:** Seinte ja muude takistuste tõttu võivad kiirus ja ühendus kannatada.

![Füüsiline kiht](/lectures/images/physical_layer.png)

---

### Seadmed võrgu struktuurimiseks

- **Passiivsed seadmed:** Võrgukaabli pikendamiseks või ühenduste loomiseks.
  - **Ühenduspistikud:** Võrgukaabli pikendamiseks.  
  - **Seinapistik:** Üks või kaks porti, millel saab olla RJ-45 või RJ-11 otsik.
  - **Juhtmepaneel (Patch panel):** Kaablite korraldamise ja jaotamise punkt.
  - **Passiivne jaotur (Hub):** Jaotab sisendsignaali mitme tööjaama vahel, vajamata elektritoidet.

![Passiivsed seadmed](/lectures/images/patchpanel.png)

- **Aktiivsed seadmed:** Võimendavad ja muudavad signaale, võimaldades andmete edastamist pikematel vahemaadel.
  - **Ülekandemeediumi konverterid:** Ühendavad erinevat tüüpi kaableid, näiteks UTP ja valguskaableid.
  - **Repiiter:** Võimendab signaale, et need jõuaksid kaugemale.
  - **Hub (Jaotur):** Seade, mis ühendab mitu tööjaama ja moodustab neist ühe võrgu. Kui port on rikkis, võib hub selle välja lülitada.

![Jaotur](/lectures/images/hub.png)

---

### Sild, switch, ruuter ja lüüs

- **Sild:** Jagab võrku segmentideks ja edastab sõnumeid õigesse segmenti, vähendades liiklust.
- **Switch:** Suunab andmed otse õigesse sihtkohta, muutes võrgu kiiremaks ja turvalisemaks.
- **Ruuter:** Suunab andmed erinevate võrkude vahel, kasutades IP-aadresse.
- **Lüüs:** Ühendab erinevaid võrke ja tõlgib nendevahelisi andmeid.

![Võrguseadmed](/lectures/images/networkdevices.png)

---

### 2. Andmekihi kaadri struktuur

Andmekiht aitab seadmetel omavahel suhelda. See jaguneb kaheks osaks:
- **LLC (Loogilise lingi kontroll):** Suhtlus tarkvara ja riistvara vahel.
- **MAC (Meediumipöörduse juhtimine):** Kontrollib, kuidas andmed saadetakse ja vastuvõetakse.

**Võrgutopoloogiad:**
- **Punkt-punkt:** Kaks seadet ühendatud otse.
- **Tsentraalne ühendus (Hub-and-Spoke):** Üks keskne sõlm ühendab mitmeid seadmeid.
- **Võrgustik (Mesh):** Iga seade on ühendatud iga teise seadmega.

![Võrgutopoloogiad](/lectures/images/networktopology.png)

---

**Pooldupleks vs. Täisdupleks:**
- **Pooldupleks:** Seadmed saavad kas saata või vastu võtta, mitte mõlemat korraga.
- **Täisdupleks:** Seadmed saavad korraga andmeid saata ja vastu võtta.

![Pooldupleks ja täisdupleks](/lectures/images/dupleks.png)

---

**Pakkimine kaadriks:**  
Arvutivõrkudes saadetakse infot väikestes pakikestes, mida kutsutakse **kaadriteks**. Kaadri sees olevate andmete kohta lisatakse päised ja vahel ka sabad. Päis sisaldab andmete kohta olulist teavet, näiteks siht- ja lähteaadresse.

![OSI kanalikiht](/lectures/images/datalink.png)
