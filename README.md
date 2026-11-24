# STY Erronka 2 · Planifikazioa eta Atazen Jarraipena

> **Proiektua:** STY (ServersToYou) – *Uni Center: Enpresa baten IT sistemen ezarpena*  
> **Zentroa:** Uni Eibar-Ermua · SISA 2  
> **Data:** 2026ko Azaroak 24 (Semana 6 / Exekuzio Fasea)  
>
> Dokumentu bakarra atazen egoera eta denbora-erregistroa moduluka jarraitzeko:
> * 🔴 **Sin hacer (Egiteke)**
> * 🟡 **Haciendo (Egiten ari gara / Martxan)**
> * 🟢 **Hecho (Eginda)** *(Tardatutako denborarekin / Denbora-erregistroa)*

---

## 📊 Aurrerapenaren eta Denboraren Laburpen Orokorra

| Asignatura / Modulua | Eginda | Egiten | Egiteke | Tardatutako Denbora Guztira |
| :--- | :---: | :---: | :---: | :---: |
| **1. SEA** · Sistema Eragileen Administrazioa | 2 | 2 | 3 | **6,5 ordu** |
| **2. SZERI** · Sareko Zerbitzuak eta Internet | 2 | 1 | 2 | **5,0 ordu** |
| **3. SEG** · Segurtasuna eta Datu Babesa | 1 | 1 | 3 | **3,0 ordu** |
| **4. DBKSA** · Datu Baseak Kudeatzeko Sistemak | 1 | 2 | 2 | **4,0 ordu** |
| **5. WAE & IAW** · Web Aplikazioak eta Garapena | 2 | 1 | 2 | **5,5 ordu** |
| **6. HW** · Hardwarearen Oinarriak | 1 | 1 | 1 | **3,0 ordu** |
| **7. SB** · Sistema Banatuak eta HA Klusterra | 1 | 0 | 3 | **2,5 ordu** |
| **8. PROG** · Sistemen Programazioa eta IoT | 0 | 1 | 3 | **0,0 ordu** |
| **9. HACK** · Hacking Etikoa eta Auditoria | 0 | 1 | 2 | **0,0 ordu** |
| **10. JASAN** · Jasangarritasuna eta Ekonomia Zirkularra | 1 | 0 | 1 | **2,0 ordu** |
| **GUZTIRA** | **10** | **10** | **22** | **31,5 ordu** |

---

## 1. Sistema Eragileen Administrazioa (SEA)

### 🔴 Sin hacer (Egiteke)
* [ ] Enpresa berriaren Windows Server domeinua sortu eta bi domeinuen arteko konfiantza-erlazioa konfiguratu (bi norabidekoa).
* [ ] Mantentze-atazak automatizatu Task Scheduler eta cron bidez (segurtasun kopiak eta disko garbiketa).
* [ ] Irisgarritasun lanpostuak prestatu ikusmen murriztuko 2 langileentzat (NVDA, Windows Lupa eta kontraste altua).

### 🟡 Haciendo (Egiten ari gara)
* [ ] Active Directory departamentuen OU hierarkia eta segurtasun-taldeak (`GRP_Teknikariak`) egituratzen.
* [ ] Bekadun berriarentzako PowerShell administrazio-gidoiak idazten eta OpenSSH bidezko urruneko konexio segurua probatzen.

### 🟢 Hecho (Eginda)
* [x] Windows Server 2022 instalatu, AD DS eta DNS rolak gehitu eta `sty.lan` baso nagusia promozionatu.  
  ⏱️ **Tardatutako denbora:** `4,0 ordu`
* [x] Enpresako ekipo bezeroak domeinura gehitzeko proba arrakastatsua burutu.  
  ⏱️ **Tardatutako denbora:** `2,5 ordu`

> **SEA guztira tardatutakoa:** `6,5 ordu`

---

## 2. Sareko Zerbitzuak eta Internet (SZERI)

### 🔴 Sin hacer (Egiteke)
* [ ] vsftpd zerbitzarian SSL/TLS ziurtagiria (FTPS) aktibatu eta karpeten baimen isolatuak (`chroot`) ezarri.
* [ ] Web zerbitzariaren (Apache) gune birtualak (vhosts) eta HTTPS ziurtagiri digitalak konfiguratu.

