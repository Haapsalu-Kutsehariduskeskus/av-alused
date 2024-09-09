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

# Nädal 2: OSI mudeli mõistmine - Osa 1 (Füüsiline ja kanalikiht (data link layer))

### Sissejuhatus OSI mudelisse
OSI mudel (Open Systems Interconnection Model) on nagu kaart, mis aitab mõista, kuidas andmed liiguvad üle võrgu. See jagab protsessi seitsmeks kihiks, millest igaühel on oma ülesanne. Võite seda võrrelda meeskonnaga, kus iga mängija täidab konkreetset rolli. OSI mudelist sai peamine mudel, mida ettevõtted järgivad toodete ja protokollide (reeglid, kuidas võrgud töötavad) loomisel.


Selles sessioonis keskendume kahele kihile:
1. **Füüsiline kiht**
2. **Kanalikiht**

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

### Seadmed võrgu struktuurimiseks

Seadmed nagu **sillad**, **switchid**, **ruuterid** ja **lüüsid** aitavad võrke organiseerida ja juhtida, kuidas erinevad osad omavahel suhtlevad.

---

**Sild**

Sild aitab võrku jagada väiksemateks osadeks, mida nimetatakse segmentideks. Sild saadab sõnumeid ühest segmendist teise, aga ainult siis, kui vastuvõtja on õigel segmendil. Kuidas see töötab:

1. Sild võtab sõnumi vastu ja kontrollib, kust see tuli ja kuhu see läheb.
2. Kui sild ei tea, kuhu sõnum läheb, saadab ta selle kõigile osadele ja õpib ära, kus sihtkoht on.
3. Kui sild teab sihtkohta, saadab ta sõnumi õigesse kohta.
4. Kui saatja ja vastuvõtja on samas segmendis, ei saada sild sõnumit mujale.

Sillad aitavad vähendada liiklust ja tagavad, et info jõuab ainult sinna, kuhu vaja.

---

**Switch**

Switch on nagu targem sild. See aitab seadmetel võrgu sees kiiremini suhelda. Kuidas see töötab:

1. Switch võtab sõnumi vastu ja kontrollib, kas ta teab, kuhu see läheb.
2. Kui switch ei tea, saadab ta sõnumi kõigile seadmetele, kuni saab vastuse.
3. Kui switch teab sihtkohta, ta jätab selle meelde.
4. Edaspidi saadab switch sõnumi otse õigesse kohta.

On kolme tüüpi sõnumeid:
- **Leviedastus**: Saadetakse kõigile.
- **Multiedastus**: Saadetakse kindlale grupile.
- **Üksikedastus**: Saadetakse ainult ühele seadmele.

Switchid teevad võrgu kiiremaks ja turvalisemaks.

---

**Ruuter**

Ruuter on seade, mis aitab saata infot erinevate võrkude vahel. See kasutab IP-aadresse (nagu majanumbrid arvutite jaoks) ja valib parima tee info saatmiseks. Näide:

- **Võrgus A** on seadmed A1 ja A2, **võrgus B** on seadmed B1 ja B2. Kui A1 saadab sõnumi A2-le, hoiab ruuter selle sõnumi võrgus A. Kui aga A1 saadab sõnumi B1-le, aitab ruuter sõnumi saata võrku B.

Ruuterid aitavad vähendada liiklust ja muuta võrgud turvalisemaks.

---

**Lüüs**

Lüüs ühendab kahte erinevat võrku. Näiteks võib see ühendada väikese võrgu majas suure võrguga nagu internet. Lüüs aitab tõlkida infot nii, et mõlemad võrgud saavad üksteisest aru.

---

![Võrguseadmed](/lectures/images/networkdevices.png)

### 2. Andmekihi kaadri struktuur

OSI mudelis aitab iga kiht ülemist kihti. Alumised kihid tegelevad lihtsamate asjadega, ja kui need on tehtud, liiguvad andmed järgmisele kihile, mis tegeleb keerulisemate ülesannetega.

Näide:
- Esimene kiht, füüsiline kiht, tegeleb bittide (väga väikeste andmeüksuste) liigutamisega.
- Järgmine, kanalikiht, hoolitseb juba nende andmete edasi liikumise eest, ilma et peaks muretsema, kuidas need bitid välja näevad, sest füüsiline kiht on selle töö ära teinud.

