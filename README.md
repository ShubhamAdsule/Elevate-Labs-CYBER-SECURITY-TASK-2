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

## Sample Email 
            From: Talent Acquisition <talent-acquisition@cloud-notification-services[.]com>
            To: john[.]doe@mybusiness[.]com
            Subject: $300k+ Package Job Opportunity
            
            Dear John Doe,
            
            Our company is hiring for a sales position, it's a $300K opportunity.
            
            Ideal candidate must be responsible for:
            1. Resolving sellers issues, questions, concerns with effective, clear and professional written and oral communication.
            2. Building platform and business knowledge to better serve sellers.
            3. Demonstrating excellent time-management skills and the ability to work independently.
            4. Contributing to a positive team environment.
            
            Please fill the attached form. If this offer isn't a good fit for you, feel free to refer a friend! Or someone you know is looking for an exciting new             career opportunity.
            
              Learn more on the attached document.
            
            Thanks!  
              The Human Resources Team
            
            Attachment: CanIPhish-Word-Attachment.docx
            
## Screenshot

![image](https://github.com/user-attachments/assets/fdb1b9a5-8614-4848-ad90-21b857d3efdf)


  

---

### 2. Analyzed Red Flags in the Email

- Found fake domain: `morganstanley-careers.com`
- Used generic/unprofessional tone
- Pushed urgency (“APPLY NOW” in all caps)
- Mentioned fake attachment: `Job_Application_Form.doc`

Details in: `phishing_indicators.md`

## File Contents

     # Phishing Indicators 

This document lists the suspicious traits found in the sample phishing email titled **"$300K+ Package Job Opportunity"**.

---

## 📌 Key Red Flags Identified:

### 1. **Suspicious Sender Domain**
- **From:** talent-acquisition@cloud-notification-services[.]com
- 🚩 This is not related to any real hiring or corporate domain
- ✅ Real HR emails come from company-owned domains

---

### 2. **Personalization Failure**
- Generic greeting: **"Dear John Doe"**
- 🚩 Real job emails use your actual name, and have verified contacts

---

### 3. **Unrealistic Offer**
- "$300K+ for a sales role" with no experience required
- 🚩 Unrealistic compensation is a psychological lure

---

### 4. **Urgency + CTA (Call to Action)**
- Bold phrases like **"fill the attached form"**
- Encourages quick action without thinking
- 🚩 Common tactic in phishing and scam emails

---

### 5. **Suspicious Attachment**
- `CanIPhish-Word-Attachment.docx`
- 🚩 Could contain malware or a malicious macro script

---

### 6. **Overly Polished but Generic Style**
- Tries to look professional but lacks:
  - Signature block
  - Company branding
  - Contact info
- 🚩 Looks fake under close inspection

---

## ✅ Summary:

This email demonstrates multiple phishing characteristics:
- Fake sender domain
- Urgent tone
- Vague & high-paying job offer
- Suspicious attachment

It’s designed to trick users into downloading malware or providing sensitive info. This kind of email should be **flagged and reported immediately**.


---

### 3. Simulated Email Header Analysis

Key red flags:
- Return path mismatch
- IP address not linked to real company
- No DKIM/SPF/DMARC validation
- Missing signature & reply-to info

Details in: `header_analysis.txt`

## File Contents
                             

            ---

## 📁 Files in This Repo

| File Name                 | Description                                               |
|---------------------------|-----------------------------------------------------------|
| `README.md`               | Full explanation of the task and steps                    |
| `phishing_email_sample.txt` | Raw phishing email content                              |
| `phishing_indicators.md` | Listed suspicious traits in the email                     |
| `header_analysis.txt`     | Header spoofing and email source analysis                 |

---

## 🧠 What I Learned

- How phishing emails trick users using urgency & impersonation  
- Common red flags in email headers and body content  
- Importance of domain awareness and proper email formatting  
- Documenting cybersecurity findings professionally

---

