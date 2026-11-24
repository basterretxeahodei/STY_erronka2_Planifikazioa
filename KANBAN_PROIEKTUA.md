# GitHub Projects · Kanban Egitura eta Atazen Gida (WAE IE4)

> Dokumentu honek GitHub Projects erabiliz taldeak jarraitzen duen kudeaketa-metodologia, taularen zutabeak, etiketak (Labels) eta atazen txantiloiak definitzen ditu.

---

## 📋 1. Kanban Taularen Zutabeak

Gure proiektuko GitHub Projects taulak 4 egoera nagusi ditu:

```text
┌──────────────┐     ┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│    TO DO     │ ──> │ IN PROGRESS  │ ──> │    REVIEW    │ ──> │     DONE     │
│  (Egiteke)   │     │ (Martxan)    │     │(Berrikusten) │     │  (Amaituta)  │
└──────────────└     └──────────────┘     └──────────────┘     └──────────────┘
```

1. **To Do (Egiteke):** Sprint bakoitzerako planifikatutako atazak, lehentasunaren arabera ordenatuta.
2. **In Progress (Martxan):** Kide bat garatzen ari den ataza aktiboak (kide bakoitzak gehienez 1-2 ataza aldi berean).
3. **Review (Berrikusten):** Garapena amaituta, beste taldekide batek egindako lana berrikusteko zain (Pull Request zabalik edo konfigurazioa probatzen).
4. **Done (Amaituta):** Egiaztatuta, funtzionamenduan eta dokumentatuta dagoen ataza.

---

## 🏷️ 2. Etiketak (Labels)

Atazak kategoria eta moduluaren arabera antolatuta daude:

| Etiketa | Kolorea | Deskribapena |
| :--- | :--- | :--- |
| `mod:AD-SEA` | 🔵 Urdina | Active Directory, Windows Server, PowerShell gidoiak. |
| `mod:SZERI` | 🟣 Morea | DNS, DHCP, Web Zerbitzaria, pfSense Sare Zerbitzuak. |
| `mod:SEG` | 🔴 Gorria | Segurtasun perimetrala, OpenVPN, Firewall arauak. |
| `mod:DBKSA` | 🟡 Horia | MariaDB, erabiltzaileak, rolak, prozedurak, triggerrak. |
| `mod:WAE-IAW` | 🟢 Berdea | Intraneta (PHP/HTML), GitHub Projects, ticketing. |
| `mod:SB-HA` | ⚪ Zilarra | Proxmox klusterra, CEPH/ZFS, Erredundantzia. |
| `mod:HW-IoT` | 🟠 Laranja | Berreskuratze irudiak (Clonezilla), ESP32 sentsorizazioa. |
| `mod:HACK` | ⚫ Beltza | Pentesting, makina ahula, zaurgarritasun auditoria. |
| `mod:JASAN` | 🌿 Berde argia | Jasangarritasuna, ESG, GJH 2030 txostena. |
| `mota:bug` | 🛑 Gorri bizia | Funtzionamendu akatsa edo konfigurazio errorea. |
| `mota:feature` | 🟦 Ziana | Funtzionaltasun edo azpiegitura zati berria. |
| `mota:docs` | 📄 Grisa | Dokumentazioa, txostenak eta ebidentziak. |

---

## 🗂️ 3. Sprinten Banaketa eta Mugarriak (Milestones)

* **Milestone 1:** `Sprint 1 - Ikerketa eta Parametroak` *(Urriak 22 - Azaroak 13)*
* **Milestone 2:** `Sprint 2 - Proposamen Formala eta Diseinua` *(Azaroak 16 - Azaroak 20)*
* **Milestone 3:** `Sprint 3 - Exekuzioa I: Oinarrizko Sare eta Zerbitzuak` *(Azaroak 23 - Azaroak 27)*
* **Milestone 4:** `Sprint 4 - Exekuzioa II: Domeinu Konfiantza eta Segurtasuna` *(Azaroak 30 - Abenduak 04)*
* **Milestone 5:** `Sprint 5 - Exekuzioa III: HA Klusterra eta IoT` *(Abenduak 07 - Abenduak 11)*
* **Milestone 6:** `Sprint 6 - Itxiera, Proba Teknikoak eta Azken Aurkezpena` *(Abenduak 14 - Abenduak 22)*

---

## 📝 4. Issue / Ataza Txantiloia

GitHub-en ataza berri bat sortzerakoan erabili beharreko egitura:

```markdown
### 📌 Atazaren Deskribapena
[Zer lortu nahi da ataza honekin? Zein zerbitzu hedatu edo konfiguratu behar da?]

### 🎯 Onarpen Irizpideak (Definition of Done)
- [ ] Zerbitzua instalatuta eta martxan.
- [ ] Erabiltzaile eta baimen isolatuak ezarrita.
- [ ] Bezero batetik konexio proba arrakastatsua eginda.
- [ ] Dokumentazio teknikoan ebidentziak eta pantaila-argazkiak gehituta.

### 👤 Arduraduna eta Modulua
* **Arduraduna:** @erabiltzailea
* **Modulua:** [AD, pfSense, MariaDB, Intranet, etab.]
* **Estimazioa:** [X ordu]
```

---

## 🌿 5. Git Lan-Fluxua (Git Flow)

Ataza bakoitzeko Git adar bat ireki eta amaitzean Pull Request bat sortuko da:

```bash
# 1. Azken aldaketak jaitsi
git checkout main
git pull origin main

# 2. Atazarentzako feature adarra sortu
git checkout -b feature/issue-12-mariadb-konfigurazioa

# 3. Garapena egin eta commit zehatzak burutu
git add .
git commit -m "feat(db): MariaDB instalazioa eta bind-address konfiguratu"

# 4. Urruneko biltegira igo eta Pull Request-a ireki
git push origin feature/issue-12-mariadb-konfigurazioa
```
