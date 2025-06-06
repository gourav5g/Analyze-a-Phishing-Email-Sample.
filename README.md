# Analyze-a-Phishing-Email-Sample.
Creating a Phishing Email

---

# 🛡️ Phishing Email Analysis Report

This report presents the findings from analyzing a suspicious email to identify potential phishing characteristics. The goal is to detect red flags such as spoofed sender addresses, malicious links, forged headers, and other common phishing tactics.

---

## 🔍 1. Sample Phishing Email Overview

- **Subject Line**: *"Your account has been suspended – Immediate Action Required"*
- **Displayed Sender**: `support@paypal.com`
- **Email Body Snippet**:
  > "Dear Valued Customer,  
  > We have detected suspicious activity on your account. Your access has been temporarily suspended until further verification. Please click the link below to confirm your identity and reactivate your account."

---

## 🧪 2. Phishing Indicators Identified

### 📨 2.1. Spoofed Sender Address
- **Actual Email Address**: `support@paypa1.com` *(Note: '1' used instead of 'l')*
- **Finding**: ⚠️ This is a classic example of **email spoofing**, where attackers mimic legitimate company domains to trick users.

---

### 📋 2.2. Email Header Analysis
- **Tool Used**: [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeader.aspx)
- **Key Findings**:
  - Originating IP address: `192.0.2.1` (a test range, not real)
  - Return-path does **not match** the sender domain
  - No traceable path to PayPal’s actual servers
- **Finding**: ⚠️ **Headers are inconsistent or forged**, indicating a high likelihood of phishing.

---

### 🔗 2.3. Suspicious Links
- **Link Text**: "Click here to verify your account"
- **URL**: `http://verify-account-paypal.com/recover`
- **Finding**: ⚠️ The link leads to an **unrelated third-party website** not affiliated with PayPal.

---

### ⏳ 2.4. Urgent or Threatening Language
- **Examples**:
  - "Immediate action required"
  - "Account suspended due to suspicious activity"
  - "Failure to respond within 24 hours will result in permanent deactivation"
- **Finding**: ⚠️ These are **classic fear-based tactics** used to pressure recipients into acting quickly without thinking.

---

### 🖱️ 2.5. URL Mismatches
- **Hover Text**: `http://verify-account-paypal.com/recover`
- **Actual Destination**: Same as above (does not lead to official PayPal domain)
- **Finding**: ⚠️ **Mismatched or misleading URLs** are a strong indicator of phishing.

---

### ✍️ 2.6. Spelling and Grammar Errors
- **Error Found**:
  - "Please click here to verify your account immediatly."
    - Misspelled word: *immediatly* (should be "immediately")
- **Other Issues**:
  - Awkward sentence structure and unnatural tone
- **Finding**: ⚠️ Poor grammar and spelling mistakes are often seen in phishing emails.

---

## 📊 3. Summary Table of Phishing Traits

| Indicator | Observed? | Notes |
|----------|------------|-------|
| Spoofed sender | ✅ Yes | Uses `paypa1.com` instead of `paypal.com` |
| Header discrepancies | ✅ Yes | Forged return path and fake IP address |
| Suspicious links | ✅ Yes | Leads to non-PayPal domain |
| Threatening language | ✅ Yes | Uses urgency and fear to prompt action |
| URL mismatch | ✅ Yes | Link text vs actual destination don't match |
| Spelling/grammar errors | ✅ Yes | Includes misspellings and awkward phrasing |
| Attachments | ❌ No | No attachments found |

---

## 🧠 4. Conclusion

This email demonstrates **multiple signs of a phishing attempt**, including a spoofed sender, suspicious links, forged headers, and urgent language designed to manipulate the recipient. Users should be advised:

- **Never click on unknown links**
- Always **verify the sender's legitimacy**
- Use **official websites or apps** for account-related actions
- **Report suspicious emails** to IT or security teams

---

## 🛠️ Tools Used

- [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeader.aspx)

---
