## Scope del Progetto

**Oggetto**  
Obiettivo: hardening di server basati su **Ubuntu 24.04 LTS**, sia in ambiente fisico che virtuale

**Attività incluse:**
- Applicazione del **CIS Benchmark Ubuntu 24.04 LTS**
- Obiettivo di conformità: **Level 1 completo** + controlli critici selezionati del **Level 2**
- Implementazione di misure di hardening, configurazione di audit, integrità file (AIDE), logging, permessi, servizi e network security

## Esclusioni (Out of Scope)
- Applicazioni custom e workload applicativi
- Container e orchestrazione (Docker, Podman, Kubernetes)
- Database (PostgreSQL, MySQL, MariaDB, ecc.)
- Configurazione di partizioni crittografate LUKS
- Configurazioni hardware-specifiche (BIOS/UEFI, firmware, hardware RAID)
- Reti e firewall a livello di infrastruttura (gestiti a livello di hypervisor/rete)

## Assumptions
- Gli amministratori dispongono di accesso root/sudo sui server oggetto di hardening
- I sistemi sono in un ambiente controllato e protetto (data center o cloud privato)
- Eventuali rischi residui tecnici saranno documentati nel **Risk Acceptance Register**


**Data di approvazione:** 29 Maggio 2026  
**Approvato da:** Mario Rossi – Security Administrator  

**Versione documento:** 1.0
