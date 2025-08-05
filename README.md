# Phishing Email Analysis Report

**Date:** August 5, 2025,
**Analyst:** [Mohd Uzair]

**The Following Email is a Sample Of Phishing Email:**

------------------ EMAIL HEADER ------------------

From: "Netflix Support" <support-id8345@updates-netflix.com>
Reply-To: security.claims@aol.com
Date: Tue, 5 Aug 2025 13:15:10 +0530
Subject: Action Required: Your Account is On Hold!
Received: from mail.random-server.bg (185.11.25.33) by mail.google.com with ESMTP

------------------ EMAIL BODY ------------------

Dear Customer,

We have detected a problem with your billing information and your account is now on hold. You need to update you're payment details to avoid account closure.

Failure to update your information within 24 hours will result in permanent suspension of your account. We take your security very seriously and this is a required step.

To fix this, please click the link bellow and sign in to your account:

Update Your Account Here: https://www.netflix.com/your-account

Thank you,
The Netflix Team.

-------------------------------------------------

**SPOILER ALERT / HIDDEN INFO:**
*When you hover your mouse over the link "https://www.netflix.com/your-account", the actual web address it points to is:* `http://netflix-billing-update.io/login`




## 1. Objective

To analyze a sample email for phishing indicators and document the findings to demonstrate an understanding of common phishing tactics.

## 2. Email Details

* **From:** "Netflix Support" <support-id8345@updates-netflix.com>
* **Subject:** Action Required: Your Account is On Hold!

## 3. Analysis of Phishing Indicators

The following indicators confirm that this email is a phishing attempt:

| Indicator Category           | Finding                                                                                                                                              | Risk                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| **1. Sender Address Spoofing** | The sender's email domain is `@updates-netflix.com`, not the official `@netflix.com`.                                                                | High. The sender is impersonating a trusted brand to trick the recipient.                                   |
| **2. Header Discrepancies** | The `Reply-To` address is `security.claims@aol.com`, which is unrelated to Netflix. The email originated from a server in Bulgaria (`.bg`).            | High. This shows the email's true origin is not from Netflix's infrastructure.                                |
| **3. Malicious & Mismatched URL** | The visible link text `www.netflix.com` masks the true destination URL, which is `http://netflix-billing-update.io/login`.                           | Critical. This is the payload of the attack, designed to lead to a credential harvesting website.             |
| **4. Psychological Tactics** | The email creates a false sense of urgency with threats of "permanent suspension" and a "24 hours" deadline.                                         | High. This tactic aims to cause panic and prevent the user from carefully inspecting the email.             |
| **5. Poor Grammar/Spelling** | The email contains errors like "you're" instead of "your" and "bellow" instead of "below". The greeting "Dear Customer" is generic. | Medium. These errors are unprofessional and uncharacteristic of a large corporation like Netflix. |

## 4. Conclusion

The email is definitively a phishing attack. It uses a combination of technical spoofing (sender address, malicious link) and psychological manipulation (urgency, threats) to deceive the recipient into revealing their Netflix login credentials on a fraudulent website.
