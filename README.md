# Elevate Labs – Cyber Security Internship | Task 2 🛡️

## 🎯 Task Objective

Analyze a phishing email sample and identify suspicious traits using header analysis, grammar checks, domain inspection, and content red flags. The goal is to understand how phishing works and how to detect threats early.

---

## 🧰 Tools Used

- Sample phishing email from CanIPhish.com
- Manual inspection of sender, content, and domain
- Simulated email header analysis
- Markdown and GitHub for documentation

---

## 🪜 Steps Followed

### 1. Chose a Sample Email

- Source: [CanIPhish – Job Opportunity Phishing Sample](https://caniphish.com/email-phishing-simulator?email=Job-Opportunity)
- Added full body in: `phishing_email_sample.txt`

---

### 2. Analyzed Red Flags in the Email

- Found fake domain: `morganstanley-careers.com`
- Used generic/unprofessional tone
- Pushed urgency (“APPLY NOW” in all caps)
- Mentioned fake attachment: `Job_Application_Form.doc`

Details in: `phishing_indicators.md`

---

### 3. Simulated Email Header Analysis

Key red flags:
- Return path mismatch
- IP address not linked to real company
- No DKIM/SPF/DMARC validation
- Missing signature & reply-to info

Details in: `header_analysis.txt`

---

## 📁 Files in This Repo

| File Name                 | Description                                               |
|---------------------------|-----------------------------------------------------------|
| `README.md`               | Full explanation of the task and steps                    |
| `phishing_email_sample.txt` | Raw phishing email content                              |
| `phishing_indicators.md` | Listed suspicious traits in the email                     |
| `header_analysis.txt`     | Header spoofing and email source analysis                 |
| `screenshots/` *(optional)*| If added, screenshots of analysis go here                |

---

## 🧠 What I Learned

- How phishing emails trick users using urgency & impersonation  
- Common red flags in email headers and body content  
- Importance of domain awareness and proper email formatting  
- Documenting cybersecurity findings professionally

---

📌 [Submission Link](https://forms.gle/8Gm83s53KbyXs3Ne9)
