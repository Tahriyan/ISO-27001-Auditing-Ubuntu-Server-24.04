**Automated Remediation**

Questa cartella contiene gli script e la documentazione relativa alla remediation automatizzata eseguita sul server Ubuntu 24.04

**Contenuto:**

- `compliance_report_initial.html` — Report di compliance al 50% prima degli script

![[Wazuh_CIS_Benchmark_v1.0.0(Before).png]]

- `compliance_report_remediated.html` — Report di compliance al 69% dopo l’esecuzione degli script

![[Wazuh_CIS_Benchmark_v1.0.0(After).png]]


- scap-security-guide-0.1.80.tar.gz/ — Cartella contenente tutti gli script utilizzati

```bash
wget https://github.com/ComplianceAsCode/content/releases/download/v0.1.80/scap-security-guide-0.1.80.tar.gz

oscap xccdf eval   --profile xccdf_org.ssgproject.content_profile_cis_level1_server   --report compliance-report.html   ssg-ubuntu2404-ds.xml
```



