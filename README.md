SOC257 - VPN Connection Detected from Unauthorized Country
Severity	Low
Type	Unauthorized Access
Difficulty	Easy
Playbook	Incident Responder
MITRE Techniques	T1595, T1133, T1621
SOC Alert Details
URL	https://vpn-letsdefend.io
Username	monica@letsdefend.io
Source Address	113.161.158.12
Destination Address	33.33.33.33
Alert Trigger Reason	Vpn Connection Detected from Unauthorized Country
Destination Hostname	Monica
Playbook Answers
Connect Machine
Your answer: Next

Verify
Your answer: Next

Determine whether alert was TP or FP
Your answer: True Positive

TP. Firewall log detail at 02:01 shows "Incorrect OTP Code" as the action. It is understood that the attacker Monica entered her password correctly and OTP (One time password) was sent. However, it is thought that the attacker could not access the medium (mail or sms) where the OTP was sent. If he could have accessed the OTP in the relevant medium, he would have successfully logged in to the VPN. Subsequent logs showed that the attacker tried again one minute apart. Similarly, the OTP was entered incorrectly in both logs. Therefore alert is True Positive for VPN connection. However, if alert name was VPN login, it would be False Positive.

Choose Incident Type
Your answer: Malware · Correct answer: Unauthorized Access

Unauthorized Access.A request from the user "Monica@letsdefend.io" to the address "https://vpn-letsdefend.io" from the IP 113.161.158.12 located in Vietnam at 02:01:01 AM was received with http response code 200 (success).

Does the device need to be isolated?
Your answer: Yes · Correct answer: No

No. Although the attacker cannot bypass the MFA structure in the VPN, Monica can be called a Compromised Account because she entered the password correctly. Since the attacker cannot access the system, it does not need to be isolated.

Backup evidences
Your answer: Next

Eradication
Your answer: Next

Recovery
Your answer: Next

Lesson Learned
Your answer: Next

Result
Is this alert True Positive or False Positive?
Your answer: True Positive

Artifacts
Type	Value	Comment
URL Address	wmic memorychip get capacity	a schedule task to check the if it is the vm machine or host
IP Address	113.161.158.12	VietNam Post and Telecom Corporation (VNPT
Analyst Note
URL :
https://vpn-letsdefend.io
Username :
monica@letsdefend.io
Source Address :
113.161.158.12
Destination Address :
33.33.33.33
Alert Trigger Reason :
Vpn Connection Detected from Unauthorized Country
Destination Hostname :
Monica

Upon checking the IP address, we could find the IP was being connected from Vietnam and its malicious, the Ip got unauthorized access to the user - Monica's account and there was an attempt to know the computer details, we couldn't see any file being executed, so this was a possible failed attack and the user has been contained