### 🟡 Haciendo (Egiten ari gara)
* [ ] DNS zerbitzarian kanpoko birbidaltzaileak (Forwarders) eta barne-eremuko erregistroak (`A`, `CNAME`, `MX`) doitzen.

### 🟢 Hecho (Eginda)
* [x] pfSense routerrean interfazeak banatu eta IP helbideratze estatikoa ezarri (WAN, LAN: `192.168.10.0/24`, DMZ: `192.168.20.0/24`).  
  ⏱️ **Tardatutako denbora:** `3,0 ordu`
* [x] LAN sarerako DHCP zerbitzua konfiguratu parametro osagarriekin (atebidea, DNSa eta erreserbak).  
  ⏱️ **Tardatutako denbora:** `2,0 ordu`

> **SZERI guztira tardatutakoa:** `5,0 ordu`

---

## 3. Segurtasuna eta Datu Babesa (SEG)

### 🔴 Sin hacer (Egiteke)
* [ ] OpenVPN zerbitzaria eta CA ziurtagiriak pfSense-n konfiguratu urruneko langileak LANera seguru konektatzeko.
* [ ] Segurtasun kopien sistema automatizatua martxan jarri (`rsync` bidezko sinkronizazioa).
* [ ] Honeypot eta IDS/IPS (Suricata) zaintza-sistema ezarri alertak eta erregistroak aztertzeko.

### 🟡 Haciendo (Egiten ari gara)
* [ ] pfSense suebakiaren iragazte-arauak ezartzen (DMZ isolamendua, LAN irteera arauak eta blokeo log-ak).

### 🟢 Hecho (Eginda)
* [x] Segurtasun perimetralaren azterketa eta arriskuen analisia osatu (sarbide-politikak eta pasahitz-irizpide sendoak).  
  ⏱️ **Tardatutako denbora:** `3,0 ordu`

> **SEG guztira tardatutakoa:** `3,0 ordu`

---

## 4. Datu Baseak Kudeatzeko Sistemak (DBKSA)

### 🔴 Sin hacer (Egiteke)
* [ ] SQL prozedura biltegiratuak (`stored procedures`) eta funtzio deterministak garatu aplikazioaren komunikaziorako.
* [ ] Triggerrak sortu datu-aldaketen historikoa auditoretza-taula batean automatikoki gordetzeko.

### 🟡 Haciendo (Egiten ari gara)
* [ ] `bind-address` konfigurazioa ezartzen (administratzailea soilik LANetik konektatu ahal izateko eta kanpotik blokeatzeko).
* [ ] Datu-baseko erabiltzaile-kontuak eta rolak sortzen (`GRANT` baimen zehatzekin).

### 🟢 Hecho (Eginda)
* [x] MariaDB zerbitzaria instalatu Debian makinan eta intraneteko datu-basearen eskema (`db_intranet`, `erabiltzaileak`, `iruzkinak`) diseinatu.  
  ⏱️ **Tardatutako denbora:** `4,0 ordu`

> **DBKSA guztira tardatutakoa:** `4,0 ordu`

---

## 5. Web Aplikazioak eta Garapena (WAE & IAW)

### 🔴 Sin hacer (Egiteke)
* [ ] Erabiltzaileen iruzkinen panela garatu datu-basearekin konektatuta (iruzkinak bidali eta argitaratu).
* [ ] Ticketing aplikazioa (GLPI) instalatu eta intranetaren menuan sarbidea integratu.

### 🟡 Haciendo (Egiten ari gara)
* [ ] Intranetaren saio-hasiera garatzen (`login.php`, `index.php`, pasahitzen hash egiaztapena PHP bidez).

### 🟢 Hecho (Eginda)
* [x] GitHub biltegia antolatu, Git lan-fluxua (`develop`, `feature/*`) eta taldeko lankidetza-arauak ezarri.  
  ⏱️ **Tardatutako denbora:** `2,5 ordu`
* [x] Intranetaren interfaze grafiko korporatiboa diseinatu eta maketatu (HTML5 eta CSS korporatiboa).  
  ⏱️ **Tardatutako denbora:** `3,0 ordu`

> **WAE & IAW guztira tardatutakoa:** `5,5 ordu`

