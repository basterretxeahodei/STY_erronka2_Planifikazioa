# STY Erronka 2 · Proiektuaren Planifikazioa eta Eguneroko Kudeaketa

> **Zentroa:** Uni Eibar-Ermua  
> **Zikloa:** Sareko Informatika Sistemen Administrazioa (SISA 2)  
> **Ikasturtea:** 2026 - 2027  
> **Proiektua:** ServersToYou (STY) · *Uni Center - Enpresa baten IT sistemen ezarpena*  
> **Gordailu Nagusia (Dokumentazio Teknikoa):** [STY_erronka2](https://github.com/basterretxeahodei/STY_erronka2)  
> **Planifikazio Gordailua:** [STY_erronka2_Planifikazioa](https://github.com/basterretxeahodei/STY_erronka2_Planifikazioa)

---

## 🎯 Helburua eta Ebaluazio Errubrika

Biltegi honen helburua **STY Erronka 2** proiektuaren denbora-kudeaketa, atazen banaketa, GitHub bidezko garapena eta **eguneroko jarraipena** zehaztea eta dokumentatzea da.

Proiektu honek **WAE IE4 (%10)** eta erronka orokorreko ebaluazio-irizpideetan **AURRERATUA (10)** kalifikazioa lortzeko baldintzak betetzen ditu:
* ✅ **GitHub Projects Kanban** taula integratua (To Do, In Progress, Review, Done).
* ✅ **Eguneroko jarraipen zehatza (Daily Scrum)** saio bakoitzeko helburu, egindako ataza eta blokeoekin.
* ✅ **Taldekide guztien parte-hartze aktiboa** rol eta ataza argiekin.
* ✅ **Git Lan-fluxua (Git Flow)**: Garapena `feature/` adarren bidez eta Pull Request bidezko balidazioa.
* ✅ **Irakasleekin kontrol-puntuak** (Asteazkeneroko bilerak eta feedback-aren erregistroa).

---

## 👥 Taldearen Antolaketa eta Rolak

Erronkaren gidan ezarritakoaren arabera, taldea honako rol eta arduretan banatu da:

| Rola | Arduraduna | GitHub Erabiltzailea | Funtzio Nagusiak |
| :--- | :--- | :--- | :--- |
| **Koordinatzailea** | Hodei Basterretxea | `@basterretxeahodei` | Plangintza kontrolatzea, lan-giro ona bultzatzea, barne-bilerak koordinatzea eta GitHub Projects kudeatzea. |
| **Idazkaria / Teknikaria** | Jokin Carrasco | `@Lobus12` | Dokumentazio teknikoa eta aktak biltzea, txostenak egunean edukitzea, Git adarrak bateratzea (PR). |
| **Komunikazio Arduraduna** | *[3. Taldekidea]* | *[Erabiltzailea]* | Taldearen bozeramailea izatea, irakasleekin harremana eta astean behingo informazio-trukearen idatzia egitea. |
| **Laguntzailea / Kudeatzailea** | *[4. Taldekidea]* | *[Erabiltzailea]* | Materialak eta dokumentuak eskura daudela bermatzea, ISOak eta makinak zaintzea, eta denborak kontrolatzea. |

---

## 📊 Planifikazioaren Roadmap Orokorra (Gantt)

```mermaid
gantt
    title STY Erronka 2 · Egutegi Nagusia (9-10 Aste)
    dateFormat  YYYY-MM-DD
    
    section 1. Ikerketa eta Definizioa
    Erronka aurkezpena eta Taldeak         :done, a1, 2026-10-22, 2026-10-23
    Parametroak eta Eskakizunak (2. Eranskina) :done, a2, 2026-10-23, 2026-10-30
    Sare, Sistema eta Segurtasun Ikerketa   :done, a3, 2026-10-26, 2026-11-13
    
    section 2. Proposamena eta Diseinua
    Proposamenen txostena eta Aurkezpena   :done, a4, 2026-11-16, 2026-11-18
    Irakasleen Feedback-a eta Jarduerak     :done, a5, 2026-11-18, 2026-11-20
    
    section 3. Exekuzio Teknikoa
    Astea 6: AD, DNS, pfSense, MariaDB, Intranet :active, a6, 2026-11-23, 2026-11-27
    Kontrol Puntua 1 (Irakasleak)                :crit, active, a6_cp, 2026-11-25, 1d
    Astea 7: Domeinu Konfiantza, VPN, FTPS, Irisgarritasuna :a7, 2026-11-30, 2026-12-04
    Kontrol Puntua 2 (Irakasleak)                :crit, a7_cp, 2026-12-02, 1d
    Astea 8: HA Proxmox Klusterra, ESP32 IoT, Pentesting  :a8, 2026-12-07, 2026-12-11
    Kontrol Puntua 3 (Irakasleak)                :crit, a8_cp, 2026-12-09, 1d
    
    section 4. Itxiera eta Ebaluazioa
    Babeskopiak, Hobekuntzak eta Entsegua       :a9, 2026-12-14, 2026-12-16
    Moduluen Azterketa Teknikoak (Finala)        :a10, 2026-12-17, 2026-12-18
    Azken Aurkezpen Ofiziala                     :a11, 2026-12-21, 2026-12-22
```

---

## 📁 Dokumentazioaren Egitura

* 📄 **[`EGUNEROKO_JARRAIPENA.md`](file:///c:/Users/jokin/Documents/GitHub/STY_erronka2_Planifikazioa/EGUNEROKO_JARRAIPENA.md)**: Proiektuaren egun bakoitzeko erregistroa (Daily Standup, zer egin den, arduraduna, blokeoak eta hurrengo pausoak).
* 📄 **[`KANBAN_PROIEKTUA.md`](file:///c:/Users/jokin/Documents/GitHub/STY_erronka2_Planifikazioa/KANBAN_PROIEKTUA.md)**: GitHub Projects-en erabiltzen den Kanban taularen egitura, etiketak (Labels) eta atazen deskribapen estandarra.
* 📁 **`sprints/`**:
  * `Sprint_01_Ikerketa.md` (Urriak 22 – Azaroak 13)
  * `Sprint_02_Proposamenak.md` (Azaroak 16 – Azaroak 20)
  * `Sprint_03_Exekuzioa_Oinarria.md` (Azaroak 23 – Azaroak 27) 👈 *Unekotzat hartua*
  * `Sprint_04_Exekuzioa_Zerbitzuak.md` (Azaroak 30 – Abenduak 04)
  * `Sprint_05_Exekuzioa_HA_eta_Auditoria.md` (Abenduak 07 – Abenduak 11)
  * `Sprint_06_Itxiera_eta_Ebaluazioa.md` (Abenduak 14 – Abenduak 22)

---

## 🛠️ Erabilitako Tresnak

* **GitHub Projects:** Kanban taula interaktiboa atazen jarraipena egiteko.
* **Git & GitHub:** Bertsio kontrola, adarrak (`develop`, `feature/*`) eta Pull Request berrikuspenak.
* **Draw.io / Mermaid:** Sarearen topologia-eskemak eta Gantt diagramak.
* **Trello / Google Workspace:** Bilera aktak eta materialen zerrenda.
