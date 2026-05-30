### Risk Acceptance Register - CIS Ubuntu 24.04 LTS (VM QEMU)

| ID CIS      | Controllo (breve)                                                                                                            | Motivazione Acceptance                                                                                                                | Livello Rischio | Compensating Control                                                  | Owner                                | Data       | Stato    | Review     |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | --------------- | --------------------------------------------------------------------- | ------------------------------------ | ---------- | -------- | ---------- |
| **1.1.2**   | Requisiti partizioni separate + opzioni mount (nodev/nosuid/noexec) su /tmp, /home, /var, /var/log, /var/log/audit, /var/tmp | Ambiente VM single-disk (QEMU). Ripartizionamento richiede reinstallazione completa del sistema. Non fattibile in produzione attuale. | **Medium**      | Monitoraggio continuo con AIDE + auditd + Wazuh + immutabilità regole | Security Administrator (Simulazione) | 29/05/2026 | Accepted | 31/12/2026 |
| **1.3.1.2** | AppArmor abilitato nel bootloader                                                                                            | In ambiente VM QEMU/KVM il bootloader (grub) è gestito dall’hypervisor. Modifica non persistente o non necessaria.                    | **Low**         | AppArmor abilitato a runtime + policy enforce                         | Security Administrator (Simulazione) | 29/05/2026 | Accepted | 31/12/2026 |
| **1.4.1**   | Bootloader password                                                                                                          | Ambiente virtualizzato. Password del bootloader ha scarsa utilità (hypervisor già protegge l’accesso).                                | **Low**         | Accesso fisico/VM protetto da hypervisor + autenticazione forte       | Security Administrator (Simulazione) | 27/05/2026 | Accepted | 31/12/2026 |

**Note generali di accettazione rischio:**
- Tutti i controlli: _separate partition_ e _mount options_, sono stati accettati in blocco perché richiedono un **ripartizionamento** che non è compatibile con l’attuale infrastruttura VM senza una reinstallazione da zero
-  Rischio accettato e compensating controls già attivi: **AIDE + auditd immutabile + Wazuh + hardening SSH + firewall**





