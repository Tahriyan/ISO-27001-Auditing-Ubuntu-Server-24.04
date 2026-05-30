# Hardening CIS Benchamrk & ISO 27001 Mapping - Ubuntu 24.04

### 🎯 Obiettivo del Progetto
Dimostrare che è possibile portare un server **Ubuntu 24.04 LTS** in uno stato di buona compliance (**Mappatura ISO 27001** + **CIS Benchmark**) utilizzando solo strumenti gratuiti, senza Ubuntu Pro

### 🛠️ Cosa ho fatto
- Creazione di un comune fittizio che utilizza Nextcloud
- Auditing e hardening manuale su Ubuntu Server 24.04 che contiene dati sensibili del comune
- **Oltre 50 controlli** documentati uno per uno
- Dashboard principale interconnessa su Obsidian
- Automazione parziale con **OpenSCAP**
- Analisi con **Wazuh** (14 falsi positivi documentati)

### 📋 Struttura dei file di controllo
Ogni file all’interno della cartella `Controls/` contiene:
- **Rule ID Wazuh** con nome della regola triggerata
- Requisito di controllo
- Fix applicato
- Motivazione
- Verifica

**Nota:** Alcune regole sono state **aggregate** perché molto simili tra loro 
Alcune regole utilizzano codici Wazuh (non standard CIS) perché Wazuh è stato usato come riferimento pratico per la remediation

### 📚 Fonti utilizzate (trasparenza)
- **CIS Ubuntu Linux 24.04 LTS Benchmark v1.0.0** (principale riferimento)
- **Wazuh CIS Benchmark rules**
- **OpenSCAP / SCAP Security Guide**
- ISO 27001 Annex A (per il mapping di alto livello)

**Consiglio forte:** Scarica il documento ufficiale  
→ **CIS Ubuntu Linux 24.04 LTS Benchmark** (versione più aggiornata)  
Ti sarà molto utile per capire quali controlli sono Level 1 / Level 2 e quali richiedono intervento manuale

### ⚠️ Note importanti
Questo progetto ha richiesto **molto tempo** perché ho applicato manualmente anche i controlli di **Level 2**, che possono causare instabilità se non gestiti con attenzione 
L’obiettivo era capire profondamente cosa si sta facendo, non solo applicare regole

### 📌 Come visualizzare meglio il progetto
Questo repository è stato creato principalmente su **Obsidian** 
**Si consiglia vivamente** di clonare il repo e aprirlo con Obsidian per sfruttare tutti i link interni, il grafo e la Master Dashboard.

### 🚀 Prossimi sviluppi
Il progetto è ancora in fase di ampliamento
Prossimamente aggiungerò:
- Controlli FIM per l'integrità dei file del comune
- Miglior automazione
- Eventuale mapping più completo verso ISO 27001

---

### Struttura del Repository
- `00 - Master Dashboard.md` → Vista complessiva
- `Controls/` → Tutti i controlli documentati
- `automated_remediation/` → Report OpenSCAP e screenshot Wazuh
- `CIS Controls v8 IG 1 Mapped.md`

---

**Feedback benvenuti!**  
Se hai esperienza nel settore, sarò molto grata di ricevere osservazioni, critiche o suggerimenti per migliorare il progetto
