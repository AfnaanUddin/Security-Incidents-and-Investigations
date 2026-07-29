#Incident Title: Potentially Unwanted Program / Adware Detection

##Severity: Low
Alert Source: CrowdStrike
Affected Asset: Server
Detection Type: Adware / PUP
File Status: Quarantined
Affected IP: 10.165.254.200

##Investigation steps:
1. Reviewed the security alert and confirmed the file had been written to the server's file system.
2. Verified that the security tool had automatically quarantined the file.
3. Obtained the SHA256 hash associated with the detected file.
4. Performed reputation analysis using VirusTotal.
5. Confirmed that VirusTotal classified the file as malicious and detected by multiple security vendors.
6. Reviewed the host information and verified that no additional suspicious activity was immediately apparent.

##Findings
•	The file was identified as Adware/PUP based on hash reputation.
•	The file was successfully quarantined before execution or further impact was observed.
•	VirusTotal analysis indicated the file was malicious.
•	The affected asset was a server.
•	No evidence of additional compromise was identified during the investigation.

##Impact Assessment
•	Impact Level: Low
•	Data Exposure: No evidence observed.
•	System Compromise: No evidence observed.
•	Business Impact: Minimal, as the file was automatically quarantined.


##Resolution
The file was successfully quarantined by the security solution. The SHA256 hash was verified as malicious through Virus Total analysis. No further action was required at this time, and the incident was closed as contained.
Lessons Learned
•	Automated detection and quarantine controls functioned as expected.
•	Hash reputation checks remain an effective method for validating suspicious files.
•	Continue monitoring for similar detections on server assets.

##Final Disposition
Closed – Threat Contained by Security Controls.

##Summary: A security alert was generated at 8:55 AM on June 1 indicating that a file had been written on the file system on a server. The file was classified as a Potentially Unwanted Program (PUP)/Adware based on its SHA256 hash. The security solution successfully quarantined the file upon detection.