---

Kui andmed liiguvad arvutist võrku, läbivad need kõik OSI mudeli kihid järjest. Iga kiht lisab oma info andmetele, mida kutsutakse **päiseks**. Näiteks:

1. **Rakenduskiht** kodeerib andmed sobivasse vormi.
2. **Seansikiht** lisab info seansi kohta.
3. **Transpordikiht** jagab andmed vajadusel väiksemateks osadeks ja lisab aadressid.
4. **Võrgukiht** pakib andmed kokku ja saadab need füüsilisele kihile, mis muudab need signaalideks ja saadab teele.

---

Kui andmed jõuavad kohale, võtavad kihid need vastu vastupidises järjekorras. Iga kiht eemaldab oma päise, kuni andmed jõuavad tagasi rakenduseni.

---

OSI mudelil on palju eeliseid, näiteks:
- **Keerukuse vähenemine**: Lihtsam hallata, sest igal kihil on oma kindel ülesanne.
- **Koostalitlusvõime**: Seadmed ja programmid saavad paremini koos töötada.
- **Kiirem areng**: Uute tehnoloogiate loomine on lihtsam.
- **Lihtsam õppida**: Mudeleid on kergem õppida ja mõista.

---

Iga kiht OSI mudelis täidab oma osa andmete töötlemisel ja saatmisel.

![OSI kihtide protokollide andmeüksuste nimetused](/lectures/images/osimudel.png)
![Iga kihis enda metaandmed](/lectures/images/metaandmed.png)

### 3. Kahendarvutus ja arvutus

Arvutid ja võrgud kasutavad **kahendsüsteemi**, seega on oluline sellest natuke rääkida.

- **Kahendsüsteem** on sarnane kümnendsüsteemile, mida me igapäevaselt kasutame. 
- Erinevus on selles, et kahendsüsteemis on ainult **kaks numbrit**: 0 ja 1, samas kui kümnendsüsteemis on **kümme numbrit** (0-9).
- Paljud asjad kahendsüsteemis on samad, mõned tegevused on isegi **lihtsamad**.

Arvutid kasutavad binaarsüsteemi aadresside ja **suhtluse** jaoks. Näiteks IPv4 aadress koosneb 32 bitist, mis on jagatud **4 gruppi** (oktetid).
Iga oktett on 8 bitti (1 bait).

IP-aadresse nagu `10101000` teisendatakse kümnendsüsteemi nagu `192.168.0.1`.
Teisendamiseks kasutatakse **positsioonilist märkimist**, kus iga binaarne koht kahekordistab oma väärtust (1, 2, 4, 8 jne).

![Binaarsüsteem](/lectures/images/binar.png)

Binaarsüsteemis määrab numbri **positsioon** selle väärtuse. Näiteks 8-bitises arvus on vasakpoolseim bitt 128, järgmine 64 jne.
Binaararv `11000000` teisendatakse kümnendsüsteemi kui `128 + 64 = 192`.

**Kuueteistkümnendsüsteem** kasutab **baasi 16**. Selleks kasutatakse numbreid 0-9 ja tähti **A-F** (A=10, B=11 jne).
**IPv6** aadressid koosnevad 128 bitist ja neid esitatakse heksadesimaalis lihtsamaks lugemiseks.
Iga osa IPv6 aadressist on nimetatud **heksatetiks**, mis koosneb neljast heksadesimaalsest märgist.

![Kuueteistkümnendsüsteem](/lectures/images/16.png)

**Teisendamine arvusüsteemide vahel**

- **Binaarsete arvude teisendamine kümnenditeks**: Lisa need väärtused kokku, kus on 1.
- **Kümnendite teisendamine binaariks**: Jaga arv 2-ga ja jälgi jääke.
- **Kuueteistkümnendite teisendamine kümnendiks/binaariks**: Esmalt teisenda heksadesimaal binaariks, siis binaar kümnendiks.
- **Tööriistad**: Windowsi **kalkulaator** aitab teisendustega .

![IPv4 to Binary](/lectures/images/binary2.png)

### 4. Kanalikiht (Data Link Layer)

