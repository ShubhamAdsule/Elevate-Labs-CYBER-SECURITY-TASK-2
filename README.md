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
                                     # Header Analysis 
                        
                        Note: This file focuses on **technical red flags found in the email header**.  
                        For social engineering and content-based indicators, refer to `phishing_indicators.md`.
                        
                        ---
                        
                        📧 Sample Header (Simulated from the phishing email):
                        
                        From: Talent Acquisition <talent-acquisition@cloud-notification-services[.]com>  
                        Return-Path: hr-hiring@freelance-careers.biz  
                        Received: from 45.67.89.101 (unknown relay server)  
                        To: john.doe@mybusiness.com  
                        Subject: $300k+ Package Job Opportunity  
                        Date: Tue, 15 Mar 2025 09:44:02 +0000
                        
                        ---
                        
                        ## 🔍 Technical Red Flags Identified:
                        
                        ### 1. **Mismatch Between Displayed Sender and Return-Path**
                        - Displayed sender: `cloud-notification-services[.]com`
                        - Return path: `freelance-careers.biz`
                        - 🚩 This suggests spoofing or third-party relay usage
                        
                        ---
                        
                        ### 2. **Suspicious IP Address**
                        - IP `45.67.89.101` is tied to an unknown or shady server
                        - 🚩 Not associated with any reputable company or email service
                        
                        ---
                        
                        ### 3. **Missing SPF, DKIM, or DMARC Headers**
                        - No records to verify sender authenticity
                        - 🚩 These are normally used to protect against spoofing
                        
                        ---
                        
                        ### 4. **Generic Recipient Field**
                        - Sent to: `john.doe@mybusiness.com`
                        - 🚩 Could be scraped, guessed, or sent as part of a mass-targeted spam campaign
                        
                        ---
                        
                        ### 5. **Lack of Signature/Authentication Metadata**
                        - No "signed-by", "mailed-by", or secure sender identity
                        - 🚩 Indicates that the email likely bypassed basic verification checks
                        
                        ---
                        
                        ✅ **Conclusion:**
                        
                        The email header contains clear signs of manipulation and impersonation.  
                        The mismatch of domains, suspicious server origin, and missing authentication protocols strongly indicate a phishing attempt.

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

