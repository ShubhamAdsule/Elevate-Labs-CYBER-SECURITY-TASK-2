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
      From: Morgan Stanley Careers <careers@morganstanley-careers.com>
      To: you@example.com
      Subject: Job Opportunity - Work From Home
      
      Hello,
      
      Morgan Stanley is hiring remote positions! We are seeking part-time assistants to work from home with flexible hours and excellent compensation.
      
      No prior experience is required. Simply fill out the attached form and submit it to get started.
      
      APPLY NOW: http://morganstanley-careers.com/application
      
      Best regards,  
      Morgan Stanley HR Team
      
      Attachment: Job_Application_Form.doc
   

---

### 2. Analyzed Red Flags in the Email

- Found fake domain: `morganstanley-careers.com`
- Used generic/unprofessional tone
- Pushed urgency (“APPLY NOW” in all caps)
- Mentioned fake attachment: `Job_Application_Form.doc`

Details in: `phishing_indicators.md`

## File Contents

      # Phishing Indicators 
      
      This document lists the suspicious traits found in the sample phishing email titled "Job Opportunity – Work From Home".
      
      ---
      
      ## 📌 Key Red Flags Identified:
      
      ### 1. **Suspicious Sender Domain**
      - **From:** careers@morganstanley-careers.com
      - ✅ *Morgan Stanley's official domain is* `morganstanley.com`
      - 🚩 Use of lookalike domain is a classic phishing trick
      
      ---
      
      ### 2. **Incorrect Grammar**
      - **"Morgan Stanley is hiring remote positions"**
      - 🔁 Should be: "Morgan Stanley is hiring for remote positions"
      - 🧠 Small but unprofessional — often a red flag
      
      ---
      
      ### 3. **Overly Generic & Vague Content**
      - No job title, department, or contact information
      - Lacks proper email signature or company formatting
      
      ---
      
      ### 4. **Aggressive Call to Action**
      - “APPLY NOW” in ALL CAPS
      - Links to a suspicious domain: `http://morganstanley-careers.com/application`
      - ✅ Hovering over the link would show a mismatch (typical in phishing)
      
      ---
      
      ### 5. **Fake Attachment**
      - Mentions an attached file: `Job_Application_Form.doc`
      - Could contain malware or be used for credential harvesting
      
      ---
      
      ## ✅ Summary:
      
      This email is a clear phishing attempt. It uses urgency, fake branding, poor grammar, suspicious links, and a generic tone to trick users into engaging with malicious content.


---

### 3. Simulated Email Header Analysis

Key red flags:
- Return path mismatch
- IP address not linked to real company
- No DKIM/SPF/DMARC validation
- Missing signature & reply-to info

Details in: `header_analysis.txt`

## File Contents
              Header Analysis 
            
            This analysis highlights red flags from the sample email headers used in the phishing message.
            
            ---
            
            📧 Sample Header (Extracted):
            
            From: Morgan Stanley Careers <careers@morganstanley-careers.com>  
            Return-Path: scammer@cheap-fakejobs.com  
            Received: from 185.250.54.29 (unknown host, suspicious IP range)  
            Subject: Job Opportunity – Work From Home  
            To: you@example.com  
            Date: [legitimate-looking date]
            
            ---
            
            🔍 Header Red Flags:
            
            1.  Return-Path Mismatch
               - Email says it's from `morganstanley-careers.com`
               - But the return path shows: `scammer@cheap-fakejobs.com`
               - 🚩 This indicates spoofing or bounce-back redirection
            
            2.  Suspicious IP Address
               - The sending server: `185.250.54.29`
               - Whois lookup shows it’s not tied to Morgan Stanley or any legit provider
            
            3.  Lack of DKIM/SPF Verification
               - In real email headers, you'd see SPF/DKIM/DMARC pass or fail status
               - In phishing emails, this often fails or is missing completely
            
            4.   Generic “To” Field
               - Sent to: `you@example.com` or `Undisclosed Recipients`
               - No personalized greeting, which real companies use
            
            5.   No Reply-To or Signed-By
               - Missing metadata that most legit corporate emails include
            
            ---
            
            ✅ Conclusion:
            
            This header contains clear spoofing signals and weak authentication. Combined with domain mismatches and shady IPs, it’s a textbook phishing email.
            
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

