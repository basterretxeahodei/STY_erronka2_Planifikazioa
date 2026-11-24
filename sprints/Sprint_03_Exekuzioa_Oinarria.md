# Sprint 3 · Exekuzio Teknikoa I: Oinarrizko Azpiegitura eta Zerbitzuak

> **Datak:** 2026ko Azaroaren 23tik – Azaroaren 27ra  
> **Egoera:** 🚀 Aktibo / Martxan (Uneko Sprint-a)  
> **Helburu Nagusia:** Proposamen formalean onartutako azpiegituraren oinarriak hedatzea: pfSense suebakia, Active Directory basoa, MariaDB zerbitzaria eta Intranetaren oinarrizko kodea.  
> **Mugarri Kritikoa:** 2026-11-25 · 1. Talde Kontrol Puntua irakasleekin.

---

## 🎯 Sprint-aren Helburu Zehatzak

1. **pfSense Router/Suebakia:** WAN, LAN eta DMZ interfazeak operatiboak izatea eta oinarrizko DHCP zerbitzua ematea.
2. **Windows Server Active Directory:** `sty.lan` basoa altxatzea, departamentuen OU egitura sortzea eta PowerShell bidezko erabiltzaileen kudeaketa prestatzea.
3. **MariaDB Datu-Basea:** Sarbide segurua konfiguratzea (`bind-address` LANerako, kanpotik blokeatuta) eta intraneteko datu-basea (`db_intranet`) sortzea.
4. **Intraneta:** GitHub bidez bertsioatutako PHP/HTML interfaze korporatiboa abiaraztea (`login.php`, `index.php`).
5. **Biltegiratzea (TrueNAS):** ZFS igerilekua eta oinarrizko SMB partekatzeak prestatzea.

---

## 📋 Atazen Taula (Kanban)

| ID | Ataza | Modulua | Arduraduna | Estimazioa | Egoera | GitHub Adarra |
| :---: | :--- | :--- | :--- | :---: | :---: | :--- |
| **#01** | Windows Server 2022 AD DS eta DNS instalatu | `mod:AD-SEA` | Hodei B. | 4h | `Done` | `feature/ad-install` |
| **#02** | OU hierarkia eta GRP_Teknikariak segurtasun taldea sortu | `mod:AD-SEA` | Hodei B. | 3h | `In Progress` | `feature/ad-ou-hierarchy` |
| **#03** | Bekadunarentzako PowerShell gidoiak eta OpenSSH zerbitzua | `mod:AD-SEA` | Jokin C. | 3h | `In Progress` | `feature/ssh-ad-scripts` |
| **#04** | pfSense suebakia instalatu eta 3 sareak (WAN/LAN/DMZ) banatu | `mod:SZERI` | Kidea 3 | 4h | `Done` | `feature/pfsense-interfaces` |
| **#05** | MariaDB instalazioa, bind-address eta `admin_lan` erabiltzailea | `mod:DBKSA` | Jokin C. | 4h | `In Progress` | `feature/mariadb-setup` |
| **#06** | Intraneteko saio-hasiera (`login.php`) eta hash egiaztapena | `mod:WAE-IAW` | Kidea 4 | 5h | `In Progress` | `feature/intranet-auth` |
| **#07** | TrueNAS biltegiratze zerbitzariaren hedapena eta ZFS igerilekua | `mod:HW-IoT` | Kidea 3 | 4h | `To Do` | `feature/truenas-pool` |
| **#08** | GitHub Projects taula eta eguneroko jarraipena egunean jartzea | `mod:WAE-IAW` | Taldea | 2h | `Done` | `feature/planning-daily` |

---

## 🔍 Eguneroko Banaketa (Daily Scrum Xehetasunak)

### 🗓️ Astelehena, 2026-11-23
* **Egindako lana:**
  - pfSense-n LAN eta DMZ interfazeak esleitu ziren.
  - Windows Server-en `sty.lan` domeinua promozionatu zen.
* **Blokeoak:** DNS berbideraketa interneterako erantzun gabe geratu zen; 8.8.8.8 birbidaltzailea gehituta konpondu zen.

### 🗓️ Asteartea, 2026-11-24 [GAUR]
* **Plana:**
  - GitHub Projects planifikazioa osatzea (`STY_erronka2_Planifikazioa`).
  - MariaDB-n erabiltzaileak eta baimenak (`GRANT`) definitzea.
  - Intraneteko saio-hasierako interfazea maketatzea.
* **Arduradunak:** Hodei (Kanban & AD), Jokin (MariaDB & Git Flow), Kidea 3 (pfSense arauak), Kidea 4 (PHP/CSS).

### 🗓️ Asteazkena, 2026-11-25 ⭐ [TALDE KONTROL PUNTUA 1]
* **Helburua:** Irakasleei egindako lana erakustea:
  1. AD domeinua martxan eta bezero bat sartuta.
  2. MariaDB LAN-etik konektagarri baina kanpotik babestuta.
  3. GitHub Projects taula eguneratua eta adarren erabilera.
* **Emaitzen bilketa:** Erronkaren Koadernoan irakasleen iritziak erregistratuko dira.

### 🗓️ Osteguna, 2026-11-26
* **Plana:** TrueNAS biltegiratze partekatua eta GPO bidezko disko mapaketa (Z:).

### 🗓️ Ostirala, 2026-11-27
* **Plana:** Sprint 3 amaierako bateratzea eta Sprint Review bilera laburra.
