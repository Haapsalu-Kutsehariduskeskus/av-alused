> [!TIP]
>[Networking Today](https://www.youtube.com/watch?v=TBAvNZIcdVQ&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=2)
>[Basic Switch and End Device Configuration - Part 1](https://www.youtube.com/watch?v=4fMoxkiTEjc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=2)
>[Basic Switch and End Device Configuration - Part 2](https://www.youtube.com/watch?v=ruainw-2Y28&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=3)
>[Protocols and Models - Part 1](https://www.youtube.com/watch?v=VqGIeL0jRJI&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=4)
>[Protocols and Models - Part 2](https://www.youtube.com/watch?v=agX0G-9JTpM&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=5)


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

Võrgud on seadmete kogumid, mis võimaldavad teabe jagamist ja suhtlemist. Kõik võrgus olevad seadmed, olgu need siis arvutid, nutitelefonid või muud tehnilised vahendid, moodustavad terviku, kus iga komponent täidab kindlat rolli.

- **Hostid**: Iga seade, nagu arvutid, telefonid või tahvelarvutid, võrgus nimetatakse hostiks.
- **Serverid ja kliendid**:
    - **Serverid** on nagu suured abimehed, mis salvestavad ja jagavad teavet teiste seadmetega.
    - **Kliendid** on seadmed, mis küsivad teavet, näiteks kui otsid veebisaiti.
- **Peer-to-Peer võrgud**: Mõnikord saavad seadmed jagada ja vastu võtta teavet otse üksteiselt. Seda nimetatakse peer-to-peer võrguks. See on lihtne, kuid mitte alati parim suurte võrkude jaoks.

---

## Võrkude topoloogia

Võrgu struktuuri ja ühenduste visualiseerimine on oluline, et mõista, kuidas seadmed üksteisega suhtlevad ja andmeid vahetavad. Selleks kasutatakse võrguskeeme ja erinevat tüüpi ühenduste meediat.

- **Võrgu kaardid**:
    - Kasutame spetsiaalseid diagramme, mida nimetatakse **topoloogiateks**, et joonistada ja mõista võrke.
    - Need diagrammid näitavad, kuidas kõik seadmed on ühendatud ja kuidas teave liigub.
- **Võrgu meedia**:
    - See on "tee", mida mööda andmed liiguvad, näiteks kaablid või isegi nähtamatud lained (Wi-Fi ja Bluetooth).

### Levinud võrgutopoloogiad

Võrk on kontaktpunktide kogum, mille kaudu vahetatakse informatsiooni võrku ühendatud arvutite vahel. Kontaktpunktideks nimetatakse kahe või enama võrguharu ühenduspunkti või mistahes võrguharu lõpp-punkti.
Võrkusid liigitatakse mitmel moel, võttes aluseks mõnd iseloomulikku omadust.
Üks variant on liigitamine topoloogia ehk arvutisüsteemi geomeetrilise korralduse järgi.


| **Topoloogia**    | **Kirjeldus**                                             | **Eelised**                                   | **Puudused**                                  |
|-------------------|-----------------------------------------------------------|-----------------------------------------------|-----------------------------------------------|
| **Täht**          | Kõik seadmed ühenduvad keskse jaoturiga.                  | Lihtne hallata, seadmete lisamine/eemaldamine on lihtne. | Jaoturi rike põhjustab kogu võrgu rikke.      |
| **Rõngas**        | Seadmed on ühendatud ringikujuliselt.                     | Andmed liiguvad ühes suunas, vähendades kokkupõrkeid. | Kui üks seade ebaõnnestub, võib kogu võrk olla häiritud. |
| **Siin**          | Kõik seadmed jagavad ühte sideliini (siin).               | Lihtne paigutus, lihtne rakendada.            | Kui peamine kaabel ebaõnnestub, langeb kogu võrk.        |
| **Võrgusilm**     | Iga seade on ühendatud mitme teise seadmega.              | Väga usaldusväärne, pakub varundamist.        | Keeruline ja kallis seadistada.               |

## Võrkude tüübid

Võrgud võivad olla väga erineva suuruse ja ulatusega, sõltuvalt sellest, kui palju seadmeid nad ühendavad ja millist ala nad katavad. Siin on mõned peamised võrgu tüübid:

- **LAN (Local Area Network)**: Väike võrk, nagu sinu kodus või koolis. LAN võimaldab seadmetel omavahel kiiresti ja efektiivselt suhelda.
- **WAN (Wide Area Network)**: Laiapõhjaline võrk, mis katab suuri alasid, näiteks riike või isegi mandreid. WAN on suurem kui LAN ja internet on suurim WAN, mis ühendab kogu maailma
- **Metropolitan Area Network (MAN):** MAN katab tavaliselt linna või suurt piirkonda, näiteks ülikoolilinnakut. See on suurem kui LAN, kuid väiksem kui WAN, pakkudes laiaulatuslikku võrguühendust kindlas geograafilises piirkonnas.
- **Personal Area Network (PAN):** PAN on väike võrk, mis ühendab isiklikke seadmeid, näiteks nutitelefoni ja Bluetooth kõrvaklappe. PAN-i ulatus on väga piiratud, ulatudes tavaliselt vaid mõne meetri kaugusele.
- **Storage Area Network (SAN):** SANid on spetsialiseeritud võrgud, mis ühendavad salvestusseadmeid, nagu serverid ja kõvakettad. Neid kasutatakse andmekeskustes, et hallata suuri andmemahte ja tagada kiire andmevahetus salvestussüsteemide vahel.

![Võrkude tüüpide võrdlus](/lectures/images/network_types_comparison.png)

---

## Ühendamine internetiga

Internetiga saab ühenduda mitmel erineval viisil, olenevalt kasutatavast tehnoloogiast ja kättesaadavusest. Siin on mõned peamised viisid:
- **Kaabel**: Kaabelühendus kasutab füüsilisi juhtmeid, mis võivad olla sarnased nendele, mis toovad elektri sinu koju. Kaabliga internetiühendused, nagu kaabelmodemid, pakuvad tavaliselt kiiret ja stabiilset ühendust, eriti kodu- või kontorivõrkudes.
- **DSL**: (Digital Subscriber Line): DSL kasutab tavalisi telefoniliine, et edastada internetiühendust. Kuigi see põhineb telefonitehnoloogial, saab DSL-i kaudu pakkuda suhteliselt kiiret internetti, ilma et tavalised telefonikõned oleksid häiritud.
- **Juhtmevaba**: Juhtmevabad ühendused, nagu Wi-Fi ja mobiilne andmeside (4G, 5G), kasutavad nähtamatuid raadiosignaale andmete edastamiseks. Wi-Fi ühendab seadmeid traadita ruuteriga kohalikus võrgus, samas kui mobiilne andmeside võimaldab internetti pääseda läbi mobiilsidevõrkude peaaegu kõikjal, kus on leviala.

###

 Fiiberoptiline internet

Fiiberoptiline internet kasutab andmete edastamiseks valgusimpulsse, mis liiguvad läbi õhukeste klaas- või plastikiudude. Erinevalt vaskkaablitest, mis kannavad elektrilisi signaale, võimaldab fiiberoptiline tehnoloogia andmeid edastada märkimisväärselt suurematel kiirustel ja palju pikemate vahemaade taha, ilma et signaali kvaliteet väheneks.

Lõbus fakt: Üks fiiberoptilise kaabli kiud, mis on õhem kui inimese juus, suudab korraga kanda tuhandeid telefonikõnesid või internetiühendusi!

![Fiiberoptilise kaabli näide](/lectures/images/fiber_optic.png)

---

## Võrgu komponendid

* [Võrgu seadmed](/lectures/contents/network_devices/README.md)

Võrk ei ole lihtsalt rühm omavahel ühendatud seadmeid. Selle koosseisus on erinevad komponendid, millest igaühel on oma spetsiifiline ülesanne, mis tagab võrgu tõrgeteta toimimise ja andmete edastamise.

### Lõppseadmed (Hostid)

Need on seadmed, mida sa kasutad igapäevaselt — lauaarvutid, sülearvutid, nutitelefonid, printerid. Need on andmete algus- ja lõpp-punktid, kui need võrgu kaudu liiguvad. Kui saadad e-kirja, on sinu arvuti see **lõppseade**, mis protsessi alustab, ja sinu sõbra telefon on lõppseade, mis selle vastu võtab.

![Lõppseadmed](/lectures/images/end_devices.png)

### Vahepealsed seadmed

Need seadmed on nagu võrgu liikluspolitseinikud. Nad tagavad, et sinu andmed liiguvad sujuvalt ja turvaliselt punktist A punkti B. Mõned levinud vahepealsed seadmed on:

- **Ruuterid:** Need otsustavad parima tee, mida mööda sinu andmed võrgu või interneti kaudu liiguvad.
  
- **Kommutaatorid:** Need ühendavad omavahel mitmeid seadmeid samas võrgus, näiteks kõik arvutid LAN-is, ja tagavad, et andmed jõuavad sinna, kuhu need peavad.

- **Tulemüürid:** Tulemüürid on võrgu turvamehed, kes hoiavad soovimatu liikluse eemal ja kaitsevad sinu andmeid häkkerite eest.

![Vahepealsed seadmed](/lectures/images/intermediary_devices.png)

### Võrgu meedia

* [Liidesed ja kaablid](/lectures/contents/interfaces_and_cables/README.md)

Võrgu meedia on füüsiline või traadita tee, mida mööda andmed liiguvad seadmete vahel. Andmete edastamiseks kasutatakse erinevat tüüpi meediume, mis sõltuvad võrgu vajadustest ja ulatusest. Peamised võrgu meedia tüübid on:

- **Vaskkaablid:** Traditsioonilised kaablid, nagu Etherneti kaablid, mis kannavad andmeid elektriliste signaalidena. Vaskkaablid on laialt levinud ja sobivad hästi lühemate vahemaade jaoks, pakkudes stabiilset ja usaldusväärset ühendust.
  
- **Fiiberoptilised kaablid:** Fiiberoptiline tehnoloogia kasutab valgusimpulsse andmete edastamiseks läbi klaas- või plastikiudude. See võimaldab andmete kiiret ja kvaliteetset liikumist isegi pikkadel vahemaadel, muutes fiiberoptilise kaabli ideaalseks suuremahuliste andmeedastuste ja pika vahemaa võrkude jaoks.

- **Juhtmevaba:** Juhtmevaba side, nagu Wi-Fi ja Bluetooth, kasutab raadiolaineid andmete edastamiseks õhu kaudu. See võimaldab seadmete ühendamist ilma kaabliteta, pakkudes kasutajatele suuremat liikumisvabadust ja lihtsamat seadistamist, eriti kodu- ja kontorivõrkudes.

![Võrgu meedia tüübid](/lectures/images/network_media_types.png)

---

## Mis teeb hea võrgu?

Hea võrk on rohkem kui lihtsalt seadmete kogum – sellel on omadusi, mis tagavad, et see töötab sujuvalt, turvaliselt ja vastupidavalt. Siin on mõned võtmetegurid, mis iseloomustavad hästi toimivat võrku:

- **Vigade taluvus**: Kui midagi läheb katki, saab võrk ikka töötada, kuna sellel on varuteed.
- **Mastaapsus**: Võrk saab hõlpsasti kasvada, lisades rohkem seadmeid.
- **Teenuse kvaliteet**: (QoS) Võrk tagab, et olulised asjad, nagu videokõned, toimivad sujuvalt.
- **Turvalisus**: Võrgu turvalisuse tagamine pahatahtlike isikute eest, kes võivad soovida teavet varastada.

### Käideldavus (redundancy) ja kõrge saadavus

Võrgu töökindluse ja pideva toimimise tagamiseks kasutatakse kahte olulist strateegiat: käideldavus ja kõrge saadavusega süsteeme. Need aitavad vältida võrgu seisakuid ja tagavad teenuste kättesaadavuse ka rikete korral.

**Käideldavus** tähendab mitme tee või varusüsteemide loomist, et andmed saaksid liikuda ka siis, kui üks ühendus või komponent ebaõnnestub. Näiteks võib võrguühenduses olla mitu marsruuterit või serverit, mis suudavad vajadusel üksteist asendada. Kui üks komponent lakkab töötamast, võtab teine üle, hoides võrgu toiminguid katkestusteta.

**Kõrge saadavuse süsteemid** (availability) Kõrge saadavuse süsteemid on loodud tagama, et teenused jäävad kättesaadavaks ka rikke või hoolduse ajal. Need süsteemid kasutavad sageli failover-mehhanisme, mis suunavad liikluse automaatselt töötavale varusüsteemile, ja koormuse tasakaalustamist, et jaotada töökoormus mitme serveri või ressursi vahel. Klastrite moodustamine võimaldab mitme süsteemi töötamist koos, tagades kõrge saadavuse ja töökindluse ka ootamatute probleemide korral.

---

## Võrgus turvalisuse tagamine

Võrkude kaitsmine ohtude, nagu viirused, pahavara ja häkkerid, on äärmiselt oluline, et tagada andmete ja teenuste turvalisus.

### Turvalahendused

Võrguturvalisuse tagamiseks kasutatakse erinevaid meetmeid:

- **Tulemüürid**: Tulemüürid toimivad kaitsebarjääridena, blokeerides volitamata juurdepääsu võrgule ja lubades ainult usaldusväärseid ühendusi.
- **Paroolid ja autentimine**: Paroolid ja muud autentimismeetodid, nagu kahefaktoriline autentimine (2FA), tagavad, et ainult volitatud kasutajad saavad võrgule või tundlikele andmetele ligi pääseda.

Kaitsmaks võrke keerukamate ja püsivamate ohtude eest, on vajalikud arenenud turvameetmed, mis suudavad reageerida erinevatele rünnakutele ja kaitsta tundlikke andmeid.

### Täiustatud turvameetmed

- **Sissetungimise tuvastussüsteemid (IDS)**: IDS-id jälgivad pidevalt võrgu liiklust, et tuvastada kahtlasi või ebatavalisi tegevusi, mis võivad viidata küberrünnakule. Need süsteemid hoiatavad administraatoreid võimalikest turvarikkumistest, võimaldades neil kiiresti reageerida ja ennetada kahju.

- **Virtuaalsed privaatvõrgud (VPN-id)**: VPN-id loovad turvalised ja krüpteeritud ühendused interneti kaudu, mis võimaldavad kasutajatel kaugjuurdepääsu ettevõtte või organisatsiooni võrgule ilma tundlikke andmeid ohtu seadmata. VPN-id tagavad, et kõik andmed on kaitstud, isegi kui neid edastatakse avalike võrkude kaudu.

- **Krüpteerimistehnikad**: Krüpteerimine kaitseb andmeid, muutes need koodiks, mida saavad lugeda ja dešifreerida ainult volitatud osapooled. See kaitseb teavet volitamata juurdepääsu eest, eriti kui andmeid edastatakse üle interneti või hoitakse pilveteenustes. Krüpteerimine on üks kõige tõhusamaid viise tundliku teabe turvaliseks hoidmiseks.

### Ajalooline fakt

- **Esimene teadaolev krüpteerimissüsteem**: Krüpteerimist on kasutatud juba tuhandeid aastaid. Üks varasemaid teadaolevaid krüpteerimismeetodeid oli *Caesari šiffer*, mida kasutas Julius Caesar oma sõnumite salastamiseks. See meetod asendas kirjad tähestikus kindla arvu positsioonidega, muutes sõnumi arusaamatuks, kui saaja ei teadnud nihet.

![Võrgu turvalisuse näide](/lectures/images/Network-Security.jpg)

---

## IT-eksperdiks saamine

Võrkude tundmaõppimine ja nendega töötamine võib avada ukse põnevatele ja hästi tasustatud töökohtadele IT-valdkonnas. Selleks, et näidata oma oskusi ja teadmisi, on olemas spetsiaalsed sertifikaadid, mis tõendavad sinu pädevust võrgu- ja IT-valdkonnas. Üks populaarsemaid neist on CCNA (Cisco Certified Network Associate) sertifikaat, mis tõestab, et oled võrguadministraatorina pädev ja oskad seadistada, hallata ja lahendada probleeme võrkudes.

Sellised sertifikaadid, nagu CCNA, annavad sulle konkurentsieelise ja näitavad tööandjatele, et oled võrguasjades ekspert. Lisaks on palju teisi sertifikaate ja koolitusprogramme, mis aitavad sul arendada oma oskusi ja valmistavad sind ette eduka karjääri jaoks IT-maailmas.

---

## Põhilised võrgu protokollid ja standardid


### Mis on võrgu protokollid?


Võrgu protokollid on nagu liikluseeskirjad, mida andmed peavad järgima, et need saaksid tõhusalt ja turvaliselt liikuda seadmete vahel. Protokollid määravad kindlaks, kuidas andmeid pakitakse, saadetakse, vastu võetakse ja tõlgendatakse. Ilma nende eeskirjadeta ei oleks seadmetel võimalik omavahel suhelda.


### Olulised protokollid, mida peaksid teadma


- **TCP/IP**: See on interneti selgroog ja kõige olulisem protokollide komplekt. TCP (Transmission Control Protocol) tagab, et andmed edastatakse usaldusväärselt ja õiges järjekorras. IP (Internet Protocol) tegeleb andmepakettide aadressimise ja marsruutimisega, tagades, et need jõuavad õigesse sihtkohta.
  
- **Ethernet**: Ethernet on juhtmega võrgu standardprotokoll. Seda kasutatakse kohalikus võrgus (LAN) andmete liigutamiseks füüsiliste kaablite kaudu. Ethernet tagab, et andmed liiguvad tõhusalt ja sujuvalt üle kaablite.

![Protokollide vooskeem](/lectures/images/protocol_flowchart.png)


### Standardiorganisatsioonid

Võrkude ja seadmete ülemaailmse suhtlemise võimaldamiseks on meil standardiorganisatsioonid, mis loovad reeglid ja juhised, et kõik süsteemid oleksid ühilduvad ja töötaksid ühtselt.

- **IEEE (Institute of Electrical and Electronics Engineers)**: IEEE kehtestab standardid paljudele tehnoloogiatele, sealhulgas võrgustandarditele nagu Ethernet. IEEE standardid tagavad, et seadmed saavad üksteisega suhelda olenemata tootjast või asukohast

- **IETF (Internet Engineering Task Force)**: IETF arendab ja edendab vabatahtlikke interneti standardeid, nagu TCP/IP, mis hoiavad interneti töötamise sujuva ja ühtse ülemaailmsel tasandil. Nende töö tagab, et andmed liiguvad tõhusalt ja turvaliselt üle võrgu.

Need standardiorganisatsioonid mängivad olulist rolli globaalse võrgu toimimises, luues universaalsed eeskirjad ja protokollid, mis võimaldavad tehnoloogiatel koostööd teha.

---

## Võrguseadmete kasutamine; põhiline kommutaator ja seadmete seadistamine


### Mis on Cisco IOS?


* [Sissejuhatus Cisco IOS CLI-sse](/lectures/contents/intro_to_cisco_cli/README.md)

Cisco IOS (Internetwork Operating System) on Cisco võrguseadmete, nagu ruuterid ja kommutaatorid, operatsioonisüsteem. Nii nagu arvutil on operatsioonisüsteem, näiteks Windows või macOS, ja nutitelefonidel iOS või Android, toimivad võrguseadmed spetsiaalsete operatsioonisüsteemidega, nagu Cisco IOS.

Cisco IOS pakub käsurealiidest (CLI), mille kaudu saavad võrguadministraatorid seadistada ja hallata võrguühendusi, seadistada turvalisust ja jälgida võrgu jõudlust.


### Erinevad võrgu operatsioonisüsteemid


Võrgu operatsioonisüsteemid (NOS) haldavad ja kontrollivad võrguseadmete, nagu ruuterite ja kommutaatorite, riistvara ja tarkvara ressursse. Need süsteemid pakuvad tööriistu, mis võimaldavad võrke tõhusalt seadistada, hallata ja turvata. Siin on mõned tuntud võrgu operatsioonisüsteemid:

- **Juniperi JUNOS**: JUNOS-i kasutatakse Juniper Networksi seadmetes ja see on tuntud oma stabiilsuse, modulaarse disaini ja tugeva turvalisuse poolest. Kasutajasõbralik liides ja võimas funktsionaalsus muudavad selle populaarseks suuremate ja keerukamate võrkude haldamisel.

- **HP ProCurve**: HP ProCurve NOS töötab HP võrgu toodetel ja on tuntud lihtsa integreerimise poolest HP riistvaraga. See on mõeldud võrkude lihtsaks haldamiseks ning pakub töökindlat ja skaleeritavat lahendust nii väikestele kui ka suurematele ettevõtetele.

- **MikroTiki RouterOS**: MikroTiki seadmetes kasutatav RouterOS on populaarne tänu oma paindlikkusele ja taskukohasusele. See pakub laia valikut funktsioone, sealhulgas tulemüürid, VPN-i tugi ja ribalaiuse haldamine, muutes selle ideaalseks väiksemates ja keskmise suurusega võrkudes, kus on vaja suurt kohandatavust.

Erinevad võrgu operatsioonisüsteemid pakuvad lahendusi erinevate võrguvajaduste jaoks, alates väikeettevõtetest kuni suurte ettevõtete ja organisatsioonide infrastruktuurini.

### Kuidas see toimib

Võrgu operatsioonisüsteemi toimimist saab mõista, jagades selle kolmeks oluliseks kihiks:

- **Shell** on kasutajaliides, mis võimaldab sul seadmega suhelda ja seda juhtida. Kui sa sisestad käske või annad süsteemile juhiseid (näiteks seadistad IP-aadressi või kontrollid võrguühendusi), siis toimub see shelli kaudu. Shell on nagu mängu ekraan, mis võimaldab sul näha ja teha toiminguid.

- **Kernel** on süsteemi süda ehk aju, mis juhib kogu toimimist kulisside taga. See haldab suhtlust riistvara ja tarkvara vahel, korraldab ressursse ning tagab, et kõik protsessid toimivad tõhusalt ja sujuvalt. Kernel on vastutav süsteemi jõudluse ja stabiilsuse eest.

- **Riistvara** on füüsiline seade ise, näiteks ruuter või kommutaator, mille sees on komponendid nagu emaplaat, protsessor ja mälu. Riistvara vastutab seadme tegeliku töö eest, nagu andmete edastamine ja võrguliikluse suunamine. Kernel suhtleb otse riistvaraga, et juhtida ja optimeerida selle toimimist.

Need kolm komponenti töötavad koos, et tagada võrgu operatsioonisüsteemi sujuv toimimine ja seadmete tõhus haldamine.

### Riistvaraspetsifikatsioonide mõistmine

Võrguseadmete, nagu ruuterid, kommutaatorid ja serverid, puhul mängivad riistvaraspetsifikatsioonid olulist rolli nende jõudluse ja võimekuse määramisel. Siin on mõned olulised spetsifikatsioonid ja nende tähendused:

- **Protsessor (CPU)**: on seadme "aju", mis juhib kõiki toiminguid. Võimsam CPU võimaldab seadmel kiiremini andmeid töödelda, hallata rohkem ühendusi ja tõhusamalt lahendada keerukaid võrgutoiminguid.

- **Mälu (RAM ja Flash)**: Mälu suurus määrab, kui palju andmeid ja konfiguratsioone seade korraga käsitleb. Rohkem mälu võimaldab seadmel töötada suurema andmemahuga ja hallata keerulisemaid ülesandeid, nagu suurte andmepakettide töötlemine või mitu võrguühendust korraga.

- **Liideste tüübid**: Võrguliidesed, nagu Ethernet, määravad seadme andmeedastuskiiruse ja ühenduvuse võimalused. Näiteks vanemad seadmed toetavad 10/100/1000 Mbps porte, kuid tänapäeva arenenud võrguseadmed võivad toetada kiirusi kuni **400 Gbps**, mis võimaldab väga kiiret andmevahetust suurtes võrkudes.

Esimene kaubanduslik Etherneti kiirus oli 10 Mbps, kuid nüüd suudavad kaasaegsed võrguseadmed hallata palju suuremaid kiirusi, tagades andmete kiire ja sujuva liikumise võrkudes.

![Cisco IOS-i juurdepääs](/lectures/images/cisco_ios_access.png)

---

## Käsurea kasutamine

Cisco seadmetel ei ole visuaalset kasutajaliidest, nagu arvutitel, kus näed ikoone ja graafikat. Selle asemel kasutatakse spetsiaalset käsurida, kus sisestad käske, et seadet juhtida – see on nagu "salakoodide" sisestamine, et asjad juhtuksid.

### Käsureale juurdepääsu viisid:

- **Konsoolikaabel**: Spetsiaalne kaabel, mille abil ühendad seadme otse ja teed konfiguratsiooni kohapeal.
- **Secure Shell (SSH)**: See võimaldab sul seadet eemalt ja turvaliselt juhtida, kasutades krüpteeritud ühendust.
- **Telnet**: Ka eemalt juhtimise võimalus, kuid see ei ole turvaline, sest andmeid ei krüpteerita. Seetõttu kasutatakse Telneti tänapäeval harvemini.


### Liikumine käsusüsteemis

Cisco seadmetel on mitu erinevat käsurežiimi, mida saad kasutada:

- **User Exec Mode**: See on algtaseme režiim, kus saad teha lihtsamaid toiminguid. Näed `>` sümbolit.
- **Privileged Exec Mode**: Siin saad teha keerulisemaid ja süsteemitaseme käske. Näed `#` sümbolit.
- **Global Configuration Mode**: See režiim on seadme põhjalike konfiguratsioonide tegemiseks. . Näed `#` koos mõne lisasõnaga, nagu `Switch(config)#`.

### Käskude sisestamine

Käsurida nõuab täpsust. Näiteks, kui tahad kontrollida seadme ühenduvust, võid sisestada järgmise käsu:


```
ping 192.168.10.5
```

See käsk annab seadmele juhise proovida ühendust konkreetse IP-aadressiga, kontrollides, kas see on võrgu kaudu saavutatav.


### Abi ja otseteed:


- Kui unustad käsu, võid pärast sõna kirjutada `?`, mis näitab sulle järgmisi võimalikke käske või süntaksit.
- Samuti saad kasutada otseteid, et säästa aega. Näiteks, `configure` asemel võid lihtsalt kirjutada `conf`, säästes aega ja lihtsustades sisestamist.

### Käsurea otseteed ja tööriistad:

Cisco seadmete käsurida pakub mitmeid otseteid ja tööriistu, mis aitavad tööd kiirendada ja muudavad seadmete haldamise mugavamaks:

- **Tabulaator (Tab)**: Kui oled käsu sisestamist alustanud, võid vajutada tabulaatorit, et käsu täitmine automaatselt lõpetada. See on kasulik, kui sa ei mäleta täpset käsu vormi.
- **Nooleklahvid**: Nooleklahvid võimaldavad sul liikuda käsuribal edasi ja tagasi, et parandada vigu või sisestada varem kasutatud käske uuesti.
- **Ctrl + C**: Kui tahad peatada käsu täitmise või käimasoleva protsessi, vajuta Ctrl + C. See viib sind tagasi põhiekraanile, et saaksid jätkata teiste toimingutega.
- **Ctrl + Shift + 6**: See klahvikombinatsioon toimib nagu "paus" nupp. Kui mingi protsess võtab liiga kaua aega või soovid ajutiselt peatada tegevuse, saad seda kombinatsiooni kasutada, et katkestada protsessi täitmine ilma käsurida sulgemata.

Need otseteed ja tööriistad aitavad tööd lihtsustada, võimaldades võrguadministraatoril kiiremini ja tõhusamalt seadmeid hallata.

---


## Oma võrguseadmete seadistamine; põhiline seadmete seadistamine

### Seadmete nimetamine

Iga võrguseade, näiteks ruuter või kommutaator, vajab unikaalset ja tähendusrikast nime, et saaksid seadmeid hõlpsasti hallata ja tuvastada. Selle asemel, et nimetada seadmeid juhuslikult (nt "Mickey" või "Goofy"), kasuta nimesid, mis annavad teavet seadme asukoha või funktsiooni kohta, näiteks "SW-Floor-1" (kommutaator esimesel korrusel).

### Nimetamisreeglid:

- Nimi peab algama tähega, mitte numbriga.
- Selles ei tohiks olla tühikuid, kuid võid kasutada sidekriipsu (-).
- Nimi peaks olema vähem kui 64 tähemärki pikk.


### Standardne nimetamise konventsioon

Suuremates võrkudes on standardne nimetamise süsteem oluline, et tagada ühtsus ja lihtne haldamine. Ühtselt nimetatud seadmed teevad võrgu haldamise ja tõrkeotsingu palju lihtsamaks. Näiteks, kui nimetad kommutaator "TLN-SW1", viitab see sellele, et tegemist on esimese kommutaatoriga Tallinnas, andes selge ettekujutuse selle asukohast ja rollist.


### Tugevate paroolide seadistamine

Tugevad paroolid on hädavajalikud, et kaitsta võrgu seadmeid volitamata juurdepääsu eest. Paroolid aitavad tagada, et ainult volitatud isikud saavad seadmetele ligi ja teha konfiguratsioonimuudatusi. Tugeva parooli reeglid hõlmavad tavaliselt:

- ** Kasuta pikki ja keerulisi paroole, mis sisaldavad tähti, numbreid ja sümboleid.
- ** Vältida lihtsaid ja kergesti äraarvatavaid paroole, nagu "admin" või "12345".

Nende põhiliste seadistusreeglite järgimine aitab sul luua turvalise ja hästi korraldatud võrgu.

![Seadme seadistamine](/lectures/images/device_configuration.png)

---


## Võrguprotokollide õppimine; protokollide ja mudelite mõistmine

### Miks on suhtlemiseks vaja reegleid?

Nii nagu inimesed peavad suhtlemiseks kasutama ühist keelt, peavad ka arvutid järgima kindlaid reegleid, mida nimetatakse protokollideks, et andmeid tõhusalt ja korrektselt vahetada. Kui üks arvuti "räägib" ühte protokolli ja teine teist, ei suuda nad üksteisest aru saada – just nagu kui üks inimene räägib inglise keelt ja teine prantsuse keelt.

### Suhtlemise põhitõed

Igas suhtluses on vaja järgmisi komponente:

- **Saatjat** Isik või seade, mis saadab sõnumi.
- **Vastuvõtjat**  Isik või seade, mis saab sõnumi.
- **Meediumit** Kanal, mille kaudu sõnum liigub – näiteks kaablite, Wi-Fi või muu ühenduse kaudu.

### Andmeedastusmeetodid


Andmeedastusmeetodid määravad, kuidas ja millisel viisil andmed liiguvad seadmete vahel. Siin on kolm peamist tüüpi:

- **Simplex**: Andmed liiguvad ainult ühes suunas. Näiteks televisiooniülekanne, kus signaal liigub jaamast telerisse, kuid teler ei saada midagi tagasi.
  
- **Half-Duplex**: Andmed liiguvad mõlemas suunas, kuid mitte samaaegselt. Mõtle raadiosaatjale, kus üks inimene räägib, samal ajal kui teine kuulab.
  
- **Full-Duplex**: Andmed liiguvad mõlemas suunas samaaegselt. Näiteks telefonikõne, kus mõlemad osapooled saavad korraga rääkida ja kuulata.

---

## Mis on protokollid?

Protokollid on reeglid ja standardid, mida seadmed järgivad, et suhelda ja andmeid vahetada. Need tagavad, et kõik seadmed räägivad "sama keelt" ja mõistavad üksteist.

Protokollid aitavad:

- **Kodeerimisel**: Sõnumi muutmisel vorminguks, mida saab saata, näiteks muutes sõnad või andmed digitaalseteks signaalideks.
- **Formaatimisel**: Tagades, et sõnum on õigesti struktureeritud ja seda saab lugeda ja mõista.
- **Ajastamisel**: Kontrollides, et andmeid saadetakse ja võetakse vastu õige kiirusega ning õiges järjekorras.
- **Kohaletoimetamisel**: Otsustades, kas sõnum saadetakse ühele seadmele, rühmale või kõigile võrgus olevatele seadmetele.

Need protokollid loovad võrgu suhtlemise aluse, tagades, et andmed liiguvad õigesti ja tõhusalt erinevate seadmete vahel.

### Vigade tuvastamine ja parandamine

Vigade tuvastamine ja parandamine on kriitilise tähtsusega, et andmed edastataks võrgus täpselt ja usaldusväärselt. Kuna andmete liikumisel võivad tekkida häired ja moonutused, kasutavad protokollid erinevaid tehnikaid, nagu kontrollsummad või tsükliline redundantsuskood (CRC), vigade avastamiseks.

Kui viga avastatakse, võib süsteem kas küsida andmete uuesti saatmist või proovida neid parandada, kasutades lisateavet, mis saadeti koos andmetega. Sellised mehhanismid tagavad, et võrgusuhtlus püsib stabiilne ja täpne.

Hamming-koodid, mis töötati välja 1940. aastatel, on üks esimesi vigade tuvastamise ja parandamise meetodeid ning neid kasutatakse tänapäevalgi.

### Sõnumite edastamise tüübid

Võrgus on erinevaid viise, kuidas sõnumeid edastatakse:

- **Unicast**: Sõnumi saatmine ühelt seadmelt ühele teisele seadmele.
- **Multicast**: Sõnumi saatmine ühelt seadmelt mitmele sihtseadmele.
- **Broadcast**: Sõnumi saatmine kõigile võrgu seadmetele korraga.

### Anycast-suhtlus

Anycast-suhtlus on meetod, kus sõnum saadetakse mitmele potentsiaalsele vastuvõtjale, kuid see jõuab ainult lähima või kõige optimaalsema sihtkohani. Anycasti kasutatakse sageli koormuse tasakaalustamiseks ja võrgu jõudluse optimeerimiseks.

### Erinevad protokollide tüübid

Võrkudes kasutatakse erinevaid protokolle, millel on oma kindlad ülesanded:

- **Võrgu suhtlusprotokollid**: Aitavad seadmetel suhelda ja andmeid vahetada.
- **Turvaproktokollid**: Tagavad, et andmed on turvalised ja ainult volitatud isikud saavad neile ligi.
- **Marsruutimisprotokollid**: Aitavad leida parima marsruudi andmete edastamiseks.
- **Teenuste avastamise protokollid**: Aitavad seadmetel võrgu kaudu üksteist leida ja teenuseid pakkuda.

### Levinud võrgu protokollid


| **Protokoll** | **Täisnimi**                        | **Eesmärk**                                                                 |
|---------------|-------------------------------------|------------------------------------------------------------------------------|
| **HTTP**      | Hypertext Transfer Protocol         | Kasutatakse veebilehtede edastamiseks internetis.                            |
| **FTP**       | File Transfer Protocol              | Kasutatakse failide edastamiseks arvutite vahel.                             |
| **DNS**       | Domain Name System                  | Tõlgib domeeninimed IP-aadressideks.                                         |
| **SMTP**      | Simple Mail Transfer Protocol       | Kasutatakse e-kirjade saatmiseks ühelt serverilt teisele.                    |

**Lõbus fakt**: DNS-i kutsutakse interneti "telefoniraamatuks", sest see seob domeeninimed (nt www.example.com) vastavate IP-aadressidega, mis on arvutitele arusaadavad.

### Kuidas protokollid koos töötavad

Paljud protokollid töötavad koos, et tagada sujuv ja tõhus suhtlus võrgus. Näiteks:

- **HTTP**: Aitab laadida veebilehti ja edastada veebisisu.
- **TCP**: Tagab, et andmed jõuavad vigadeta kohale, kontrollides andmepakettide terviklikkust.
- **IP**: Leiab parima marsruudi andmete liikumiseks võrgus.
- **Ethernet**: Ühendab seadmeid füüsiliselt kaablite või Wi-Fi kaudu.

### Mis on protokollikomplekt?

**Protokollikomplekt** on rühm protokolle, mis töötavad koos, et täita erinevaid võrgusuhtluse ülesandeid. Kõige tuntum ja laialdasemalt kasutatav protokollikomplekt on TCP/IP, mis on interneti selgroog.

![Protokolli andmevoog](/lectures/images/protocol_data_flow.png)

### TCP/IP areng

TCP/IP (Transmission Control Protocol/Internet Protocol) on interneti kõige olulisem protokollikomplekt, mis loodi 1970ndatel. Selle arendamine mängis võtmerolli kaasaegse interneti loomisel, võimaldades seadmetel suhelda üle kogu maailma ja tagades, et andmeid saab usaldusväärselt ja tõhusalt edastada. TCP/IP on pidevalt arenenud, et kohaneda kasvava internetikasutuse ja uute tehnoloogiatega, säilitades samas oma keskse rolli ülemaailmse suhtluse võimaldamisel.

### Andmete saatmine võrgu kaudu

Kui saadad sõnumi või laadid veebilehte, jagatakse andmed väikesteks tükkideks, mida nimetatakse pakettideks. Need pakitakse kokku ja saadetakse üle võrgu. Iga pakett liigub oma teed mööda sihtkohta, kus vastuvõttev seade need uuesti kokku paneb, et saaksid tervikuna näiteks veebilehte näha.

### Kes teeb reeglid?

Võrgu toimimiseks järgivad kõik seadmed ja programmid kindlaid reegleid, mida loovad ja haldavad spetsiaalsed organisatsioonid. Need protokollid ja standardid tagavad, et kõik süsteemid suudavad koos töötada. Mõned peamised organisatsioonid, kes neid reegleid loovad ja haldavad, on:

- **IETF**: (Internet Engineering Task Force) IETF arendab ja hooldab interneti toimimiseks vajalikke protokolle ja standardeid. Nende töö tagab, et internet töötab sujuvalt ja kõik seadmed saavad omavahel suhelda.
- **ICANN**: (Internet Corporation for Assigned Names and Numbers) ICANN haldab ja koordineerib domeeninimesid ja IP-aadresse, tagades, et igal veebisaidil on kordumatu nimi ja aadress, mida saab tuvastada kogu maailmas.
- **IEEE**: (Institute of Electrical and Electronics Engineers) IEEE loob standardeid elektroonikaseadmete jaoks, sealhulgas võrguseadmete jaoks, näiteks Etherneti ja Wi-Fi standardid.

### IETF ja RFC-d

**Internet Engineering Task Force (IETF)** mängib võtmerolli interneti toimimise tagamisel. IETF koosneb inseneride, võrgu disainerite ja teadlaste rahvusvahelisest kogukonnast, kes arendavad ja täiustavad interneti protokolle, nagu HTTP, TCP/IP ja DNS. Nende töö avaldatakse dokumentides, mida kutsutakse RFC-deks (Request for Comments). RFC-d on tehnilised dokumendid, mis määratlevad, kuidas internetitehnoloogiad töötavad ja kuidas neid arendada.

RFC-d toimivad interneti tehnoloogiate "sinikavadena," ja iga uus standard, mida IETF arendab, saab laialdaseks juhendiks võrgu ja interneti edasisele arengule.

Üks kõige lõbusamaid ja tuntumaid RFC-dokumente on RFC 1149, mille nimi on "A Standard for the Transmission of IP Datagrams on Avian Carriers". See dokument avaldati 1. aprillil 1990 ja kirjeldab, kuidas saata IP-andmepakette tuvide abil!

Kuigi see RFC oli mõeldud naljana, käsitledes "linnukandja" (avian carriers) kui andmete edastusviisi, järgib see siiski tehnilist dokumentatsiooni formaati ja on päris IETF-i poolt avaldatud dokument. See on olnud internetikultuuri osa ja rõõmustanud paljusid tehnikaasjatundjaid oma loomingulise huumoriga.

Lõbus fakt: 2001. aastal viis Norra Linuxi kasutajate rühm läbi eduka katse, kus nad edastasid andmeid tuvide abil, järjekorras "linnupõhist" IP-pakettide edastust, tõestades, et RFC 1149 võib (aeglase ja mitte praktilise) viisi korral isegi toimida!

![Linnukandja RFC-dokument](/lectures/images/avianpigeon.png)

---

## Võrgukihtide ja -mudelite mõistmine; kihid ja mudelid

### Miks me kasutame kihte?

Võrgud on keerulised süsteemid, kus toimub tohutu hulk andmete vahetust. Kihid aitavad jagada selle keeruka protsessi väiksemateks ja lihtsamateks ülesanneteks, muutes andmete saatmise ja vastuvõtmise hallatavamaks. Igal kihil on oma spetsiifiline roll – sama nagu koogi küpsetamisel, kus iga etapp (näiteks glasuuri lisamine või kaunistamine) täidab oma kindlat ülesannet.

### Kihilise arhitektuuri eelised

Kihilise arhitektuuri kasutamine võrkudes on kasulik mitmel põhjusel:

- **Modulaarsus**: Nii nagu saad oma võileivale lisada või eemaldada juustu ilma kogu võileiva muutmata, võimaldab kihiline võrk arhitektuuris ühe osa muutmist (nt tarkvara uuendamine) ilma, et teised osad oleksid mõjutatud.
  
- **Mastaapsus**: Kui võileib kasvab kihiti, saab ka võrk kasvada – lisades uusi komponente või teenuseid, mõjutamata kogu süsteemi. Kihid aitavad võrkudel laieneda ja kohaneda uute nõudmistega ilma suuri ümberkorraldusi tegemata.
  
- **Lihtne tõrkeotsing**: Kihiline struktuur muudab probleemide tuvastamise ja parandamise lihtsamaks. Kui probleem ilmneb ühes kihis, saab seda parandada ilma, et see mõjutaks teisi kihte. See on nagu võileiva puhul halva koostisosa (näiteks salatilehe) eemaldamine, ilma et peaks kogu võileiba ümber tegema.

Kihiline arhitektuur muudab võrgu toimimise ja hoolduse lihtsamaks, skaleeritavaks ja tõhusamaks.

### OSI mudel (7 kihti):

1. **Füüsiline**: Vastutab andmete edastamise eest füüsiliste signaalidena, näiteks elektriliste impulssidena või valgusimpulssidena (nagu tulede sisse ja välja lülitamine).
2. **Andmeside** (kanalikiht): Vormistab andmed õigesse formaati ja hoolitseb vigade tuvastamise ning parandamise eest. Siin toimivad ka võrguadapterid ja MAC-aadressid.
3. **Võrk**: Määrab parima tee, mida mööda andmed liiguvad. IP-aadressid ja marsruutimine toimuvad selles kihis.
4. **Transpordikiht**: Tagab, et andmed jõuavad vigadeta ja õiges järjekorras kohale, kasutades selliseid protokolle nagu TCP ja UDP.
5. **Seanss**: Haldab ühenduste loomist ja lõpetamist seadmete vahel, et andmevahetus oleks järjepidev.
6. **Esitluskiht**: Tegeleb andmete kodeerimise ja dekodeerimisega, pakkides ja pakkimata faile, et neid oleks rakendustasandil lihtne töödelda.
7. **Rakenduskiht**: See on kõige lähemal kasutajale ja suhtleb otse tarkvara või rakendustega, nagu veebibrauserid ja e-posti programmid.

### TCP/IP mudel (4 kihti):

1. **Võrgujuurdepääs**: See kiht ühendab OSI mudeli füüsilise ja andmeside kihi ülesanded, hõlmates riistvara ja füüsilisi ühendusi andmeedastuseks.
2. **Internet**: Hõlmab OSI mudeli võrgukihi ülesandeid, suunates andmeid üle erinevate võrkude ja vastutades IP-aadresside ning marsruutimise eest.
3. **Transpordi**: Sama funktsioon nagu OSI transpordikihil, hoolitsedes andmete terviklikkuse ja järjekorra eest, kasutades TCP või UDP protokolle.
4. **Rakenduskiht**: Ühendab OSI mudeli rakendus-, esitlus- ja seansikihid, pakkudes liidest kasutajarakenduste ja võrgu vahel, näiteks veebisirvimine ja e-posti vahetamine.

Mõlemad mudelid annavad selge ülevaate, kuidas andmed liiguvad võrgus kihiti, kuid TCP/IP mudel on praktilisem ja seda kasutatakse tänapäeval laialdasemalt, eriti internetis.

### OSI ja TCP/IP mudelite võrdlus

* [OSI mudel ja TCP/IP komplekt](/lectures/contents/osi_model_and_tcp_ip_suite/README.md)

| **Aspekt**          | **OSI mudel**                                 | **TCP/IP mudel**                                |
|---------------------|------------------------------------------------|-------------------------------------------------|
| **Kihid**           | 7 kihti                                        | 4 kihti                                         |
| **Kasutus**         | Peamiselt õpetamiseks ja kontseptuaalseks mõistmiseks| Laialdaselt kasutatav reaalses internetis |
| **Kihid**           | Füüsiline, andmeside, võrk, transport, seanss, esitlus, rakendus | Link, Internet, Transport, Rakendus |
| **Rakendamine**     | Pole praktikas täielikult rakendatud           | Interneti ja enamiku võrkude alus              |


### OSI mudeli meeldejätmine

Lõbus viis OSI mudeli kihtide meeldejätmiseks on järgmine lause: **"All people seem to need data processing."** iga sõna esindab ühte OSI kihti, aidates sul neid järjekorras meelde jätta:

### Kuidas andmed kihtides liiguvad?

Andmete edastamisel võrgus jagatakse need väiksemateks osadeks, mida nimetatakse segmentideks. Need segmendid liiguvad läbi erinevate kihtide, kus neid töödeldakse ja täiendatakse, et tagada sujuv edastus. Multipleksimine toimub siis, kui segmente segatakse teiste andmetega, et need kiiremini liiguksid.

### Andmete kapseldamine

Kui andmed liiguvad OSI või TCP/IP mudeli kihtide kaudu alla, lisab iga kiht oma teabe (nt päised) andmetele juurde. Seda protsessi nimetatakse kapseldamiseks. Kui andmed jõuavad sihtkohta, eemaldatakse need kihid järk-järgult (nagu kingituse lahtipakkimine), kuni algsed andmed on nähtavad ja kasutatavad.

### Andmete adresseerimine võrgus

Andmete liikumiseks võrgus on vajalik aadressimine. Kaks peamist tüüpi aadresse on:

- **IP-aadress (3. kiht)**: Seda kasutatakse andmete suunamiseks üle kogu võrgu ja globaalsetes mastaapides. See on nagu postiaadress, mis ütleb, kuhu andmed peaksid lõppkokkuvõttes jõudma.
- **MAC-aadress (2. kiht)**: See on seadme ainulaadne aadress, mida kasutatakse kohalikus võrgus. See on nagu maja number, mis täpsustab, milline seade kohapeal andmed vastu võtab.

![Protokollid tegevuses](/lectures/images/protocols_in_action.png)

Need kontseptsioonid moodustavad võrkude töö alustalad ja aitavad andmeid usaldusväärselt sihtkohta viia.

* [Ethernet LAN-i kommutatsioon](/lectures/contents/ethernet_lan_switching/README.md)
* [IPv4 aadressimine](/lectures/contents/ipv4_addressing/README.md)


### IPv4 vs. IPv6

IPv4 ja IPv6 on mõlemad Interneti protokolli (IP) versioonid, mida kasutatakse seadmete tuvastamiseks ja andmete saatmiseks võrgus. Siin on nende kahe protokolli peamised erinevused:

| **Aspekt**           | **IPv4**                                      | **IPv6**                                                 |
|----------------------|-----------------------------------------------|----------------------------------------------------------|
| **Aadressi pikkus**  | 32-bitine (nt 192.168.1.1)                    | 128-bitine (nt 2001:0db8:85a3::8a2e:0370:7334)           |
| **Aadresside arv**   | ~4,3 miljardit aadressi                       | 340 undecillion aadressi (tohutult suur number!)         |
| **Vorming**          | Punktidega kümnendkohaline vorming            | Kuueteistkümnendkohaline vorming koos koolonitega        |
| **IPv6 vajadus**     | Piiratud aadressiruum, aadressid otsa saamas  | Suur aadressiruum, et mahutada kasvavat internetti ühendatud seadmete arvu |

![Map of the internet (IPv4) space](/lectures/images/ipv4_map_of_the_internet.png)

IPv4 aadressiruum (~4,3 miljardit aadressi) tundus piisav 1980ndatel, kuid tänapäeval, koos nutitelefonide, IoT-seadmete ja arvutite kiire kasvuga, on aadressiruum otsakorral. Seetõttu loodi IPv6, et tagada palju suurem aadressiruum, mis suudab toetada pidevalt kasvavat seadmete arvu.

> The IP address space is managed globally by the Internet Assigned Numbers Authority (IANA), and by five regional Internet registries (RIRs)  
> responsible in their designated territories for assignment to local Internet registries, such as Internet service providers (ISPs), and other  
> end users. IPv4 addresses were distributed by IANA to the RIRs in blocks of approximately 16.8 million addresses each, but have been exhausted  
> at the IANA level since 2011. Only one of the RIRs still has a supply for local assignments in Africa. Some IPv4 addresses are reserved for  
> private networks and are not globally unique.

### Mis toimub erinevates võrkudes?

Kui kaks seadet, nagu sinu arvuti ja printer, asuvad samas kohalikus võrgus (näiteks koduvõrgus), kasutavad nad üksteisega suhtlemiseks MAC-aadresse. MAC-aadressi võib võrrelda maja numbriga, mis aitab seadmetel üksteist kiiresti leida, kui need on samas füüsilises võrgus.

Kui aga kaks seadet asuvad erinevates võrkudes (näiteks sinu koduarvuti ja server internetis), kasutatakse suhtlemiseks IP-aadresse. IP-aadress on nagu tänava aadress, mis aitab andmetel leida tee üle interneti õigele sihtvõrgule. Kui andmed jõuavad õigesse võrku, kasutavad need taas MAC-aadressi, et leida konkreetne seade, kuhu andmed peavad jõudma.

![OSI vs TCP/IP mudelid](/lectures/images/osi_vs_tcpip_models.png)

> [!TIP]
> [Switch liidesed](/lectures/contents/switch_interfaces/README.md)
> [IPv4 päis](/lectures/contents/ipv4_header/README.md)
> [Marsruutimise alused](/lectures/contents/routing_fundamentals/README.md)
> [Staatiline marsruutimine](/lectures/contents/static_routing/README.md)

---
