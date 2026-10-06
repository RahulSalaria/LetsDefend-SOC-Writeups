# LetsDefend-SOC-Writeups
Case studies and incident response walkthroughs from LetsDefend platform investigations
SOC282 - Phishing Alert - Deceptive Mail Detected
Severity	Medium
Type	Exchange
Difficulty	Medium
Playbook	Phishing Playbook - Security Analyst
MITRE Techniques	T1566, T1566.002, T1059, T1204
⭐ This alert is prepared for the ‘How to Investigate a SIEM Alert’ course. If you haven’t taken the course yet, please complete it first.

SOC Alert Details
SMTP Address	103.80.134.63
Device Action	Allowed
E-mail Subject	Free Coffee Voucher
Source Address	free@coffeeshooop.com
Destination Address	Felix@letsdefend.io
Playbook Answers
Parse Email
Your answer: Next

Are there attachments or URLs in the email?
Your answer: Yes

Upon examining the email on the email security tab, it can be observed that there is a hyperlink attached to the text within the email. <br> https://files-ld.s3.us-east-2.amazonaws[.]com/free-coffee.zip

Analyze Url/Attachment
Your answer: Malicious

After analyzing the file on TI platforms such as anyrun or VirusTotal, it has been determined that the attachment is malicious. <br> Free_coffee[.]zip

Check If Mail Delivered to User?
Your answer: Delivered

Based on the device action in the alert details, the email was allowed and delivered to the user. The malicious email contains a suspicious URL.

Delete Email From Recipient!
Your answer: Delete

Check If Someone Opened the Malicios File/URL?
Your answer: Not Opened · Correct answer: Opened

On the log management and processes tab, it can be seen that Felix’s host accessed the malicious URL, downloaded the malware, and executed it.

Result
Is this alert True Positive or False Positive?
Your answer: True Positive

Analyst Note
From:
free@coffeeshooop.com
To:
Felix@letsdefend.io
Subject:
Free Coffee Voucher
Sender IP:
103.80.134.63
Date:
2024-05-13 11:52:00

The mail was sent From:
free@coffeeshooop.com to To:
Felix@letsdefend.io, Upon checking the reputation of the email , it has dns,spf, dkim failed. The mentioned ip -103.80.134.63 was also flagged, upon checking the logs at 2024-05-13 11:52:00, we could only see the mail had come at what particular point , but the malicious file wasnt opened at all , so this is a potentional phishing attack 
