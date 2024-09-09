<div class="small-grey-box">
  ## Module 1: Networking Today
  - [Networking Today](https://www.youtube.com/watch?v=TBAvNZIcdVQ&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=2)

  ## Module 2: Basic Switch and End Device Configuration
  - [Basic Switch and End Device Configuration - Part 1](https://www.youtube.com/watch?v=4fMoxkiTEjc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=2)
  - [Basic Switch and End Device Configuration - Part 2](https://www.youtube.com/watch?v=ruainw-2Y28&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=3)

  ## Module 3: Protocols and Models
  - [Protocols and Models - Part 1](https://www.youtube.com/watch?v=VqGIeL0jRJI&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=4)
  - [Protocols and Models - Part 2](https://www.youtube.com/watch?v=agX0G-9JTpM&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=5)
</div>

# Week 1: Sissejuhatus võrkudesse

Kas oled kunagi mõelnud, kuidas saad oma sõpradega internetis rääkida, mängida mänge inimestega, kes on kaugel, või vaadata videoid kogu maailmast? Kõik see on võimalik tänu millelegi, mida nimetatakse **võrguks**!

Selles õppetunnis õpime, mis on võrgud, kuidas need töötavad ja miks need on nii olulised.

## Võrkude areng

Võrgud algasid aeglase dial-up ühendusega, kus kasutati telefoniliini internetiühenduseks. See oli aeglane ning telefoni ja internetti ei saanud samal ajal kasutada! Siis tuli lairibaühendus, mis tegi asjad kiiremaks DSL-i ja kaabli abil. Nüüd kasutame fiiberoptilisi kaableid, mis on ülikiired ja edastavad andmeid valgusena läbi pisikeste klaaskiudude. See areng on teinud kõik, mida me internetis teeme, palju kiiremaks ja usaldusväärsemaks.

### Interneti kiiruse võrdlus

| **Ühenduse tüüp**   | **Keskmine kiirus**     |
|---------------------|-------------------------|
| **Dial-up**         | 56 Kbps (Kilobitti sekundis) |
| **DSL**             | 1-15 Mbps (Megabitti sekundis) |
| **Kaabel**          | 10-200 Mbps             |
| **Fiiberoptiline**  | 100-1000 Mbps (1 Gbps)  |

---

## Kuidas võrgud meid ühendavad

Võrgud toovad meid üksteisele lähemale kui kunagi varem, võimaldades meil suhelda, jagada ja õppida koos inimestega kogu maailmas!

Mõtle sellele, et saad saata sõnumi või video kellegile teisel pool maailma vaid sekunditega. See on võrkude jõud!

### Lõbusad faktid võrkude kohta

- **Internet** on maailma suurim võrk, mis ühendab üle 5 miljardi seadme!
- **Wi-Fi** tähendab "Wireless Fidelity" ja võimaldab sul ühendada võrku ilma kaabliteta.
- **Esimene sõnum**, mis saadeti ARPANETi (interneti eelkäija) kaudu 1969. aastal, oli lihtsalt "LO", enne kui süsteem kokku jooksis!
- **Fiiberoptilised kaablid** suudavad edastada andmeid peaaegu valguse kiirusel, võimaldades ülikiiret internetiühendust.
- **Internetis on rohkem kui 1,7 miljardit veebisaiti**, ja see arv kasvab pidevalt.
- **Esimene e-kiri** saadeti Ray Tomlinsoni poolt 1971. aastal ja see oli lihtsalt testisõnum, mis ütles "QWERTYUIOP."
- **Üle 300 miljardi e-kirja** saadetakse iga päev üle maailma — rääkimata sellest, et me oleme ühendatud!
- **Termin "Wi-Fi"** ei tähenda tegelikult midagi. See on lihtsalt lööv kaubamärgi nimi!
- **"Pilv"** ei ole ainult taevas — see on serverite võrgustik üle kogu maailma, mis salvestab ja haldab andmeid veebis.

![Lihtne võrgu diagramm](/lectures/images/simple_network_diagram.png)

## Võrgu osad

- **Hostid**: Iga seade, nagu arvutid, telefonid või tahvelarvutid, võrgus nimetatakse hostiks.
- **Serverid ja kliendid**:
    - **Serverid** on nagu suured abimehed, mis salvestavad ja jagavad teavet teiste seadmetega.
    - **Kliendid** on seadmed, mis küsivad teavet, näiteks kui otsid veebisaiti.
- **Peer-to-Peer võrgud**: Mõnikord saavad seadmed jagada ja vastu võtta teavet otse üksteiselt. Seda nimetatakse peer-to-peer võrguks. See on lihtne, kuid mitte alati parim suurte võrkude jaoks.

---

## Võrkude topoloogia

- **Võrgu kaardid**:
    - Kasutame spetsiaalseid diagramme, mida nimetatakse **topoloogiateks**, et joonistada ja mõista võrke.
    - Need diagrammid näitavad, kuidas kõik seadmed on ühendatud ja kuidas teave liigub.
- **Võrgu meedia**:
    - See on "tee", mida mööda andmed liiguvad, näiteks kaablid või isegi nähtamatud lained (Wi-Fi ja Bluetooth).

### Levinud võrgutopoloogiad

| **Topoloogia**    | **Kirjeldus**                                             | **Eelised**                                   | **Puudused**                                  |
|-------------------|-----------------------------------------------------------|-----------------------------------------------|-----------------------------------------------|
| **Täht**          | Kõik seadmed ühenduvad keskse jaoturiga.                  | Lihtne hallata, seadmete lisamine/eemaldamine on lihtne. | Jaoturi rike põhjustab kogu võrgu rikke.      |
| **Rõngas**        | Seadmed on ühendatud ringikujuliselt.                     | Andmed liiguvad ühes suunas, vähendades kokkupõrkeid. | Kui üks seade ebaõnnestub, võib kogu võrk olla häiritud. |
| **Siin**          | Kõik seadmed jagavad ühte sideliini (siin).               | Lihtne paigutus, lihtne rakendada.            | Kui peamine kaabel ebaõnnestub, langeb kogu võrk.        |
| **Võrgusilm**     | Iga seade on ühendatud mitme teise seadmega.              | Väga usaldusväärne, pakub varundamist.        | Keeruline ja kallis seadistada.               |

## Võrkude tüübid

Võrgud on erineva kuju ja suurusega. Siin on peamised tüübid:

- **LAN (Local Area Network)**: Väike võrk, nagu sinu kodus või koolis.
- **WAN (Wide Area Network)**: Suur võrk, mis katab suurt ala, nagu internet, mis ühendab kogu maailma.
- **Metropolitan Area Network (MAN):** MAN on suurem kui LAN, kuid väiksem kui WAN, tavaliselt katab see linna või suurt ülikoolilinnakut. Mõtle sellele kui super-suurusele LANile terve linna jaoks.
- **Personal Area Network (PAN):** PANid on väikesed võrgud, nagu see, mis on sinu nutitelefoni ja Bluetooth kõrvaklappide vahel. Need katavad väga väikest ala, vaid mõne meetri ulatuses.
- **Storage Area Network (SAN):** SANid on spetsiaalsed võrgud, mis ühendavad salvestusseadmeid, nagu kõvakettad, serveritega. Neid kasutatakse sageli andmekeskustes, et hallata suures koguses andmeid.

![Võrkude tüüpide võrdlus](/lectures/images/network_types_comparison.png)

---

## Ühendamine internetiga

On erinevaid viise, kuidas internetti ühendada:
- **Kaabel**: Kasutades kaableid, nagu need, mis toovad elektri sinu koju.
- **DSL**: Eriline tüüpi internet, mis tuleb telefoniliinide kaudu.
- **Juhtmevaba**: Kasutades nähtamatuid laineid ühendamiseks, nagu Wi-Fi või mobiilne andmeside.

###

 Fiiberoptiline internet

Fiiberoptilised kaablid töötavad, edastades andmeid valgusimpulssidena läbi õhukeste klaaskiudude või plastikiudude. Erinevalt traditsioonilistest vaskkaablitest, mis kasutavad andmete edastamiseks elektrilisi signaale, suudavad fiiberoptilised kaablid edastada teavet palju suurematel kiirustel ja pikemate vahemaade taha ilma signaali kvaliteeti kaotamata.

Lõbus fakt: Üks fiiberoptilise kaabli kiud, mis on õhem kui inimese juus, suudab korraga kanda tuhandeid telefonikõnesid või internetiühendusi!

![Fiiberoptilise kaabli näide](/lectures/images/fiber_optic.png)

---

## Võrgu komponendid

* [Võrgu seadmed](/lectures/contents/network_devices/README.md)

Võrk ei ole lihtsalt hunnik omavahel ühendatud arvuteid. Sellel on erinevad osad, millest igaühel on oma konkreetne ülesanne.

### Lõppseadmed

Need on seadmed, mida sa kasutad igapäevaselt — lauaarvutid, sülearvutid, nutitelefonid, printerid. Need on andmete algus- ja lõpp-punktid, kui need võrgu kaudu liiguvad. Kui saadad e-kirja, on sinu arvuti see **lõppseade**, mis protsessi alustab, ja sinu sõbra telefon on lõppseade, mis selle vastu võtab.

![Lõppseadmed](/lectures/images/end_devices.png)

### Vahepealsed seadmed

Need seadmed on nagu võrgu liikluspolitseinikud. Nad tagavad, et sinu andmed liiguvad sujuvalt ja turvaliselt punktist A punkti B. Mõned levinud vahepealsed seadmed on:

- **Ruuterid:** Need otsustavad parima tee, mida mööda sinu andmed võrgu või interneti kaudu liiguvad.
  
- **Lülitid:** Need ühendavad omavahel mitmeid seadmeid samas võrgus, näiteks kõik arvutid LAN-is, ja tagavad, et andmed jõuavad sinna, kuhu need peavad.

- **Tulemüürid:** Tulemüürid on võrgu turvamehed, kes hoiavad soovimatu liikluse eemal ja kaitsevad sinu andmeid häkkerite eest.

![Vahepealsed seadmed](/lectures/images/intermediary_devices.png)

### Võrgu meedia

* [Liidesed ja kaablid](/lectures/contents/interfaces_and_cables/README.md)

Võrgu meedia on tee, mida mööda andmed liiguvad. On kolm peamist tüüpi:

- **Vaskkaablid:** Need on traditsioonilised kaablid, nagu Etherneti kaablid, mis kasutavad andmete edastamiseks elektrilisi signaale.
  
- **Fiiberoptilised kaablid:** Fiiberoptilised kaablid kasutavad andmete edastamiseks valgust, võimaldades neil liikuda uskumatult suurte kiirustega, mistõttu on need ideaalne pika vahemaa suhtlemiseks.

- **Juhtmevaba:** See on nähtamatu tee, mida mööda sinu andmed liiguvad, kui kasutad Wi-Fi ühendust. Kaablite asemel edastatakse andmed õhu kaudu raadiolainetega.

![Võrgu meedia tüübid](/lectures/images/network_media_types.png)

---

## Mis teeb hea võrgu?

- **Vigade taluvus**: Kui midagi läheb katki, saab võrk ikka töötada, kuna sellel on varuteed.
- **Mastaapsus**: Võrk saab hõlpsasti kasvada, lisades rohkem seadmeid.
- **Teenuse kvaliteet**: Võrk tagab, et olulised asjad, nagu videokõned, toimivad sujuvalt.
- **Turvalisus**: Võrgu turvalisuse tagamine pahatahtlike isikute eest, kes võivad soovida teavet varastada.

### Redundantsus ja kõrge saadavus

**Võrgu saadavuse** tagamiseks ja seisakute vältimiseks on olulised strateegiad nagu redundantsus ja kõrge saadavuse süsteemid.  
**Redundantsus** hõlmab mitme tee või varukoopiate seadistamist, mille kaudu andmed saavad liikuda, nii et kui üks tee ebaõnnestub, saab teine ​​üle võtta ilma võrgu häirimiseta.

**Kõrge saadavuse süsteemid** on loodud teenuste toimimise tagamiseks isegi riistvaratõrgete või hoolduse ajal, sageli kasutades **failover-mehhanisme**, koormuse tasakaalustamist ja klastrite moodustamist.

---

## Võrgus turvalisuse tagamine

Võrke tuleb kaitsta ohtude eest, nagu viirused ja häkkerid.

- **Turvalahendused**: Tulemüürid ja paroolid aitavad hoida võrku turvalisena.

### Täiustatud võrgu turvalisus

Võrkude kaitsmiseks keerukate ohtude eest on vaja täiustatud turvameetmeid.  
**Sissetungimise tuvastussüsteemid (IDS)** jälgivad võrgu liiklust kahtlaste tegevuste suhtes ja hoiatavad administraatoreid võimalike turvarikkumiste eest.

**Virtuaalsed privaatvõrgud (VPN-id)** loovad turvalisi, krüpteeritud ühendusi interneti kaudu, võimaldades kasutajatel juurdepääsu võrgule eemalt, ilma tundlikke andmeid paljastamata.

**Krüpteerimistehnikad** kaitsevad andmeid, muutes need koodiks, mida saavad dešifreerida ainult volitatud osapooled, kaitstes teavet volitamata juurdepääsu eest edastamise ajal.  
**Esimene teadaolev krüpteerimissüsteem** kasutati Julius Caesari poolt enam kui 2000 aastat tagasi salajaste sõnumite saatmiseks oma kindralitele, meetodit tuntakse nüüd kui "Caesari šifrit".

![Võrgu turvalisuse näide](/lectures/images/Network-Security.jpg)

---

## IT-eksperdiks saamine

Võrkude tundmaõppimine võib tulevikus viia lahedate töökohtadeni. On olemas spetsiaalsed sertifikaadid (nagu diplomid), mida saad omandada, näiteks CCNA, et näidata, et oled võrguasjades ekspert.

---

## Põhilised võrgu protokollid ja standardid

### Mis on võrgu protokollid?

Mõtle võrgu protokollidele kui liikluseeskirjadele, mida andmed järgivad. Need määratlevad, kuidas andmeid pakitakse, saadetakse, vastuvõetakse ja mõistetakse. Ilma nende reegliteta ei teaks seadmed, kuidas üksteisega suhelda.

### Olulised protokollid, mida peaksid teadma

- **TCP/IP**: See on interneti selgroog. TCP (Transmission Control Protocol) tagab, et andmed saadetakse usaldusväärselt, samas kui IP (Internet Protocol) tegeleb andmepakettide aadressimise ja marsruutimisega, et need jõuaksid õigesse sihtkohta.
  
- **Ethernet**: Ethernet on juhtmega võrkude standardprotokoll. See tagab, et andmed liiguvad sujuvalt üle kaablite, nagu need, mis on LAN-is.

![Protokollide vooskeem](/lectures/images/protocol_flowchart.png)

### Standardiorganisatsioonid

Selleks, et võrgud ja seadmed saaksid suhelda globaalselt, on meil standardiorganisatsioonid:

- **IEEE (Institute of Electrical and Electronics Engineers)**: See grupp kehtestab standardid paljudele tehnoloogiatele, sealhulgas Ethernetile.
  
- **IETF (Internet Engineering Task Force)**: IETF arendab ja edendab vabatahtlikke interneti standardeid, nagu TCP/IP, mis hoiavad interneti sujuvana.

---

## Võrguseadmete kasutamine; põhiline lüliti ja seadmete seadistamine

### Mis on Cisco IOS?

* [Sissejuhatus Cisco IOS CLI-sse](/lectures/contents/intro_to_cisco_cli/README.md)

Cisco IOS on operatsioonisüsteem (OS) spetsiaalsete seadmete, nagu ruuterid ja lülitid, jaoks, mis aitavad internetti ühendada. Nii nagu sinu arvutil on Windows või telefonil iOS või Android, on võrguseadmetel Cisco IOS.

### Erinevad võrgu operatsioonisüsteemid

Võrgu operatsioonisüsteemid (NOS) haldavad võrguseadmete, nagu ruuterid ja lülitid, riistvara ja tarkvara ressursse. Siin on mõned näited:

- **Juniperi JUNOS**: Tuntud oma stabiilsuse ja modulaarse disaini poolest, JUNOS-i kasutatakse Juniper Networksi seadmetes. Seda kiidetakse kasutajasõbraliku liidese ja tugeva turvalisuse omaduste poolest.

- **HP ProCurve**: Seda NOS-i kasutatakse HP võrgu toodetes. See pakub lihtsat integreerimist HP riistvaraga ja on mõeldud võrguülesannete lihtsaks haldamiseks.

- **MikroTiki RouterOS**: Tuntud oma paindlikkuse ja kulutõhususe poolest, kasutatakse RouterOS-i MikroTiki seadmetes. See pakub täiustatud funktsioone, nagu tulemüürid, VPN ja ribalaiuse haldamine, muutes selle populaarseks väikestes ja keskmise suurusega võrkudes.

### Kuidas see toimib

- **Shell** on nagu ekraan, mida näed mängides mängu. See võimaldab sul seadet juhtida.
- **Kernel** on nagu aju, mis paneb kõik kulisside taga tööle.
- **Riistvara** on tegelik seade, nagu ruuter või lüliti, mille sees on osad, nagu emaplaat ja mälu.

### Riistvaraspetsifikatsioonide mõistmine

Võrguseadmete, nagu ruuterid, lülitid ja serverid, puhul mängivad riistvaraspetsifikatsioonid olulist rolli nende jõudluse ja võimekuse määramisel. Olulised spetsifikatsioonid hõlmavad protsessorit (CPU), mälu ja liideste tüüpe, millest igaüks mõjutab, kui hästi seade suudab andmeid töödelda, liiklust hallata ja ühendusi tagada.

Esimene kaubanduslik Etherneti kiirus oli 10 Mbps, kuid tänapäeva täiustatud võrguseadmed suudavad hallata kiirusi kuni 400 Gbps!

![Cisco IOS-i juurdepääs](/lectures/images/cisco_ios_access.png)

---

## Käsurea kasutamine

Cisco seadmetel ei ole ilusat ikoonidega ekraani nagu sinu arvutil. Selle asemel kasutad spetsiaalset käsurida, mis on nagu salakoodide kirjutamine, et asjad juhtuksid.

### Käsureale juurdepääsu viisid:

- **Konsoolikaabel**: See on nagu spetsiaalne kaabel, mille ühendad otse seadistamiseks.
- **Secure Shell (SSH)**: See võimaldab sul seadet eemalt, kuid turvaliselt juhtida.
- **Telnet**: See võimaldab samuti eemalt juhtimist, kuid see pole turvaline, seega ei kasutata seda enam eriti.

### Liikumine käsusüsteemis

On kaks peamist režiimi, mida kasutad:
- **User Exec Mode**: See on põhirežiim, kus saad teha lihtsaid asju. Näed `>` sümbolit.
- **Privileged Exec Mode**: See režiim võimaldab teha keerukamaid asju. Näed `#` sümbolit.
- **Global Configuration Mode**: See on koht, kus saad muuta seadme toimimist. Näed `#` koos mõne lisasõnaga, nagu `Switch(config)#`.

### Käskude sisestamine

Kui sisestad käske, pead olema täpne. Näiteks, kui tahad kontrollida, kas seade töötab, võid kirjutada:

```
ping 192.168.10.5
```
See ütleb seadmele, et kontrollida, kas teine seade sellel aadressil on saavutatav.

### Abi ja otseteed:

- Kui unustad käsu, võid pärast sõna kirjutada `?`, ja see näitab sulle, mida saad edasi teha.
- Samuti saad kasutada otseteid, et säästa aega. Näiteks, `configure` asemel võid lihtsalt kirjutada `conf`!

### Klaviatuuri kasutamine

- **Tabulaator (Tab)**: Aitab käskude täitmist, kui oled neid juba alustanud.
- **Nooleklahvid**: Liiguta kursorit vigade parandamiseks või käskude kordamiseks.
- **Ctrl + C**: Peatab käimasoleva tegevuse ja viib sind tagasi põhiekraanile.
- **Ctrl + Shift + 6**: See on nagu "paus" nupp. See peatab tegevuse, kui miski võtab liiga kaua aega.

---

## Oma võrguseadmete seadistamine; põhiline seadmete seadistamine

### Seadmete nimetamine

Iga võrguseade, nagu ruuter või lüliti, vajab spetsiaalset nime, et saaksid selle hõlpsasti leida. Ära nimeta oma seadmeid "Mickey" või "Goofy" – kasuta nimesid, mis ütlevad, kus need asuvad, näiteks "SW-Floor-1" (Lüliti 1. korrusel).

### Nimetamisreeglid:

- Nimi peab algama tähega, mitte numbriga.
- Selles ei tohiks olla tühikuid, kuid võid kasutada sidekriipsu (-).
- Nimi peaks olema vähem kui 64 tähemärki pikk.

### Standardne nimetamise konventsioon

- Standardne nimetamise konventsioon on suurtes võrkudes ühtsuse ja lihtsa haldamise jaoks oluline. See aitab kõigil seadmeid ja nende rolle kiiresti tuvastada, muutes tõrkeotsingu ja hoolduse tõhusamaks. Näiteks, lüliti nimetamine "TLN-SW1" viitab sellele, et see on esimene lüliti Tallinnas, muutes selle asukoha ja eesmärgi selgeks.

### Tugevate paroolide seadistamine

Paroolid hoiavad sinu seadmeid turvalisena inimeste eest, kes ei peaks neid kasutama.

![Seadme seadistamine](/lectures/images/device_configuration.png)

---

## Võrguprotokollide õppimine; protokollide ja mudelite mõistmine

### Miks on suhtlemiseks vaja reegleid?

Nii nagu inimesed peavad rääkima sama keelt, et üksteisest aru saada, peavad ka arvutid järgima konkreetseid reegleid, mida nimetatakse **protokollideks**, et suhelda.

Kujuta ette, kui üks inimene räägib inglise keelt ja teine prantsuse keelt – nad ei mõistaks üksteist, kui nad ei lepiks kokku, et räägivad sama keelt!

### Suhtlemise põhitõed

Iga suhtluse jaoks on vaja:
- **Saatjat** (isik või seade, mis sõnumi saadab).
- **Vastuvõtjat** (isik või seade, mis sõnumi saab).
- **Meediumit** (kuidas sõnum edastatakse, näiteks kaablite või Wi-Fi kaudu).

### Andmeedastusmeetodid

Andmeedastusmeetodid määravad, kuidas andmed seadmete vahel liiguvad. Siin on kiire ülevaade kolmest peamisest tüübist:

- **Simplex**: Andmed liiguvad ainult ühes suunas. Näiteks on televisiooniülekanne, kus signaal liigub jaamast sinu telerisse ilma vastussignaalita.
  
- **Half-Duplex**: Andmed liiguvad mõlemas suunas, kuid mitte samaaegselt. Mõtle raadiosaatjale, kus üks inimene räägib, samal ajal kui teine kuulab.
  
- **Full-Duplex**: Andmed liiguvad mõlemas suunas samaaegselt. See on nagu telefonikõne, kus mõlemad inimesed saavad korraga rääkida ja kuulata.

---

## Mis on protokollid?

**Protokollid** on reeglid, mida seadmed järgivad, et omavahel rääkida.

Need aitavad:
- **Kodeerimisel**: Sõnumi muutmine vorminguks, mida saab saata, näiteks sõnade muutmine digitaalseteks signaalideks.
- **Formaatimisel**: Veendudes, et sõnum on korralikult organiseeritud, et seda saaks mõista.
- **Ajastamisel**: Tagades, et sõnumeid saadetakse ja võetakse vastu õige kiirusega.
- **Kohaletoimetamisel**: Otsustades, kas sõnum läheb ühele seadmele, rühmale või kõigile.

### Vigade tuvastamine ja parandamine

Vigade tuvastamine ja parandamine on võtmetähtsusega, et andmed edastataks võrgus täpselt. Kui andmed liiguvad, võivad need saada häirete tõttu vigu.  
Nende vigade avastamiseks kasutavad protokollid meetodeid nagu kontrollsummad või CRC, mis aitavad avastada probleeme andmetes.

Kui viga leitakse, saab süsteem kas küsida andmete uuesti saatmist või proovida seda automaatselt parandada, kasutades andmetega kaasa saadetud lisateavet. Need protsessid hoiavad meie suhtluse usaldusväärse ja täpse.

Vigade tuvastamise meetodeid, nagu Hamming-koodid, on kasutatud alates 1940. aastatest ja need on endiselt olulised tänapäeva tehnoloogias!

### Sõnumite edastamise tüübid

- **Unicast**: Sõnumi saatmine ühelt seadmelt ühele teisele seadmele.
- **Multicast**: Sõnumi saatmine ühelt seadmelt mitmele seadmele.
- **Broadcast**: Sõnumi saatmine kõigile võrgu seadmetele.

### Anycast-suhtlus

Anycast-suhtlus on meetod, kus üks sõnum saadetakse mitmele vastuvõtjale, kuid see jõuab ainult lähima või optimaalseima sihtkohani. Seda kasutatakse sageli koormuse tasakaalustamiseks ja võrgu jõudluse parandamiseks.

### Erinevad protokollide tüübid

On palju erinevaid protokolle, millest igaühel on oma ülesanne:
- **Võrgu suhtlusprotokollid**: Aitavad seadmetel võrgu kaudu suhelda.
- **Turvaproktokollid**: Hoiavad andmeid turvalisena, veendudes, et ainult õiged inimesed näevad neid.
- **Marsruutimisprotokollid**: Aitavad leida parima tee, mida mööda andmed saavad liikuda.
- **Teenuste avastamise protokollid**: Aitavad seadmetel leida üksteist võrgus.

### Levinud võrgu protokollid

| **Protokoll** | **Täisnimi**                        | **Eesmärk**                                                                 |
|---------------|-------------------------------------|------------------------------------------------------------------------------|
| **HTTP**      | Hypertext Transfer Protocol         | Kasutatakse veebilehtede edastamiseks internetis.                            |
| **FTP**       | File Transfer Protocol              | Kasutatakse failide edastamiseks arvutite vahel.                             |
| **DNS**       | Domain Name System                  | Tõlgib domeeninimed IP-aadressideks.                                         |
| **SMTP**      | Simple Mail Transfer Protocol       | Kasutatakse e-kirjade saatmiseks ühelt serverilt teisele.                    |

**Lõbus fakt**: DNS-süsteemi nimetatakse sageli interneti "telefoniraamatuks", kuna see seob domeeninimed vastavate IP-aadressidega!

### Kuidas protokollid koos töötavad

Paljud protokollid töötavad koos, et tagada sujuv toimimine.

Näiteks:
- **HTTP**: Aitab veebilehti laadida.
- **TCP**: Tagab, et andmed jõuavad vigadeta kohale.
- **IP**: Leiab parima marsruudi, mida mööda andmed saavad liikuda.
- **Ethernet**: Ühendab seadmeid kaablite või Wi-Fi kaudu.

### Mis on protokollikomplekt?

**Protokollikomplekt** on rühm protokolle, mis töötavad koos suhtlusülesannete täitmiseks.

Kõige levinum on **TCP/IP**, mis on interneti selgroog.

### TCP/IP areng

Arutlege TCP/IP ajaloo ja arengu üle, sealhulgas selle rolli üle kaasaegse interneti arengus.

### Andmete saatmine võrgu kaudu

Kui saadad sõnumi, näiteks laadid veebilehte, jagatakse andmed väikesteks tükkideks, pakitakse kokku ja saadetakse üle võrgu.

Vastuvõttev seade paneb need siis uuesti kokku, et saaksid veebilehte näha.

### Kes teeb reeglid?

On palju organisatsioone, kes loovad ja hooldavad neid reegleid (protokolle), tagades, et kõik toimib koos.

Mõned neist on:
- **IETF**: Nemad tagavad, et internet toimiks sujuvalt.
- **ICANN**: Nad aitavad hallata veebisaitide nimesid ja IP-aadresse.
- **IEEE**: Nad loovad standardid elektroonikaseadmete jaoks.

Internet Engineering Task Force (IETF) on võtmetähtsusega organisatsioon, mis vastutab interneti toimimise tagamiseks vajalike standardite ja protokollide arendamise ja hooldamise eest. IETF ühendab ülemaailmse inseneride, võrgu disainerite ja teadlaste kogukonna, kes teevad koostööd tehniliste standardite, nagu HTTP, TCP/IP ja DNS, loomisel ja täiustamisel.

IETF-i töö avaldatakse dokumentides, mida nimetatakse "RFC-deks" (Request for Comments), mis toimivad interneti tehnoloogiate sinikavadena!

![Protokolli andmevoog](/lectures/images/protocol_data_flow.png)

---

## Võrgukihtide ja -mudelite mõistmine; kihid ja mudelid

### Miks me kasutame kihte?

Võrgud võivad olla keerulised, kuid kihid aitavad meil jagada suure andmete saatmise ülesande väiksemateks, lihtsamateks ülesanneteks.

Igal kihil on konkreetne ülesanne, nagu koogi küpsetamine, glasuuri lisamine ja kaunistamine!

### Kihilise arhitektuuri eelised

Kihiline arhitektuur võrkudes on kasulik mitmel põhjusel:

- **Modulaarsus**: Kujuta ette, et tahad oma võileivas juustu vahetada. Sa saad seda teha, ilma et peaksid puudutama leiba või liha. Võrkudes tähendab see, et saad uuendada ühte osa, ilma et see häiriks teisi osi.
  
- **Mastaapsus**: Nii nagu saad teha suurema võileiva, lisades rohkem kihte, võivad võrgud kasvada, lisades rohkem kihte või osi, ilma et peaksid kogu asja muutma.
  
- **Lihtne tõrkeotsing**: Kui midagi on sinu võileivas valesti, näiteks halb salatileht, saad selle hõlpsasti leida ja parandada. Võrkudes, kui on probleem, on lihtsam leida ja parandada see vaid ühes kihis.

### OSI mudel (7 kihti):

1. **Füüsiline**: Saadab elektrisignaale (nagu tulede sisse ja välja lülitamine).
2. **Andmeside**: Tagab, et andmed on õiges vormingus.
3. **Võrk**: Otsustab, milline on parim tee, mida mööda andmed liiguvad.
4. **Transpordikiht**: Tagab, et andmed jõuavad turvaliselt kohale.
5. **Seanss**: Haldab ühendust seadmete vahel.
6. **Esitluskiht**: Valmistab andmed ette, et rakendus saaks neid kasutada.
7. **Rakenduskiht**: Suhtleb otse tarkvaraga, mida kasutad, nagu veebibrauserid.

### TCP/IP mudel (4 kihti):

1. **Võrgujuurdepääs**: Ühendab füüsilise ja andmesidekihid (hõlmab riistvara).
2. **Internet**: Hõlmab võrgu kihi ülesandeid (suunab andmed võrkude kaudu).
3. **Transpordi**: Sama mis OSI transpordikiht.
4. **Rakenduskiht**: Ühendab kolm ülemist OSI kihti (rakenduste ja tarkvara jaoks).

### OSI ja TCP/IP mudelite võrdlus

* [OSI mudel ja TCP/IP komplekt](/lectures/contents/osi_model_and_tcp_ip_suite/README.md)

| **Aspekt**          | **OSI mudel**                                 | **TCP/IP mudel**                                |
|---------------------|------------------------------------------------|-------------------------------------------------|
| **Kihid**           | 7 kihti                                        | 4 kihti                                         |
| **Kasutus**         | Peamiselt õpetamiseks ja kontseptuaalseks mõistmiseks| Laialdaselt kasutatav reaalses internetis |
| **Kihid**           | Füüsiline, andmeside, võrk, transport, seanss, esitlus, rakendus | Link, Internet, Transport, Rakendus |
| **Rakendamine**     | Pole praktikas täielikult rakendatud           | Interneti ja enamiku võrkude alus              |

### OSI mudeli meeldejätmine

Lõbus viis OSI kihtide meeldejätmiseks on lause: **"Palun Ära Too Soolast Pizza Ära."** Iga sõna aitab sul kihte järjekorras meelde jätta.

### Kuidas andmed kihtides liiguvad?

Kui andmeid saadetakse võrgus, jagatakse need väiksemateks osadeks, mida nimetatakse segmentideks.

Need segmendid pannakse kokku (või multipleksitakse) teiste andmetega, et need kiiremini liiguksid.

### Andmete kapseldamine

Kui andmed liiguvad kihtide kaudu alla, lisab iga kiht oma teabe juurde. Seda nimetatakse kapseldamiseks.

Kui andmed jõuavad sihtkohta, eemaldatakse kihid, nagu kingituse lahtipakkimine, kuni algsed andmed on nähtavad.

### Andmete adresseerimine võrgus

Igal andmel on vaja aadressi, et teada, kuhu see läheb. On kaks peamist tüüpi:
- **IP-aadress (3. kiht)**: Näitab võrgule, kuhu andmed peaksid globaalsetes mastaapides minema (nagu postiaadress).
- **MAC-aadress (2. kiht)**: Näitab, milline konkreetne seade kohalikus võrgus peaks andmed vastu võtma (nagu maja number).

![Protokollid tegevuses](/lectures/images/protocols_in_action.png)

* [Ethernet LAN-i lülitamine](/lectures/contents/ethernet_lan_switching/README.md)
* [IPv4 aadressimine](/lectures/contents/ipv4_addressing/README.md)

### IPv4 vs. IPv6

IPv4 ja IPv6 on mõlemad versioonid Interneti protokollist (IP), mida kasutatakse seadmete tuvastamiseks võrgus, kuid neil on olulised erinevused:

| **Aspekt**           | **IPv4**                                      | **IPv6**                                                 |
|----------------------|-----------------------------------------------|----------------------------------------------------------|
| **Aadressi pikkus**  | 32-bitine (nt 192.168.1.1)                    | 128-bitine (nt 2001:0db8:85a3::8a2e:0370:7334)           |
| **Aadresside arv**   | ~4,3 miljardit aadressi                       | 340 undecillion aadressi (tohutult suur number!)         |
| **Vorming**          | Punktidega kümnendkohaline vorming            | Kuueteistkümnendkohaline vorming koos koolonitega        |
| **IPv6 vajadus**     | Piiratud aadressiruum, aadressid otsa saamas  | Suur aadressiruum, et mahutada kasvavat internetti ühendatud seadmete arvu |

IPv4 4,3 miljardit aadressi tundus 1980. aastatel küllaldasena, kuid nutitelefonide, IoT-seadmete ja muu plahvatusliku kasvuga loodi IPv6, et käsitleda internetti ühendatud seadmete arvu tohutut kasvu!

### Mis toimub erinevates võrkudes?

Kui kaks seadet, nagu sinu arvuti ja printer, asuvad samas kohalikus võrgus (näiteks sinu kodus), suhtlevad nad üksteisega kasutades MAC-aadresse. Mõtle MAC-aadressile kui maja numbrile – see aitab seadmetel üksteist kiiresti leida, kui need on lähedal.

Aga kui kaks seadet on erinevates võrkudes (näiteks sinu kodus olev arvuti ja internetis olev server), toimivad asjad veidi teisiti.  
Nad kasutavad IP-aadresse andmete saatmiseks üle interneti.  
IP-aadress on nagu tänava aadress, mis aitab sinu andmetel leida tee õigele võrgule. Kui andmed jõuavad õigele võrgule, kasutavad need MAC-aadressi, et leida konkreetne seade, kuhu need peavad jõudma.

![OSI vs TCP/IP mudelid](/lectures/images/osi_vs_tcpip_models.png)

* [Switch liidesed](/lectures/contents/switch_interfaces/README.md)
* [IPv4 päis](/lectures/contents/ipv4_header/README.md)
* [Marsruutimise alused](/lectures/contents/routing_fundamentals/README.md)
* [Staatiline marsruutimine](/lectures/contents/static_routing/README.md)

---
