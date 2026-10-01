# SOC Incident Investigation: Introduction to Phishing (TryHackMe)


<img width="1577" height="695" alt="Screenshot 2026-10-01 211931" src="https://github.com/user-attachments/assets/1ce9c8b2-5307-4069-833b-ee44227b6aaa" />
<img width="1586" height="689" alt="Screenshot 2026-10-01 211912" src="https://github.com/user-attachments/assets/dabddb96-aa08-4dcf-a3a5-f7852aa6a83f" />
<img width="1535" height="771" alt="Screenshot 2026-10-01 210248" src="https://github.com/user-attachments/assets/1d5db170-6ad5-4e8c-825a-fa2d20903b5e" />

## 📌 Overview
This repository documents the triage, analysis, and resolution of phishing and perimeter-related security alerts within the TryHackMe **SOC Simulator** ("Introduction to Phishing" scenario). 

All alerts in the queue were investigated, classified, and resolved with **100% True Positive** and **100% False Positive** identification accuracy.

---

## 🔍 Incident Investigations

### Case 1: Alert #8816 — Blocked Connection to Blacklisted URL

Reason for Classifying as True Positive: 
upon checking the user clicked a malicious link
hxxp[://]bit[.]ly/3sHkX3da12340

Reason for Escalating the Alert: 
no need for escalation firewall successfully blocked the link

Recommended Remediation Actions: 
advise the user to not click malicious link in browsers

List of Attack Indicators: 
hxxp[://]bit[.]ly/3sHkX3da12340 web-browsing

### Case 2: Alert #8815 — Suspicious External Link (Legitimate HR Email)
* **Severity:** Medium
* **Category:** Phishing
* **Sender:** `onboarding@hrconnex.thm`
* **Recipient:** `j.garcia@thetrydaily.thm`
* **Analyzed URL:** `hxxps[://]hrconnex[.]thm/onboarding/15400654060/j[.]garcia`
* **Classification:** **False Positive**

### Case 3: Alert #8815 —  Email Containing Suspicious External Link

Reason for Classifying as True Positive: 
-upon checking the email contains a malicious link hxxp[://]bit[.]ly/3sHkX3da12340\n\nIf

Reason for Escalating the Alert: 
n/a
Recommended Remediation Actions: 
need to inform user to not click the link from maliscious emails

List of Attack Indicators: 
hxxp[://]bit[.]ly/3sHkX3da12340\n\nIf
urgents@amazon[.]biz

### Case 4: Alert #8817 —  Email Containing Suspicious External Link

Reason for Classifying as True Positive: 
a phishing email impersonating Microsoft
upon checking the email has a malicious link
hxxps[://]m1crosoftsupport[.]co/login

List of Attack Indicators: 
hxxps[://]m1crosoftsupport[.]co/login
102.89.222.143

## 🛠️ Tools & Analyst Skills Demonstrated
* **SIEM / Alert Triage:** Filtering, searching, and managing queue workflows in a SOC environment.
* **Threat Intelligence / OSINT:** Domain/URL reputation lookups, un-shortening links, defanging indicators (`hxxp`).
* **Network & Log Analysis:** Inspecting firewall action logs (allow vs. block) and identifying affected internal hosts.
* **Incident Documentation:** Writing clean, audit-ready case notes and rationale for True Positive vs. False Positive closures.