---

## 6. Hardwarearen Oinarriak (HW)

### 🔴 Sin hacer (Egiteke)
* [ ] Ekipo bezeroen eta zerbitzarien berreskuratze-irudi osoak sortu eta gorde (Clonezilla bidez).

### 🟡 Haciendo (Egiten ari gara)
* [ ] Datu-zentroaren baldintzak dokumentatzen (SAI/UPS potentzia kalkulua eta Hot-Swap diskoen kudeaketa).

### 🟢 Hecho (Eginda)
* [x] Enpresak erabiliko duen hardware eta software lizentzien azterketa eta aurrekontu-txostena burutu.  
  ⏱️ **Tardatutako denbora:** `3,0 ordu`

> **HW guztira tardatutakoa:** `3,0 ordu`

---

## 7. Sistema Banatuak eta HA Klusterra (SB)

### 🔴 Sin hacer (Egiteke)
* [ ] Proxmox VE 2 nodoko klusterra eratu eta zerbitzuen Alta Eskuragarritasuna (HA) aktibatu.
* [ ] Makina birtual baten erorketa-simulazioa (failover) probatu zerbitzua gelditu gabe.
* [ ] Active Directory GPO bidez unitate sareak (Z:) automatikoki mapeatu bezeroei.

### 🟡 Haciendo (Egiten ari gara)
* *Une honetan ez dago atazarik martxan atal honetan (hurrengo sprint-ean hasiko da).*

### 🟢 Hecho (Eginda)
* [x] TrueNAS biltegiratze zerbitzaria hedatu eta ZFS biltegiratze igerilekua (Pool) prestatu.  
  ⏱️ **Tardatutako denbora:** `2,5 ordu`

> **SB guztira tardatutakoa:** `2,5 ordu`

---

## 8. Sistemen Programazioa eta IoT (PROG)

### 🔴 Sin hacer (Egiteke)
* [ ] ESP32 / Raspberry Pi mikrokontroladorearekin DHT22 sentsorea konektatu eta zirkuitua muntatu.
* [ ] Sentsorearen datuak (tenperatura eta hezetasuna) REST API / PHP script bidez MariaDBra automatikoki bidali.
* [ ] Intraneteko web interfazean denbora errealeko ingurumen datuen grafikoak txertatu.

### 🟡 Haciendo (Egiten ari gara)
* [ ] Arduino IDE / Python programazio-ingurunea konfiguratu eta datuak biltzeko oinarrizko kodea prestatzen.

### 🟢 Hecho (Eginda)
* *Oraindik ez dago ataza amaiturik modulo honetan.*

> **PROG guztira tardatutakoa:** `0,0 ordu`

---

## 9. Hacking Etikoa eta Auditoria (HACK)

### 🔴 Sin hacer (Egiteke)
* [ ] LANeko zaurgarritasun auditoria egin Nmap eta Metasploit erabiliz eta ahuleziak ustiatu.
* [ ] Auditoretza-txostena eta identifikatutako segurtasun-arazoak konpontzeko kontraneurriak idatzi.

### 🟡 Haciendo (Egiten ari gara)
* [ ] Sarean makina ahulgarria (Metasploitable) txertatu eta laborategiko ingurune isolatua prestatzen.

### 🟢 Hecho (Eginda)
* *Oraindik ez dago ataza amaiturik modulo honetan.*

> **HACK guztira tardatutakoa:** `0,0 ordu`

---

## 10. Jasangarritasuna eta Ekonomia Zirkularra (JASAN)

### 🔴 Sin hacer (Egiteke)
* [ ] IoT sentsoreetatik jasotako datu errealekin enpresaren energia-kontsumoa eta karbono-aztarna kalkulatu.

### 🟡 Haciendo (Egiten ari gara)
* *Une honetan ez dago atazarik martxan atal honetan.*

### 🟢 Hecho (Eginda)
* [x] Jasangarritasun planaren oinarria garatu 3 arloak kontuan hartuta (ingurumena, soziala, ekonomikoa) eta GJH/ODS 2030 helburuekin lotu.  
  ⏱️ **Tardatutako denbora:** `2,0 ordu`

> **JASAN guztira tardatutakoa:** `2,0 ordu`