Kui kaks arvutit omavahel räägivad, peab keegi aitama neil üksteist mõista. Kanalikiht teebki seda, pakkides andmed nii, et mõlemad arvutid teavad, kuidas neid lugeda. Lisaks kontrollib see kiht, kas andmed on õiged või kahjustatud. Kui andmed on katki, saadetakse need tagasi. Arvutiga paralleele tuues võib kanalikihti vaadelda ka seadmedraiverina.

Selle kihi töö on aidata arvutitel andmeid edastada ja vastu võtta võrgu kaudu.

Kanalikiht jaguneb kaheks oluliseks osaks:
- **LLC (Loogilise lingi kontroll)**: Aitab arvutil suhelda oma tarkvara ja riistvaraga.
- **MAC (Meediumipöörduse juhtimine)**: Kontrollib, kuidas andmed saadetakse ja vastuvõetakse. Igal seadmel on oma **MAC-aadress**, mis on nagu seadme unikaalne nimi võrgus.

Võrgu topoloogiat võib mõelda kui kaarti sellest, kuidas arvutid on ühendatud:

- **Füüsiline topoloogia**: Näitab, kuidas arvutid ja seadmed (nt ruuterid ja kommutaatorid) on kaablite või traadita ühendustega seotud.
- **Loogiline topoloogia**: Näitab, kuidas andmed liiguvad, milliseid teid nad kasutavad.

**Levinumad topoloogiad**

- **Punkt-punkt**: Kaks seadet on omavahel otse ühendatud. Kujuta ette, et need on nagu kaks inimest, kes räägivad teineteisega läbi otse telefoni.
- **Tsentraalne ühendus (Hub-and-Spoke)**: Üks kesksõlm (näiteks ruuter) ühendab mitmeid teisi seadmeid. Mõtle sellele kui klassiruumile, kus õpetaja räägib korraga kõigile õpilastele.
- **Võrgustik (Mesh)**: Iga seade on ühendatud iga teise seadmega. See on väga usaldusväärne, kuid keeruline ja kallis seadistada. Mõtle sellele kui väga keerulisele veebile.

![Võrgutopoloogiad ](/lectures/images/networktopology.png)

**Andmete edastus sideliinis**

- **Pooldupleks**: Seadmed saavad korraga kas ainult saata või vastu võtta, mitte mõlemat korraga.
- **Täisdupleks**: Seadmed saavad korraga andmeid saata ja vastu võtta.

Pooldupleks on nagu kõndimine kitsal sillal, kus üks inimene peab teisele teed andma. Täisdupleks on aga nagu lai tee, kus kaks autot saavad mõlemad korraga sõita.

![Pooldupleks ja täisdupleks ](/lectures/images/dupleks.png)

Kui mitu seadet proovivad korraga andmeid saata, võib tekkida "kokkupõrge", nagu kaks inimest, kes üritavad korraga rääkida.
- **CSMA/CD**: Kui kokkupõrge tuvastatakse, seadmed ootavad ja proovivad hiljem uuesti.
- **CSMA/CA**: Seda kasutatakse Wi-Fi võrkudes, kus seadmed üritavad vältida kokkupõrget, oodates oma järjekorda.

Arvutivõrkudes saadetakse infot väikestes pakikestes, mida kutsutakse **kaadriteks** (frame). Need kaadrid on nagu kastid, mis hoiavad bitid (väiksed andmetükid) sees. Mõnikord lisatakse kaadrisse erilisi bitte, et arvuti teaks, millal kaader algab ja lõpeb.
Kui kaadri sees on liiga palju järjestikuseid sarnaseid bitte, võib arvuti ära segi minna. Seepärast lisatakse mõned lisa-bitid, et arvuti teaks kindlalt, kus kaadri lõpp on. Nii nagu salakirjas lisatakse vahel tähti, et sõnum oleks arusaadav.

Kaadriga saadetavatele andmetele lisatakse juurde **päis** (header) ja olenevalt protokollist võibolla ka **saba** (trailer). Päis sisaldab **väljasid**, mis annavad andmete kohta informatsiooni, näiteks kaadri puhul **sihtaadress**, **lähteaadress**, üle kantavate andmete hulk, kaadri kontrollsumma jms.

![OSI kanalikiht](/lectures/images/datalink.png)
