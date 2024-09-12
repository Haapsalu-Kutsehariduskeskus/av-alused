[!TIP]
>[Physical Layer](https://www.youtube.com/watch?v=AHV54tqhZU0&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=6)
>[Number Systems](https://www.youtube.com/watch?v=RdoxJsWzFKc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=7)
>[Data Link Layer](https://www.youtube.com/watch?v=eK4s5TQm45c&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=8)
>[Ethernet Switching](https://www.youtube.com/watch?v=KWm7_vsfdE4&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=9)

# Nädal 2: OSI mudeli mõistmine - Osa 1 (Füüsiline ja kanalikiht)

### Sissejuhatus OSI mudelisse

OSI mudel (Open Systems Interconnection Model) on universaalne võrgustandard, mis selgitab, kuidas erinevad süsteemid ja seadmed suhtlevad võrgu kaudu. Seda võib võrrelda juhendiga, mis õpetab, kuidas andmed liiguvad ühest punktist teise läbi erinevate kihtide, millest igaüks täidab oma konkreetset rolli. Kujutlege OSI mudelit kui meeskonda, kus igal liikmel on kindel ülesanne, mis aitab kaasa üldisele edule.

OSI mudel koosneb seitsmest kihist, millest igaüks vastutab andmeedastuse erineva aspekti eest. Selles sessioonis keskendume kahest madalamale kihile, mis moodustavad võrgu füüsilise aluse:
1. **Füüsiline kiht**
2. **Kanalikiht**

---

### 1. Füüsiline kiht: Võrgu aluspõhi

- **Mis on füüsiline kiht?**  
  Füüsiline kiht tegeleb kõigega, mis on võrgus nähtav ja puudutatav — kaablid, juhtmed, pistikud, signaalid jne. See kiht vastutab andmete füüsilise edastamise eest ühest seadmest teise.

  **Näited füüsilisest kihist:** 
  - Kaablid (näiteks vaskkaablid ja fiiberoptilised kaablid)
  - Elektrilised signaalid või valgussignaalid (sõltuvalt kaablist)
  - Pistikud ja liidesed (näiteks RJ45 kaabli ots)
  - Võrguseadmete füüsilised paigutused ja ühendused (võrgutopoloogia)

  **Lihtne seletus:** Füüsiline kiht on vastutav selle eest, et andmed liiguksid juhtmete või kaablite kaudu ühest seadmest teise, kasutades selleks elektrilisi signaale või valgust.

- **Olulised tehnoloogiad ja standardid:**
  - RS-232 (standardsed signaali edastamise meetodid)
  - RJ45 (ühenduste tüüp, mida kasutatakse näiteks Ethernet kaablites)
  - 100BASE-TX (Etherneti kiirusstandard)
  - 802.11 (Wi-Fi standardid)
  - DSL ja muud internetiühenduse meetodid

- **Edastuskandjate tüübid:**
  - **Vaskkaablid:** Need on kõige tavalisemad ja laialt levinud kaablid, mida kasutatakse võrguühenduste loomiseks.
    - **Varjestamata keerdpaar (UTP):** See on tavaline kaabel, mida kasutatakse kodustes ja kontorivõrkudes. Selle ülesanne on vähendada häireid, mis võivad tulla teistest signaalidest või elektromagnetilistest allikatest.
  - **Fiiberoptilised kaablid:** Need kaablid edastavad andmeid valgussignaalide abil, mis võimaldab kiiret andmesidet pikkade vahemaade taha. 
    - **Fiiberoptiliste kaablite eelised:** Need on palju kiiremad ja töökindlamad kui vaskkaablid, kuid sageli ka kallimad.
  - **Juhtmevaba meedia (näiteks Wi-Fi ja Bluetooth):** Nende abil saab andmeid edastada ilma füüsiliste kaabliteta. 
    - **Väljakutsed juhtmevabas suhtluses:** Füüsilised takistused, nagu seinad, võivad signaali kvaliteeti ja kiirust vähendada.

![Füüsiline kiht](/lectures/images/physical_layer.png)

---

### Seadmed võrgu struktuurimiseks

Võrgu struktuuri moodustamiseks kasutatakse erinevaid seadmeid, mis aitavad andmeid suunata, võimendada ja jagada erinevate tööjaamade vahel. Seadmed jagunevad kaheks peamiseks kategooriaks: passiivsed ja aktiivsed seadmed.

- **Passiivsed seadmed:** Need seadmed ei vaja elektritoidet ja neid kasutatakse võrgukaablite ühendamiseks, pikendamiseks või organiseerimiseks. Nende peamine ülesanne on võimaldada füüsiliste ühenduste loomist, kuid nad ei töötle andmeid ega signaale.

![Serverikapp](/lectures/images/rack.png)

  - **Ühenduspistikud:** Neid kasutatakse võrgukaablite pikendamiseks, võimaldades ühendada erinevaid kaableid või seadmeid.
    - **Näide:** Kui kaks lühikest kaablit ei ulatu omavahel kokku, saab neid ühenduspistikuga pikendada, luues füüsilise ühenduse.
  
  - **Seinapistik:** Seinapistik on tavaliselt paigaldatud seinakarp, kuhu on ühendatud võrgukaabel. Need võivad sisaldada RJ-45 (Ethernet) või RJ-11 (telefoniliin) pesasid. 
    - **Funktsioon:** Võimaldab lihtsamat ligipääsu võrguühendusele erinevates ruumides, luues puhta ja organiseeritud ühenduspunkti.

![Liidespaneel](/lectures/images/patchpanel.png)

  - **Juhtmepaneel (Patch panel):** Seda kasutatakse suuremasse võrku ühendatud kaablite korraldamiseks. Iga kaabel on ühendatud juhtmepaneeliga, mis võimaldab kiiret ja lihtsat ligipääsu, kui kaablit on vaja vahetada või testida.
    - **Eesmärk:** Tagada lihtne kaablite haldus ja hooldus, hoides kaablid korras ja loogilises järjekorras.

  - **Passiivne jaotur (Hub):** See seade jaotab sisendsignaali mitme tööjaama vahel, kuid ei töötle signaale ega suuda neid võimendada. Hub lihtsalt jagab kogu võrgu liikluse igasse ühendatud seadmesse, olenemata sellest, kas andmed on neile mõeldud või mitte.
    - **Oluline omadus:** Ei vaja elektritoidet, kuna see ei tee andmetega midagi peale nende füüsilise jaotamise.

![Delta keskus Tartus](/lectures/images/tartu_delta_server_room.png)



- **Aktiivsed seadmed:** Need seadmed vajavad elektritoidet, kuna nad töötlevad, võimendavad või muundavad signaale. Need võimaldavad andmete edastamist kaugematele vahemaadele ja paremat ühenduse kvaliteeti, suunates andmed õigesse kohta.

  - **Ülekandemeediumi konverterid:** Need seadmed võimaldavad erinevat tüüpi kaablite omavahelist ühendamist, näiteks UTP (vaskkaabel) ja fiiberoptilised kaablid (valguskaabel). See võimaldab ühendada erinevaid võrguosasid, mis kasutavad erinevaid tehnoloogiaid.
    - **Näide:** Kui üks võrguseade kasutab UTP kaablit ja teine fiiberoptilist kaablit, võimaldab konverter nende kahe seadme vahelist suhtlust.

  - **Repiiter:** Seade, mis võimendab ja taastab signaale, et need jõuaksid kaugemale. Kui signaal liigub mööda kaablit, kaotab see järk-järgult oma tugevuse, ja repiiter taastab selle, et andmed jõuaksid kaugematesse kohtadesse.
    - **Näide:** Kui kaks arvutit asuvad üksteisest liiga kaugel ja signaal hakkab nõrgenema, paigaldatakse nende vahele repiiter, mis tugevdab signaali ja tagab ühenduse püsimise.

  - **Hub (Jaotur):** Aktiivne jaotur, mis ühendab mitu tööjaama ja moodustab neist ühe võrgu. Erinevalt passiivsest hub'ist vajab aktiivne hub elektritoidet ja suudab mõnel juhul tuvastada rikkis pordi, mille ta seejärel välja lülitab. Siiski ei suuda ka aktiivne hub andmeid sihtotstarbeliselt suunata – see saadab kõik signaalid kõigile ühendatud seadmetele.
    - **Oluline erinevus passiivsest hub'ist:** Aktiivne jaotur suudab signaale töödelda ja mõnel juhul ka tuvastada vigaseid ühendusi.

  ![Jaotur](/lectures/images/hub.png)

---

### Sild, switch, ruuter ja lüüs

Need seadmed on veelgi intelligentsemad aktiivsed seadmed, mis suudavad andmeid sihtotstarbeliselt suunata, töötada koos erinevate võrkudega ja pakkuda turvalisust ning efektiivsust.

- **Sild (Bridge):** Jagab võrku väiksemateks segmentideks, et vähendada liiklust. Sild uurib, kuhu andmed peavad minema, ja saadab need ainult sinna, vähendades seeläbi ülejäänud võrgu koormust.
  - **Näide:** Kui suur võrk on jagatud kaheks segmendiks, võib sild otsustada, et andmed peavad minema ainult ühte segmenti, ja ei edasta neid teise.

- **Switch:** Suudab suunata andmed otse õigesse sihtkohta, ilma kogu võrku üle koormamata. See teeb võrgu kiiremaks ja turvalisemaks, kuna andmed liiguvad ainult nendele seadmetele, kellele need on mõeldud.
  - **Erinevus hub'ist:** Switch on tunduvalt targem kui hub, kuna ta teab, milline seade on millise pordi taga, ja saadab andmed ainult õigesse kohta.

- **Ruuter (Router):** Ruuter on seade, mis suunab andmeid erinevate võrkude vahel, kasutades IP-aadresse. Ruuter teeb kindlaks, milline on parim tee andmete liikumiseks erinevate võrkude kaudu, ja suunab need õigesse sihtkohta.
  - **Näide:** Ruuter ühendab koduvõrgu internetiga ja otsustab, millised andmepaketid peavad liikuma kodusesse võrku ja millised internetti.

- **Lüüs (Gateway):** Lüüs ühendab erinevat tüüpi võrgud ja tõlgib nendevahelisi andmeid, näiteks koduvõrgu ja interneti vahel.
  - **Näide:** Lüüs võib tõlkida andmeid, kui kaks võrku kasutavad erinevaid protokolle (näiteks kui koduvõrk kasutab üht tüüpi aadresse ja internet kasutab teist tüüpi).

![Võrguseadmed](/lectures/images/networkdevices.png)

---

### 2. Kanalikihi kaadri struktuur

Kanalikiht (Data Link Layer) on OSI mudeli teine kiht, mis vastutab usaldusväärse andmevahetuse eest seadmete vahel kohalikus võrgus või mõnes teises füüsilises sidekeskkonnas. Selle kihi ülesandeks on organiseerida andmete liikumist punktist A punkti B nii, et see toimub vigadeta ja õiges järjestuses. Kuna andmed peavad liikuma üle füüsilise keskkonna (kaablid, raadiosignaalid jne), siis jaotatakse need andmed väikesteks ühikuteks, mida nimetatakse kaadriteks. Kaadrisse lisatakse kontrollandmed, mis aitavad tagada, et andmed jõuavad õigesti kohale. Kanalikiht jaguneb kaheks osaks:

- **LLC (Loogilise lingi kontroll):** LLC (Logical Link Control) vastutab loogilise ühenduse loomise ja haldamise eest kõrgemate kihtide (tarkvara) ja madalamate kihtide (riistvara) vahel. Selle kaudu saab tarkvara vahetada andmeid riistvaraga, näiteks võrgukaardiga. LLC ülesanne on kontrollida, kas saadetud andmed jõuavad kohale ja kas need on õiged. Kui edastuse käigus tekib viga, võib LLC need andmed uuesti saata, et vältida andmekadu. LLC on ka oluline selleks, et erinevad võrguprotokollid (nt IP, IPX) saaksid töötada sujuvalt koos.

- **MAC (Meediumipöörduse juhtimine):** MAC (Media Access Control) tegeleb andmete füüsilise edastamisega läbi võrgu, näiteks Etherneti kaudu. MAC-aadressid mängivad võtmerolli selles protsessis, kuna iga seade võrgus peab olema identifitseeritav unikaalse MAC-aadressi abil. MAC-aadress määrab, milline seade saadab või võtab andmeid vastu. MAC juhib ka seda, kuidas seadmed võrgus pääsevad ühisele sidekeskkonnale. Näiteks mitmed seadmed võivad üritada korraga andmeid saata, kuid MAC tagab, et need edastused ei lähe omavahel konflikti ja andmed ei lähe kaduma.

MAC-protokollid aitavad hallata ka edastuse konflikte. Näiteks Etherneti kasutatav CSMA/CD (Carrier Sense Multiple Access with Collision Detection) protokoll tuvastab, kui kaks seadet üritavad samaaegselt andmeid saata, ja aitab neid konflikte lahendada.

![Võrgukaart](/lectures/images/access_media.png)

---

### Võrgutopoloogiad

Võrgutopoloogiad määravad, kuidas seadmed on omavahel füüsiliselt või loogiliselt ühendatud ning kuidas andmed liiguvad võrgus. Need on võrgudisaini aluseks ja mõjutavad, kui efektiivne, töökindel ja kiire on andmevahetus.

- **Punkt-punkt (Point-to-Point):** See topoloogia hõlmab otsest ühendust kahe seadme vahel. See on lihtsaim ja sageli kõige töökindlam viis andmete edastamiseks, kuna ei ole vahesõlmi, mis võiksid tekitada viivitusi või vigade allikaid. Punkt-punkt ühendust kasutatakse sageli väikestes võrguüksustes, nagu näiteks arvuti ühendamisel otse printeriga.

- **Tsentraalne ühendus (Hub-and-Spoke):** See topoloogia hõlmab ühte keskset sõlme, mis ühendab mitut seadet. Keskne sõlm, näiteks switch või hub, koordineerib liiklust ja suunab andmed õigesse sihtkohta. Selline ülesehitus on tihti kasutusel väiksemates ettevõtete võrkudes, kus on vaja lihtsat ja selget võrguhaldust. Kuigi see on lihtne üles ehitada, on keskne sõlm võrguliikluse kitsaskoht – kui see tõrkub, siis kogu võrk lakkab töötamast.

- **Võrgustik (Mesh):** Mesh-topoloogias on igal seadmel ühendus mitmete teiste seadmetega. See pakub väga suurt töökindlust, sest kui üks tee andmete edastamiseks on katkenud, saavad andmed liikuda läbi alternatiivsete teede. Seda topoloogiat kasutatakse tavaliselt suuremates ja missioonikriitilistes süsteemides, kus on oluline, et ükski tõrge ei katkestaks võrgu tööd, näiteks andmekeskustes või sõjaväevõrkudes.

![Võrgutopoloogiad](/lectures/images/networktopology.png)

---

### Pooldupleks vs. Täisdupleks

**Dupleks-süsteemid** kirjeldavad, kuidas seadmed suhtlevad omavahel ja kas need saavad andmeid vahetada samaaegselt või mitte.

- **Pooldupleks (Half-Duplex):** Pooldupleksi korral saab seade korraga kas saata või vastu võtta andmeid, kuid mitte mõlemat. See tähendab, et suhtlus toimub ühes suunas korraga. Seda tüüpi side on levinud vanemates raadioside süsteemides, kus näiteks politseiraadio kaudu saab üks osapool korraga rääkida, kuid teised peavad ootama, kuni edastamine on lõppenud, enne kui nad saavad vastata.

- **Täisdupleks (Full-Duplex):** Täisdupleksi korral saavad seadmed korraga saata ja vastu võtta andmeid, võimaldades tõhusamat suhtlust. Enamik kaasaegseid võrguseadmeid, nagu Ethernet-kaablid ja switchid, toetavad täisdupleksühendust, mis suurendab võrgu läbilaskevõimet ja vähendab viivitusi, kuna andmevahetus toimub mõlemas suunas samaaegselt.

---

### Pakkimine kaadriks

Selleks et andmed oleksid usaldusväärselt edastatud ja õigesti identifitseeritud, jagatakse need **kaadriteks** (frames), mis sisaldavad nii kasutaja andmeid kui ka juhtimisinformatsiooni. Kaader koosneb järgmistest osadest:

- **Päis (header):** Siia kuuluvad olulised andmed, nagu saatja ja vastuvõtja MAC-aadressid, samuti vigade avastamise mehhanismid, näiteks tsükliline redundantsuskontroll (CRC). Päise abil saab kaader võrgus õigesti tuvastatud ja suunatud.
- **Andmed (data):** See on kaadri sisu, mida edastatakse. Andmed võivad pärineda kõrgematest kihtidest, näiteks rakenduskihilt (e-post, veebilehed jne).
- **Saba (trailer):** Saba sisaldab täiendavat informatsiooni, mis on vajalik vigade tuvastamiseks ja parandamiseks, võimaldades andmekihil kontrollida, kas kaader on edastamise käigus kahjustamata.

Kaadrite struktuur ja nende kontrollmehhanismid aitavad tagada, et edastatud andmed jõuavad terviklikult ja õigesti kohale.

![OSI kanalikiht](/lectures/images/datalink.png)

---

### 3. Etherneti Lülitamine (Switching)

Etherneti lülitamine keskendub mitmele olulisele aspektile, sealhulgas Ethernet-raami struktuurile, MAC-aadressidele ja MAC-aadresside tabelitele. Lisaks käsitletakse lüliti kiiruseid ja edastamisviise. Ethernet töötab OSI mudeli kahes kihis – andmelingi kihis (kiht 2) ja füüsilises kihis (kiht 1). Seda tehnoloogiat reguleerivad IEEE 802 standardid.

![Ethernet lüliti struktuur](/lectures/images/ethernet_switch_structure.png)

### Etherneti Kapseldamine

Etherneti raam (frame) koosneb mitmest osast: saatja ja sihtaadressist, andmetest ning järelkärust, mis sisaldab vigade tuvastamiseks Raami Kontrolljärjestust (FCS). Etherneti adresseerimine toimub MAC-aadresside abil, mis aitavad andmepakette edastada lokaalses võrgus (LAN). Vigade tuvastamiseks kasutab Ethernet Raami Kontrolljärjestust (FCS), mis paikneb raami lõpus ja aitab avastada edastusvigu.

![Etherneti raami struktuur](/lectures/images/ethernet_frame_structure.png)

### Etherneti MAC-aadressimine

MAC-aadressid koosnevad 48-bitistest binaarväärtustest, mida väljendatakse 12 kuueteistkümnendsüsteemi numbrina (ehk 6 baidina). Need peavad olema unikaalsed ja need määrab tootja, kasutades organisatsiooni unikaalset identifikaatorit (OUI). Etherneti MAC-aadresse kasutatakse ainult lokaalseks andmeedastuseks, sest marsruutimine toimub OSI mudeli võrgu kihis (kiht 3).

![MAC-aadressi struktuur](/lectures/images/mac_address_structure.png)

### Side Tüübid

Etherneti võrkudes võib side toimuda erineval viisil:
- **Unicast**: üks seade saadab raami otse konkreetsele seadmele.
- **Broadcast**: raam saadetakse kõigile seadmetele võrgus, kusjuures MAC-aadress on FF:FF:FF:FF:FF:FF.
- **Multicast**: raam saadetakse mitmele seadmele, kuid mitte kõigile, näiteks ainult kindlale seadmete grupile.

![Side tüübid Ethernetis](/lectures/images/ethernet_communication_types.png)

### MAC-aadresside Tabel

Lülitid kasutavad MAC-aadresse, et otsustada, kuhu andmepakett suunata. Kui lüliti saab raami, kontrollib see oma MAC-aadresside tabelit ja määrab, millise pordi kaudu raam edastada. Kui sihtaadress pole teada, saadetakse raam kõigile portidele, välja arvatud sellele, kust see tuli.

![MAC-aadresside tabel lülitis](/lectures/images/mac_address_table.png)

### Lülitusmeetodid

Etherneti lülitid kasutavad erinevaid meetodeid andmete edastamiseks. Üks neist on **Store-and-Forward**, kus lüliti loeb terve raami, kontrollib vigu ja alles siis edastab selle sihtkohta. Teine meetod on **Cut-Through**, mille puhul lüliti edastab raami enne, kui kogu pakett on vastu võetud. Cut-Through meetodil on kaks varianti:
- **Fast Forward**: edastamine algab kohe pärast sihtaadressi lugemist, mis tagab madala latentsuse.
- **Fragment-Free**: lüliti kontrollib esimese 64 baiti jooksul vigu enne edastamist.


### Lüliti Mälu Puhverdamine

Lülitid kasutavad raamide hoidmiseks kahte meetodit: **pordipõhine mälu**, kus raamid salvestatakse iga pordi jaoks eraldi järjekorda, ja **jagatud mälu**, kus raamid paigutatakse jagatud mälupuhvrisse, mida seotakse dünaamiliselt sihtportidega.

![Lüliti mälu puhverdamine](/lectures/images/switch_memory_buffering.png)

### Dupleksseaded ja Automaatne Läbirääkimine

Etherneti seadmed saavad töötada kas täisdupleksis või pooldupleksis. **Täisdupleksis** saavad seadmed saata ja vastu võtta andmeid samaaegselt, samas kui **pooldupleksis** saavad nad teha üht asja korraga – kas saata või vastu võtta. **Automaatne läbirääkimine** võimaldab seadmetel määrata optimaalsed kiiruse ja duplekseaded automaatselt. **Dupleksi sobimatus** on tavaline probleem, kus üks seade töötab täisdupleksis ja teine pooldupleksis, põhjustades jõudlusprobleeme.


### Auto-MDIX Funktsioon

Kaasaegsetel lülititel on funktsioon nimega **Auto-MDIX**, mis tuvastab automaatselt, kas kasutatakse sirget või ristkaablit, ning kohandab oma seaded vastavalt. See aitab vältida käsitsi sekkumise vajadust ja lihtsustab kaabelduse õiget toimimist.

![Auto-MDIX funktsioon](/lectures/images/auto_mdix_feature.png)

---