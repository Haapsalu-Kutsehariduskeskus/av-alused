# Nädal 5: Võrguseadmed ja nende haldamine (Moodulid 16-17)

# Võrguseadmete Ülevaade

Võrguseadmed on võrgu infrastruktuuri olulised osad, mis tagavad andmete liikumise, turvalisuse ja haldamise. Selles ülevaates käsitleme kolme peamist võrguseadmete tüüpi: **lülitid (switchid)**, **ruuterid** ja **3-kihi (Layer 3) switch**. Lisaks selgitame nende füüsilisi omadusi, valgusdioodide (LED) tähendusi ja seadmete lähtestamise meetodeid.

## 1. Lülitid (Switchid)
Lülitid on seadmed, mis ühendavad võrgus erinevaid seadmeid, nagu arvutid ja printerid, ning suunavad andmeid nende vahel.

- **Ethernet-pordid (RJ45)**: Kasutatakse seadmete ühendamiseks võrku.
- **Konsoolport**: Kasutatakse seadme lokaalseks seadistamiseks CLI kaudu.
- **SFP-pordid**: Kasutatakse fiiberoptilisteks ühendusteks, mis tagavad kiiremad ja pikamaaühendused.
- **LED-tulukesed**:
  - **Roheline tuli**: Näitab, et seade on ühendatud ja töötab korralikult. Kui tuli vilgub, siis toimub andmevahetus.
  - **Oranž tuli**: Võib viidata aeglasemale ühendusele või dupleksi sobimatusele (näiteks poole-dupleksi režiim).

![Switchi pordid ja LED-id](/lectures/images/switch_ports_and_leds.png)

**Täiendav info**:
- [Artikkel lülitite lähtestamisest ja pordide tähendustest](https://robots.net/news/how-do-you-reset-a-network-switch)


## 2. Ruuterid
Ruuterid suunavad andmepakette erinevate võrkude vahel, näiteks sisevõrgu ja interneti vahel.

- **WAN-port**: Kasutatakse ühenduse loomiseks internetiga.
- **LAN-port**: Kohalik ühendus sisevõrguga.
- **Reset-nupp**: Väike süvendatud nupp, mida vajutatakse seadme lähtestamiseks. Selleks on vaja kasutada nõela või kirjaklambrit.

![Ruuteri pordid ja nupud 1](/lectures/images/router_ports_buttons1.png)
![Ruuteri pordid ja nupud 2](/lectures/images/router_ports_buttons2.png)
**Täiendav info**:
- [Artikkel ruuteri lähtestamisest ja LED-tulede tähendustest](https://www.softhandtech.com/decoding-ethernet-port-lights)

## 3. 3-kihi (Layer 3) switch

Switch, mis suudab teha nii võrgu lülitamise (Layer 2) kui ka marsruutimise (Layer 3) ülesandeid. Näiteks Cisco Catalyst 3560 on populaarne 3-kihi switch, mis ühendab VLAN-e ja suudab marsruutida andmepakette erinevate võrkude vahel, ilma et oleks vaja eraldi ruuterit. See on kasulik suuremates ettevõttevõrkudes, kus on vaja kiiret andmeedastust ja ühenduse suunamist erinevate alamvõrkude vahel.

## 4. Võrguseadmete Paigutus

Võrguseadmed paigutatakse kolme peamise kihi järgi:

1. **Core kiht** on võrgu keskne osa, mis ühendab kõik võrgu osad ja võimaldab kiiret andmevahetust. Siin asuvad võimsad 3-kihi switchid, mis suunavad andmepakette erinevate alamvõrkude vahel.

2. **Distribution kiht** koondab liikluse väiksematest võrgusegmentidest ja suunab selle core kihile. Siin kasutatakse L2 ja L3 switch'e, mis suudavad nii lülitada kui marsruutida.

3. **Access kiht** ühendab lõppkasutajate seadmed võrku, näiteks arvutid ja printerid. Sellel kihil kasutatakse tavalisi switch'e ja ruutereid.

See kolmekihiline mudel tagab, et andmed liiguvad kiiresti ja tõhusalt läbi kogu võrgu.

![Võrgu hierarhia](/lectures/images/network_hierarchy.png)

## 5. Seadmete Lähtestamine

- **Lüliti lähtestamine CLI kaudu**:
  1. Ühenda konsoolipordiga ja logi CLI-sse sisse.
  2. Kasuta käsku `erase startup-config` ja seejärel `reload`, et seade lähtestada tehase seadetele.

- **Ruuteri lähtestamine nuppu kasutades**:
  - Vajuta ja hoia reset-nuppu 10-30 sekundit, kuni LED hakkab vilkuma.

---

Selle põhjalikuma ülevaate ja lisainfo saamiseks tutvu täiendavate ressurssidega:
- [Robots.net - Lüliti lähtestamine](https://robots.net/news/how-do-you-reset-a-network-switch)
- [Cisco Documentation - Etherneti porditulede tähendused näide](https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst9500/hardware/install/b_catalyst_9500_hig/9500-leds.pdf)
