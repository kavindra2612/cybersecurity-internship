# 📌 Phishing Email Analysis  

This project demonstrates how to identify a phishing email using a real-world example that impersonates Deloitte but originates from a malicious domain.  

The purpose of this project is to help beginners understand how phishing attacks work and how to detect them using practical analysis techniques.

---

## 🎯 Objective  

- Analyze a real phishing email  
- Identify red flags and attack techniques  
- Understand email authentication (SPF, DKIM, DMARC)  
- Improve cybersecurity awareness  

---

## 🟦 1. What is a Phishing Email?  

A phishing email is a fraudulent message designed to trick users into:

- Clicking malicious links  
- Sharing sensitive information (resume, credentials, banking details)  
- Downloading malware  
- Trusting fake job offers or alerts  

👉 Phishing = Deception + Social Engineering  

---

## 🟦 2. Email Overview  

The analyzed email claims to be:

> “Deloitte – Analyst Trainee Recruitment”

### 🔍 Observations:
- Generic greeting (Dear Candidate)  
- Attractive job opportunity  
- “Upload Resume & Apply” button  
- No personalization  

➡️ Looks professional at first glance but contains multiple red flags.

---

## 🟦 3. Sender Analysis (Spoofing Detection)  

### ✅ Expected Domains:
- @deloitte.com  
- @deloitte.co.in  

### ❌ Actual Sender:
- support@fresherjobsz.com  

🚨 Mismatch between claimed brand and sender domain = Phishing  

---

## 🟦 4. Email Header Analysis  

### ✔ SPF: PASS  
- Valid for fresherjobsz.com  
- Does NOT verify Deloitte  

➡️ SPF PASS ≠ Safe Email  

---

### ✔ DKIM: PASS (Signed by msnd3.com)  
- Signed by third-party domain  
- Not related to Deloitte  

➡️ DKIM mismatch = Suspicious  

---

### ✔ DMARC: PASS  
- Only validates attacker’s domain configuration  

➡️ DMARC PASS ≠ Legitimate Email  

---

### ✔ Mailer Info  
- Bulk mailing software detected  

➡️ Real companies typically use official internal systems  

---

## 🟦 5. Suspicious Link Analysis  

### ❌ Malicious URL:
```
https://freshers.info/question.php?ID=519&title=Deloitte-Recruitment
```

### 🚨 Issues:
- Not an official Deloitte domain  
- Redirects to unrelated website  
- Possible phishing/data theft  

### ✅ Legitimate URLs:
- https://jobs.deloitte.com/  
- https://careers.deloitte.com/  

➡️ Link mismatch = Critical phishing indicator  

---

## 🟦 6. Social Engineering Techniques  

The email uses urgency:

> “Upload Resume & Apply”

➡️ Goal:
- Create pressure  
- Force quick action  
- Reduce user thinking  

---

## 🟦 7. Brand Mismatch  

| Element | Value |
|--------|------|
| Claimed Brand | Deloitte |
| Sender Domain | fresherjobsz.com |
| Link Domain | freshers.info |

➡️ No alignment = Confirmed phishing  

---

## 🟦 8. Content & Professionalism Check  

### Issues:
- Generic greeting  
- No personalization  
- No HR signature  
- Poor formatting  
- No official footer  

### Real Emails Include:
- Candidate name  
- Official HR details  
- Proper formatting  
- Company branding  

---

## 🟦 9. Phishing Indicators Summary  

| Indicator | Finding | Verdict |
|----------|--------|--------|
| Sender Domain | fresherjobsz.com | ❌ Phishing |
| DKIM | msnd3.com | ❌ Suspicious |
| SPF/DMARC | Valid for attacker domain | ⚠️ Misleading |
| Link | freshers.info | ❌ Dangerous |
| Urgency | Immediate action | ❌ Phishing |
| Greeting | Generic | ⚠️ Suspicious |
| Brand Match | No | ❌ Phishing |

---

## 🟥 Final Verdict  

This email is NOT from Deloitte.  

It is a phishing / job scam designed to steal personal information.

---

## 🚫 Do NOT:
- Click any links  
- Upload your resume  
- Reply to the email  

---

## ✅ Do:
- Report as Phishing  
- Delete the email  

---

## 🟦 10. Tools Used  

- Email Header Analysis (Manual)  
- Domain Verification  
- Link Inspection  

---

## 💡 Learning Outcome  

After completing this analysis, you can:

- Identify phishing emails  
- Analyze SPF, DKIM, DMARC  
- Detect fake domains and links  
- Understand social engineering techniques  

---
