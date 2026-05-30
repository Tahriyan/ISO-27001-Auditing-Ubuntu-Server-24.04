# CIS Ubuntu 24.04 LTS - Master Hardening Dashboard

**Stato complessivo:** Completed
**Versione OS:** Ubuntu 24.04 LTS  
**Data ultimo aggiornamento:** 29 Maggio 2026  
**Prossimo audit interno:** 31 Dicembre 2026 
**Responsabile Hardening:** __


### Riepilogo Compliance
| Metrica               | Valore  | Stato   |
| --------------------- | ------- | ------- |
| Controlli CIS Totali  | 279     | -       |
| Compliant             | **212** | **80%** |
| In Lavorazione        | 14      | 🟡      |
| Risk Accepted         | 24      | 🔴      |
| Compensating Controls | 15      | 🟢      |
| False Positive        | 14      | 🟢      |


### Risk Accepted & Compensating Controls

| ID        | Controllo                                       | Motivazione                         | Compensating Control             | Stato       |
| --------- | ----------------------------------------------- | ----------------------------------- | -------------------------------- | ----------- |
| 1.1.2.x   | Partizioni separate + mount options             | VM single-disk → richiede reinstall | AIDE + auditd immutabile + Wazuh | Accepted    |
| 1.4.1     | Bootloader password                             | Scarsa utilità in ambiente VM       | Hypervisor protection + 2FA      | Accepted    |
| 4.2 / 4.4 | UFW + iptables                                  | nftables già configurato            | nftables + default deny          | Compensated |
| 6.1.2.1   | systemd-journal-remote + systemd-journal-upload |                                     | Journald + Wazuh                 | Compensated |
| 6.1.3     | rsyslog                                         |                                     | Journald + Wazuh                 | Compensated |


## Struttura del Repository
- [[01 - Scope & Assumptions]]
- [[02 - Risk Acceptance Register]]
- Controls
- Controls/Compensating-Controls
- automated_remediation



## Stato per Dominio CIS
###### Fix Manuali

**1 Initial Setup**
	[[1.1.1.10 - Disable unused filesystem kernel modules]]
	[[1.3.1.4  - Ensure all AppArmor Profiles are in enforce mode]]
	[[1.5.5 - Ensure Automatic Error Reporting is disabled]]
	[[1.6.2  - Ensure local login warning banner is configured properly]]

**2 Services**
	[[2.1.21 - Ensure mail transfer agent is configured for local-only mode]]
	[[2.3.2.1, 2.3.2.2 - Ensure systemd-timesyncd is enabled and running]]
	[[2.3.3.2  - Ensure chrony is running as user _chrony]]
	[[2.4.2.1 - Ensure at is restricted to authorized users]]

**3 Network**
	[[3.2.1 - Ensure DCCP is disabled]]
	[[3.2.2 -  Ensure TIPC is disabled]]
	[[3.2.3  - Ensure RDS is disabled]]
	[[3.2.4- Ensure SCTP is disabled]]


**4 Host Based Firewall** 
	[[4.2.x  UFW Firewall not used (nftables compensating control)]]
	[[4.3.5 - Ensure nftables base chains exist]]
	[[4.3.10 - Ensure nftables rules are permanent]]
	[[4.4.1.x - iptables not used (nftables compensating control)]]


**5 Access Control**
	[[5.3.2.4  - Ensure password history is remembered]]
	[[5.3.3.1.3 - Ensure lockout for failed password attempts includes the root account]]
	[[5.3.3.2.1,  5.3.3.2.2, 5.3.3.2.3, 5.3.3.2.4, 5.3.3.2.5 Password Complexity]]
	[[5.3.3.3.1, 5.3.3.3.2, 5.3.3.3.3 - Ensure password history remember, enforce_for_root and use_authtok are configured (pam_pwhistory)]]
	[[5.4.1.2 - Ensure minimum days between password changes is configured]]
	[[5.4.2.6  - Ensure root user umask is configured]]

**6 Logging and Auditing** 
	**6.1.1 Configure systemd-journald service** 
		[[6.1.1.3  - Ensure journald log rotation is configured]]
	**6.1.2 Configure journald**
		[[6.1.2.1.x - systemd-journal-remote and systemd-journal-upload removed (alternative journald + Wazuh)]]
		[[6.1.2.3, 6.1.2.4 - Ensure journald Compress and Storage are configured]]
		[[6.1.3.x - rsyslog removed (alternative journald + Wazuh)]]
		[[6.1.4.1  - Ensure access to all logfiles has been configured]]
	**6.2 System Auditing**
		[[6.2.1.1 - Ensure auditd is installed]]
		[[6.2.1.2,  6.2.1.4  - Ensure auditd is enabled and active]]
		[[6.2.1.3 - Auditd early boot and log retention configured]]
		[[6.2.2.2 - Ensure audit logs are not automatically deleted]]
	**6.2.3 Configure auditd Rules**
		[[6.2.3.1  - Ensure changes to system administration scope (sudoers) is collected]]
		[[6.2.3.2 - Ensure actions as another user are always logged]]
		[[6.2.3.3 - Ensure events that modify the sudo log file are collected]]
		[[6.2.3.4 -  Ensure events that modify date and time information are collected]]
		[[6.2.3.5 - Ensure events that modify the system's network environment are collected]]
		[[6.2.3.7 -  Ensure unsuccessful file access attempts are collected]]
		[[6.2.3.8 - Ensure events that modify user group information are collected]]
		[[6.2.3.9 - Ensure discretionary access control permission modification events are collected]]
		[[6.2.3.10 - Ensure successful file system mounts are collected]]
		[[6.2.3.11 - Ensure session initiation information is collected]]
		[[6.2.3.12 - Ensure login and logout events are collected]]
		[[6.2.3.13 - Ensure file deletion events by users are collected]]
		[[6.2.3.14 - Ensure events that modify the system's Mandatory Access Controls are collected]]
		[[6.2.3.15 - Ensure successful and unsuccessful attempts to use the chcon command are collected]]
		[[6.2.3.16 - Ensure successful and unsuccessful attempts to use the setfacl command are collected]]
		[[6.2.3.17 - Ensure successful and unsuccessful attempts to use the chacl command are collected]]
		[[6.2.3.18 - Ensure successful and unsuccessful attempts to use the usermod command are collected]]
		[[6.2.3.19 - Ensure kernel module loading unloading and modification is collected]]
		[[6.2.3.20 - Ensure the audit configuration is immutable]]
	**6.2.4 Configure auditd File Access** 
		[[6.2.4.8 - Ensure audit tools mode is configured]]
		[[6.2.4.9 - Ensure audit tools owner is configured]]
		[[6.2.4.10 - Ensure audit tools are group-owned by root]]
	**6.3 Configure Integrity Checking**
		[[6.3.2 - Ensure filesystem integrity is regularly checked]]
		[[6.3.3 - Ensure cryptographic mechanisms are used to protect the integrity of audit tools]]

**7 System Maintenance**
	**7.1 System File Permissions**
		[[7.1.10 -  Ensure permissions on etc security opasswd are configured]]








