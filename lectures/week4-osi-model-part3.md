[!TIP]
>[IPv6 Addressing](https://www.youtube.com/watch?v=0m4PJxUh-L8&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=16)
>[ICMP](https://www.youtube.com/watch?v=BLkTmio7ccc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=17)
>[Transport Layer](https://www.youtube.com/watch?v=1UW6D6iP9Fc&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=18)
>[Application Layer](https://www.youtube.com/watch?v=It7gHtCFhpY&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=19)

# Nädal 4: OSI mudel - 3. osa (Transpordi-, seansi-, esitlus- ja rakenduskiht) (Moodulid 12-15)

Eelmistel tundidel oleme juba vaadanud füüsilisi ja kanalikihte, nüüd keskendume järgmistele, kõrgematele kihtidele: transpordikiht ning seansi-, esitlus- ja rakenduskiht. Need kihid on võtmetähtsusega tagamaks, et andmed liiguvad võrgus õigesti ja rakendused saavad töötada ootuspäraselt.

## IPv6 aadressimine

IPv6 (Internet Protocol version 6) on uusim IP versioon, mis lahendab IPv4 puudujäägid, pakkudes palju suuremat aadressiruumi ja täiendavaid funktsioone. IPv6 aadressid on 128-bitised, võrreldes IPv4 32-bitiste aadressidega, mis tähendab, et saadaval on tohutult rohkem unikaalseid aadresse.

### IPv6 aadressi struktuur:
- **Aadresside pikkus:** 128 bitti.
- **Tähistus:** Tavaliselt kirjutatakse kuusnurksetes rühmades, mis on eraldatud koolonitega (nt 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
- **Tööjaotus:** IPv6 pakub automaatset aadresside konfigureerimist ja on loodud töötama suuremates võrkudes.

IPv6 toob kaasa ka muid kasulikke funktsioone nagu sisseehitatud turvalisus (IPSec) ja multicast-tugi, mis teeb selle tulevikus oluliseks protokolliks.

![IPv6 aadressi struktuur](/lectures/images/ipv6_address_structure.png)

## ICMP (Internet Control Message Protocol)

ICMP on protokoll, mida kasutatakse võrgu seadmete omavaheliseks suhtluseks, et tuvastada ja raporteerida võrgu probleeme. ICMP ei ole andmesideprotokoll, vaid seda kasutatakse vigade aruandmiseks ja diagnostika tegemiseks.

### ICMP funktsioonid:
- **Ping:** Kõige tuntum ICMP rakendus, mida kasutatakse seadme kättesaadavuse ja viivituse mõõtmiseks.
- **Traceroute:** Kasutab ICMP sõnumeid, et jälgida marsruuti, mida andmepakett võtab võrgu kaudu sihtkohani.
- **Vea sõnumid:** ICMP saadab sõnumeid, kui marsruutimist ei saa lõpule viia või kui sihtseade on kättesaamatu.

**Näide:** Kui saadad käsu `ping`, siis saadab arvuti ICMP sõnumi teisele seadmele ja saab vastuse, kui seade on kättesaadav.

![ICMP töövoog](/lectures/images/icmp_workflow.png)

### Transpordikiht

Transpordikihi peamine ülesanne on tagada andmete usaldusväärne edastamine kahe seadme vahel. Kui madalamad kihid vastutavad andmete füüsilise edastamise eest, siis transpordikiht kontrollib, et andmete ülekanne oleks usaldusväärne ja korrektne. Transpordikiht jagab andmed väiksemateks osadeks, mida nimetatakse segmentideks.

![Transpordikihi segmendid](/lectures/images/transport_layer_segments.png)

Kaks peamist transpordikihi protokolli on **TCP (Transmission Control Protocol)** ja **UDP (User Datagram Protocol)**.

#### TCP (Transmission Control Protocol)

TCP on usaldusväärne protokoll, mis tagab, et kõik andmed jõuavad vastuvõtjale õiges järjekorras ja vigadeta. Seda tehakse mitmes etapis:

1. **Ühenduse loomine**: Enne andmeedastuse alustamist luuakse ühendus saatja ja vastuvõtja vahel, kasutades "kolmeastmelist käepigistust" (three-way handshake).
2. **Segmentide nummerdamine**: Iga segment saab unikaalse numbri, mis tagab, et andmed jõuavad kohale õiges järjekorras.
3. **Kinnitused**: Vastuvõtja saadab kinnituse (ACK), kui ta on segmendi kätte saanud. Kui kinnitust ei saadeta, saadab saatja segmendi uuesti.
4. **Voolukontroll ja kongestiivjuhtimine**: TCP jälgib võrgu koormust ja reguleerib andmete saatmise kiirust, et vältida ülekoormust.

**Näide**: Kui laadid alla faili internetist, kasutab süsteem sageli TCP-d, kuna fail tuleb edastada terviklikult ja õiges järjekorras.

#### UDP (User Datagram Protocol)

UDP on kiirem ja lihtsam protokoll kui TCP, kuid see ei paku usaldusväärsust. UDP ei loo ühendust saatja ja vastuvõtja vahel ning ei nõua kinnitusi. See tähendab, et andmeid saadetakse "parima võimaliku" põhimõttel. See sobib rakendustele, kus andmete kiire edastamine on olulisem kui täpsus.

**Näide**: Videokõned ja reaalajas voogedastus kasutavad sageli UDP-d, sest nendes olukordades on olulisem, et andmed liiguvad kiiresti, mitte et kõik paketid täpselt kohale jõuavad.

#### Pordid

Transpordikiht kasutab pordinumbreid, et eristada erinevaid teenuseid ja rakendusi, mis suhtlevad sama võrguühenduse kaudu. Näiteks:
- **HTTP** kasutab porti **80**.
- **HTTPS** kasutab porti **443**.

Pordid tagavad, et erinevad rakendused saavad üheaegselt töötada, kasutades sama IP-aadressi.

![Pordid ja protokollid 1](/lectures/images/ports_and_protocols1.png)
![Pordid ja protokollid 2](/lectures/images/ports_and_protocols2.png)

### Seansikiht

Seansikiht (Session Layer) haldab ja kontrollib seansse kahe seadme vahel. Seansid on vajalikud, et tagada sujuv andmevahetus ja võimalus katkestuste korral seanssi jätkata.

Seansikiht vastutab seansi loomise, haldamise ja lõpetamise eest. Lisaks võimaldab see kahe seadme vahel andmevahetust sünkroniseerida ja jälgida.

**Näide**: Veebikohtumiste ajal aitab seansikiht tagada, et kui ühendus katkeb, saab kasutaja jätkata sama kohtumist ilma andmeid kaotamata.

### Esitluskiht

Esitluskiht (Presentation Layer) vastutab andmete esitamise ja kodeerimise eest sellisel viisil, et vastuvõtva seadme tarkvara suudaks neid õigesti tõlgendada. See hõlmab andmete tihendamist, krüpteerimist ja vormindamist erinevates standardites.

- **Tihendamine**: Andmete maht vähendatakse, et kiirendada nende edastamist (nt ZIP-failid).
- **Krüpteerimine**: Andmed kodeeritakse, et tagada turvalisus (nt SSL/TLS).
- **Vormingud**: Esitluskiht suudab töödelda erinevaid andmevorminguid, nagu tekstifailid (ASCII), pildid (JPEG), video (MPEG).

**Näide**: Kui saadad e-kirja manusega, mis on ZIP-failis, siis tihendab esitluskiht manuse ja saadab selle väiksemas mahus edasi.

![Esitluskihi kodeerimine](/lectures/images/presentation_layer_encoding.png)

### Rakenduskiht

Rakenduskiht (Application Layer) on kõige kõrgem kiht OSI mudelis ja vastutab selle eest, et kasutajad saaksid ligipääsu erinevatele võrguressurssidele ja teenustele. See kiht tagab, et tarkvararakendused, mida kasutajad igapäevaselt kasutavad, suudavad võrgu kaudu suhelda.

Rakenduskiht toetab selliseid teenuseid nagu:
- **E-post** (SMTP, IMAP).
- **Veebibrauserid** (HTTP, HTTPS).
- **Failide edastamine** (FTP).

**Näide**: Veebilehitseja kasutamine lehe avamiseks kasutab rakenduskihi HTTP protokolli, et suhelda veebiserveriga ja tuua lehekülje andmed sinu seadmesse.

![Rakenduskihi teenused](/lectures/images/application_layer_services.png)

### Kokkuvõte

OSI mudeli transpordikiht, seansikiht, esitluskiht ja rakenduskiht mängivad kõik võtmerolli andmeside protsessis. Transpordikiht tagab, et andmed liiguvad usaldusväärselt või kiirelt olenevalt protokollist (TCP vs UDP), seansikiht haldab andmevoogusid ja seansse, esitluskiht hoolitseb andmete esitamise ja kodeerimise eest, ning rakenduskiht pakub kasutajatele juurdepääsu võrguteenustele. Kõik need kihid töötavad koos, et võimaldada sujuvat ja tõhusat andmesidet võrgus.
