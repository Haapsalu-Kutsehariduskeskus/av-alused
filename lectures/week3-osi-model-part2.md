[!TIP]
>[IPv4 Addressing](https://www.youtube.com/watch?v=f0iCqZpJZcA&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=10)
>[Subnetting](https://www.youtube.com/watch?v=zcOeSxvE3ME&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=11)
>[VLSM](https://www.youtube.com/watch?v=loWsRUDgW34&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=12)
>[IPv6 Addressing](https://www.youtube.com/watch?v=2BJrH1jHrbY&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=13)
>[IPv6 Configuration](https://www.youtube.com/watch?v=fS6jt7D33N8&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=14)
>[Routing Basics](https://www.youtube.com/watch?v=_P5Mm11_o7k&list=PLk4NQNr6-L8onI6MaPcfsRZJOvFO3S5D6&index=15)

# Nädal 3: OSI mudeli mõistmine - Osa 2 (Võrgukiht ja alavõrgutamine)

# Võrgukiht ja marsruutimine

See osa põhineb Cisco "Sissejuhatus võrkudesse" seerial ja käsitleb OSI mudeli kolmandat kihti ehk võrgukihti (Layer 3). Võrgukiht on oluline, sest see tagab andmete liikumise erinevate seadmete vahel ja teeb marsruutimisotsuseid, et saata pakette õigesse sihtkohta.

![OSI vs TCP/IP mudelid](/lectures/images/osi_vs_tcpip_models.png)

## Võrgukihi omadused

Võrgukiht vastutab marsruutimise ja lõppseadmete aadresside määramise eest. Marsruutimine tähendab seda, et kui andmepakett peab liikuma ühest võrgust teise, siis võrgukiht otsustab, kuidas see pakett liigub ja kuhu see läheb. Peamised ülesanded selles kihis on:

- **Seadmete aadressimine**: Iga võrgus olev seade peab omama unikaalset aadressi, et andmepaketid teaksid, kuhu nad peavad jõudma.
- **Pakettide kapseldamine ja dekapseldamine**: Kui andmepakett liigub ühest kohast teise, lisatakse sellele võrgukihi päis, mis sisaldab infot, kuhu pakett läheb ja kust see tuleb.
- **Pakettide marsruutimine**: Võrgukiht otsustab, millist teed mööda pakett liigub, et jõuda sihtkohta, mis võib olla erinev võrk.

![Võrgukihi funktsioonid](/lectures/images/network_layer_functions.png)

---

## IPv4 ja IPv6 protokollid

IPv4 ja IPv6 on kaks peamist protokolli, mida kasutatakse võrgukihis. **IPv4** on juba kaua kasutusel olnud ja see suudab adresseerida umbes 4,3 miljardit seadet. Kuna aadresse hakkas nappima, loodi **IPv6**, mis suudab aadresseerida tunduvalt rohkem seadmeid (2^128 aadressi). IPv6-l on ka lihtsam päis, mis teeb võrgusuhtluse kiiremaks ja tõhusamaks.

![IPv4 vs IPv6](/lectures/images/ipv4_vs_ipv6.png)

## Ühenduseta ja parima püüdluse põhine kommunikatsioon

**Internetiprotokoll (IP)** on ühenduseta ja parima püüdluse põhine. See tähendab, et pakette saadetakse ilma kindla ühenduse loomata, ja IP ei taga, et pakett jõuab kohale või et jõuab õiges järjekorras. Kui on oluline, et andmed jõuaksid kindlasti ja õigesti kohale, kasutatakse koos IP-ga muid protokolle, näiteks **TCP**, mis haldab andmete usaldusväärset kohalejõudmist.

## IPv4 paketi struktuur

IPv4 paketi päises on mitmeid olulisi välju:

- **Lähteaadress ja sihtaadress**: Need määravad, kust pakett tuleb ja kuhu see läheb.
- **Aegumisväärtus (TTL)**: See väli näitab, kui kaua paketti võib edasi saata enne, kui see "aegub".
- **Kontrollsumma**: See väli aitab kontrollida, kas andmed on saatmise käigus kahjustada saanud.

## IPv6 paketi struktuur

IPv6 pakettide päis on küll pikem kui IPv4 oma, kuid see on samas lihtsam ja fikseeritud suurusega (40 baiti). IPv6 olulised väljad sisaldavad:

- **Aadressid**: IPv6 kasutab 128-bitiseid aadresse, mis võimaldavad palju rohkem seadmeid võrku ühendada.
- **TTL asendaja (Hop Limit)**: See asendab IPv4-s kasutatava aegumisväärtuse ja määrab, mitu "hüpet" ehk marsruuterit pakett võib läbida.
- **NAT vajaduse kaotamine**: Kuna IPv6-l on nii palju aadresse, ei ole enam vajadust NAT (Network Address Translation) tehnoloogia järele, mida IPv4-s kasutatakse aadresside kokkuhoidmiseks.

![IPv6 paketistruktuur](/lectures/images/ipv6_packet_structure.png)

## IPv4 ja IPv6 erinevused kokkuvõttes

- **IPv4**: Piiratud aadressiruum, vajadus NAT-i järele, keerulisem päis.
- **IPv6**: Suurem aadressiruum, NAT-i pole vaja, lihtsam päis.

---

## Pakettide edastamine ja marsruutimisotsused

Teine osa keskendub sellele, kuidas võrgus olevad seadmed ja marsruuterid teevad otsuseid pakettide edastamise kohta.

## Hosti marsruutimisotsused

Igal võrgus oleval seadmel ehk hostil on oma marsruutimistabel, mis aitab otsustada, kuidas andmepakette edasi saata. Host võib saata pakette:

- **Endale**: Näiteks aadress 127.0.0.1 IPv4 puhul ja ::1 IPv6 puhul.
- **Teisele seadmele samas kohalikus võrgus**: Kui sihtkoht asub samas LAN-is.
- **Kaugele seadmele**: Kui sihtkoht on väljaspool kohalikku võrku.

![Hosti marsruutimistabel](/lectures/images/host_routing_table.png)

## Kohaliku ja kauge liikluse määramine

IPv4 puhul kasutatakse hosti IP-aadressi ja alamvõrgu maski, et otsustada, kas sihtkoht on kohalik või kauge. IPv6 puhul kasutatakse võrguaadressi ja prefiksit, mida jagab kohalik ruuter.

## Vaikelüüs

Kui liiklus peab minema väljapoole kohalikku võrku, kasutatakse selleks **vaikelüüsi**. Vaikelüüs on tavaliselt ruuter või kolmanda kihi lüliti, mis edastab andmed teistesse võrkudesse.

---

## Marsruutimistabeli tüübid

Marsruuteritel on tabelid, mis aitavad otsustada, kuhu pakette saata. Seal on erinevad marsruuditüübid:

- **Otseselt ühendatud marsruudid**: Need lisatakse automaatselt, kui seadme liides on aktiivne.
- **Kaugmarsruudid**: Neid saab lisada käsitsi (staatilised marsruudid) või õppida dünaamiliselt, kasutades marsruutimisprotokolle.
- **Vaikemarsruut**: Kasutatakse siis, kui ükski teine marsruut sihtkohta ei sobi.

## Staatiline ja dünaamiline marsruutimine

Staatilised marsruudid on käsitsi seadistatud ja sobivad väikestesse võrkudesse. Dünaamiline marsruutimine aga leiab automaatselt parima tee ja kohaneb võrgus toimuvate muutustega. Marsruuterid jagavad omavahel infot marsruutide kohta, kasutades protokolle nagu OSPF ja EIGRP.

See teema annab olulise ülevaate, kuidas andmed liiguvad võrgus ja kuidas seadmed teevad marsruutimisotsuseid, et tagada sujuv ja efektiivne andmevahetus.

---

# Võrgustike põhialused

Kui erinevad seadmed – nagu arvutid, telefonid ja printerid – omavahel võrgus suhtlevad, kasutavad nad selleks erinevaid aadresse. Siin on kaks peamist tüüpi aadresse, mida seadmed kasutavad: MAC-aadressid ja IP-aadressid. Need on hädavajalikud, et võrgus liikuvad andmed jõuaksid õige seadmeni.

## MAC ja IP aadressid

MAC-aadress on seadme "füüsiline aadress", mis on unikaalne ja seotud seadme riistvaraga. Seda võiks võrrelda inimese sõrmejäljega – igal seadmel on oma kordumatu jälg, mida ei saa muuta. Kui kaks seadet on samas võrgus, suhtlevad nad omavahel MAC-aadresside kaudu.

Teisest küljest on IP-aadress rohkem nagu postiaadress. See võib muutuda sõltuvalt sellest, millises võrgus seade parajasti asub. IP-aadressid on vajalikud siis, kui seadmed suhtlevad suuremate võrkude kaudu, näiteks internetis.

![MAC vs IP](/lectures/images/mac_vs_ip.png)

Kujutame ette, et saadad oma arvutist dokumendi koduprinterile. Kuna printer ja arvuti on samas kohalikus võrgus, kasutab arvuti printeri leidmiseks selle MAC-aadressi. Kui aga soovid veebilehele minna, saadab su arvuti päringu läbi interneti, kasutades selleks IP-aadressi.

Nii MAC kui ka IP-aadressid on olulised, aga vahel on vaja neil aadressidel omavahel suhelda ja andmeid vahetada. Siin tuleb mängu ARP-protokoll.

---

### ARP ja aadresside lahendamine

Kui sa tead ainult seadme IP-aadressi, aga mitte selle MAC-aadressi, aitab ARP ehk Address Resolution Protocol. ARP toimib taustal ja aitab seadmetel IP-aadresside kaudu MAC-aadresse tuvastada. Näiteks, kui sa tahad saata andmeid koduvõrgus olevale printerile, teeb ARP päringu ja leiab selle MAC-aadressi, mis võimaldab andmed õigesti edasi saata.

ARP võib olla haavatav rünnakutele. Näiteks ARP spoofing on tehnika, kus ründaja manipuleerib ARP-protokolli, teeseldes, et ta on keegi teine, ning suunab võrguliikluse endale.

![ARP Diagramm](/lectures/images/arp_diagram.png)

Kuigi ARP aitab meil seadmeid kohalikus võrgus ühendada, on suuremahuliste võrkude jaoks tarvis keerukamaid lahendusi. Siin tuleb mängu IPv6 ja Neighbor Discovery Protocol (NDP).

---

### IPv6 ja Neighbor Discovery

Interneti laienemise ja seadmete arvu kasvuga hakkab IPv4-aadresse maailmas väheks jääma. IPv6 on uus protokoll, mis lahendab selle probleemi, pakkudes tunduvalt rohkem aadresse. Kui IPv4-võrgus toimib aadresside lahendamine ARP abil, siis IPv6 võrgus teeb seda Neighbor Discovery Protocol (NDP). NDP on turvalisem ja võimaldab seadmetel üksteist avastada ja andmeid vahetada, samuti nagu ARP, aga efektiivsemalt ja kindlamalt.

![IPv6 Neighbor Discovery](/lectures/images/ipv6_neighbor_discovery.png)

IPv6 pakub lahenduse sellele, et internetis saaks olla miljardeid rohkem seadmeid – alates nutitelefonidest kuni autode ja isegi kodumasinateni. Igaüks neist vajab unikaalset IP-aadressi, et saaksid omavahel suhelda ja andmeid vahetada.

IPv6-s on võimalik luua 340 undecillion aadressi. See tähendab, et iga liivatera planeedil võiks saada oma IP-aadressi – ja jääks isegi üle!

Kui soovid seadistada IPv6-aadressi, võib see välja näha nii:

```bash
sudo ip -6 addr add 2001:db8::1/64 dev eth0
```

---

# Ruuteri seadistamise õpik

## 1. Esmased seadistused ruuterile

Ruuter on nagu kuller, kes toimetab andmeid ühest kohast teise. Kui ta ei tea, kuhu andmed saata, siis ei jõua need õigesse kohta. Ruuteri seadistamine on vajalik, et kõik seadmed (nagu arvutid, telefonid, mängukonsoolid) saaksid omavahel andmeid vahetada ja internetti kasutada.

![Ruuteri seadistamise sammud](/lectures/images/router_setup_steps.png)

### Esimesed sammud

1. **Ühenda ruuter vooluvõrku ja arvutiga.**
2. **Sisenemine ruuteri seadistamisliidesesse** – IP-aadressi kaudu (`192.168.1.1`).
3. **Esimesed käsud:**

```bash
Router(config)# hostname MinuRuuter
Router(config)# ip address 192.168.1.1 255.255.255.0
```

Esimene interneti ruuter loodi 1981. aastal, ja selle töö kiirus oli umbes **56 kbit/s** – rohkem kui **1000 korda aeglasem** kui kiirus, mida täna kodus kasutad!

## 2. Liideste seadistamine

Liidesed on ruuteri "käed ja jalad". Iga liides võimaldab ruuteril suhelda erinevate võrkudega. Selleks, et liidesed töötaksid, tuleb need õigesti seadistada.

![Liideste seadistamise näide](/lectures/images/interface_setup.png)

### Liideste seadistamine

1.**IP-aadressi määramine liidesele:**

```bash
Router(config-if)# ip address 192.168.1.2 255.255.255.0
```

2.**Liidese aktiveerimine:**

```bash
Router(config-if)# no shutdown
```

3.**Kontrolli liideste seadistust:**

```bash
Router# show ip interface brief
```

Suurettevõtetes võib ühel ruuteril olla **sadu liideseid**, samas kui koduruuteril on tavaliselt ainult üks või kaks.

## 3. Vaikelüüs – Uks internetti

Vaikelüüs on nagu "uks", mis viib sind kohalikust võrgust välja suuremasse internetti.

![Vaikelüüsi määramine](/lectures/images/default_gateway_setup.png)

### Vaikelüüsi seadistamine

1. **Vaikelüüsi määramine ruuterile:**

```bash
Router(config)# ip default-gateway 192.168.1.1
```

Vaikelüüs on nii oluline, et kui see on seadistamata, siis pole võimalik internetti saada – justkui uks oleks igaveseks lukku pandud!

## Kõik on omavahel seotud

Ruuteri põhiseadistused, liideste seadistamine ja vaikelüüsi määramine on kõik omavahel tihedalt seotud. Kujuta ette, et ruuter on nagu suur logistika keskus, kust liiguvad pakid (andmed) erinevatesse kohtadesse. Selleks, et pakid jõuaksid õigesse kohta, peavad olema seadistatud liidesed (maanteed), ja vaikelüüs (välisuks) aitab need andmed internetti viia.

![Ruuteri töö loogika](/lectures/images/router_logic.png)

---

# IPv4 Aadressimine ja Seadmete Konfiguratsioonid

## Sissejuhatus IPv4

Interneti kasutamiseks vajavad kõik seadmed unikaalset aadressi, mida kutsutakse **IP-aadressiks**. **IPv4** (Internet Protocol version 4) on üks peamisi protokolle, mille kaudu seadmed internetis omavahel suhtlevad. IPv4 aadress koosneb neljast numbrist, mida eraldavad punktid, ja igal numbril on väärtus vahemikus 0–255. See aadress määrab seadme asukoha võrgus, võimaldades tal andmeid saata ja vastu võtta.

### Näide IPv4 aadressist

- **192.168.1.1** – see on tavaline IPv4 aadress, mida näeme koduvõrkudes.

---

### IPv4 Aadressi Struktuur

IPv4 aadress koosneb kahest osast:

1. **Võrgu osa** (Network) – määrab, millisesse võrku seade kuulub.
2. **Hosti osa** (Host) – määrab konkreetse seadme võrgus.

See sarnaneb tavalise postiaadressiga: võrguaadress on nagu linna ja tänava nimi ning hostiaadress on maja number. Võrgumask aitab eristada, milline osa aadressist kuulub võrgule ja milline seadmele.

#### Näide

- **IP-aadress:** 192.168.1.10
- **Võrgumask:** 255.255.255.0  
See tähendab, et võrguaadress on **192.168.1.0** ja hostide aadressid selles võrgus on vahemikus **192.168.1.1** kuni **192.168.1.254**.

---

### Avalikud ja Privaatvõrgu Aadressid

**Avalikud IP-aadressid** on need, mida kasutavad seadmed, et suhelda ülemaailmses internetis, ja need peavad olema unikaalsed. **Privaatvõrgu IP-aadressid** on mõeldud kasutamiseks ainult kohalikus võrgus, näiteks kodus või kontoris.

#### Privaatsete IP-aadresside vahemikud

- **192.168.x.x**
- **10.x.x.x**
- **172.16.x.x – 172.31.x.x**

Neid privaatseid aadresse ei kasutata internetis, vaid ainult kohalikus võrgus. Kui seadmed soovivad ühenduda internetiga, kasutab ruuter avalikku IP-aadressi.

---

### Unicast, Broadcast ja Multicast

IPv4 aadresse saab kasutada andmete saatmiseks kolmel viisil:

1. **Unicast** – andmed saadetakse ühele seadmele.
2. **Broadcast** – andmed saadetakse kõigile seadmetele võrgus.
3. **Multicast** – andmed saadetakse kindlale seadmete grupile.

Näiteks kui saadad e-kirja ühele sõbrale, kasutad **unicast**-aadressimist. Kui tahad jagada midagi kõigile seadmetele võrgus (nt ruuterile saadetud käsklus), kasutad **broadcast**-aadressimist.

---

## Alavõrkude Konfigureerimine (Subnetting)

Suurte võrkude efektiivseks haldamiseks jagatakse neid tihti **alavõrkudeks**. Alavõrkude loomine põhineb võrgumaskidel. See võimaldab võrguressursse paremini hallata ja tagab tõhusama andmevahetuse.

Kui sul on võrguaadress **192.168.1.0/24** (255.255.255.0), võid jagada selle kaheks alavõrguks kasutades võrgumaski **255.255.255.128**. See jagab võrguaadressid kaheks alavõrguks, millest mõlemas saab olla kuni 126 seadet.

- **Alavõrk 1:** 192.168.1.0 – 192.168.1.127
- **Alavõrk 2:** 192.168.1.128 – 192.168.1.255

### Võrguseadistuse sammud

1. Ava oma ruuteri või switchi konfiguratsioonitööriist (veebipõhine või CLI).
2. Määra seadmele IP-aadress (nt **192.168.1.1**).
3. Määra võrgumask (nt **255.255.255.128**).
4. Kinnita muudatused ja testi, kas seadmed saavad omavahel suhelda.

---

### Ruuteri Algseadistus

Iga võrguseade vajab algseadistamist, et suhelda võrguga. **Ruuteri seadistamine** on üks esimesi samme, kui ehitad võrku.

1.**Ava CLI** (Command Line Interface) – enamasti saad sellele ligi kaabelühenduse kaudu või veebiliidese kaudu.
2.**Sisene ruuteri konsooli**:

```bash
enable
```

   See lülitab CLI administratiivrežiimi.

3.**Määra ruuteri IP-aadress** (ruuteri LAN-pordile):

```bash
configure terminal
interface gigabitethernet 0/1
ip address 192.168.1.1 255.255.255.0
no shutdown
```

   Siin määrame ruuteri LAN-aadressiks **192.168.1.1** ja võrgumaskiks **255.255.255.0**.

4.**Salvesta konfiguratsioon**:

```bash
write memory
```

---

### Ruuteri Liideste Seadistamine

Peale ruuteri algseadistamist tuleb seadistada **liidesed** (interfaces), et ruuter saaks ühendust luua võrguga.

#### Näide liideste seadistusest

Kui ruuteril on kaks võrku (nt üks koduvõrk ja teine internetiühendus), peab kummalegi võrgule määrama oma liidese.

#### Sammud

1.**Sisene liidese seadistusse** (näiteks internetiühenduse jaoks):

```bash
interface gigabitethernet 0/0
ip address 10.0.0.1 255.255.255.252
no shutdown
```

2.**Seadista teine liides koduvõrgu jaoks**:

```bash
interface gigabitethernet 0/1
ip address 192.168.1.1 255.255.255.0
no shutdown
```

Nüüd on ruuter ühendatud nii koduvõrgu kui ka internetiga, ja võrguliiklus saab hakata liikuma.

---
