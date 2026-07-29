Incident Report: Malware via PUP Detection

## Executive Summary

On **June 5 at 17:59**, CrowdStrike generated a security alert indicating that a file had been written to a Windows 11 workstation's file system. The file was identified as **Malware / Potentially Unwanted Program (PUP)** based on its SHA256 hash reputation.

The security solution automatically quarantined the file upon detection, preventing execution or further activity. Subsequent reputation analysis confirmed the file was malicious. No signs of additional compromise or suspicious activity were identified on the affected workstation.

---

## Incident Details

| Field | Value |
|---------|---------|
| **Incident Title** | Malware via PUP |
| **Severity** | Low |
| **Alert Source** | CrowdStrike |
| **Affected Asset** | Windows 11 Workstation |
| **Detection Type** | Malware / PUP |
| **File Status** | Quarantined |
| **Detection Time** | June 5, 17:59 |

---

## Investigation Timeline

### Actions Performed

1. Reviewed the CrowdStrike alert and confirmed the file had been written to the host's file system.
2. Verified that the security solution automatically quarantined the file.
3. Obtained the associated SHA256 hash.
4. Conducted hash reputation analysis using VirusTotal.
5. Confirmed the file was classified as malicious and detected by multiple security vendors.
6. Reviewed host details and validated that no additional suspicious activity was present.

---

## Findings

✅ File identified as **Malware/PUP** through hash reputation analysis.

✅ Security controls successfully **quarantined the file before execution**.

✅ VirusTotal confirmed the file was **malicious** and flagged by multiple vendors.

✅ The affected asset was a **Windows 11 endpoint workstation**.

✅ No evidence of persistence, privilege escalation, lateral movement, or additional compromise was identified.

---

## Impact Assessment

| Category | Assessment |
|-----------|-----------|
| **Impact Level** | Low |
| **Data Exposure** | No evidence observed |
| **System Compromise** | No evidence observed |
| **Business Impact** | Minimal |
| **Containment Status** | Successfully Contained |

---

## Resolution

The detected file was automatically quarantined by CrowdStrike upon identification.

A SHA256 reputation check performed through VirusTotal confirmed the file was malicious. Review of the affected endpoint did not reveal any indicators of compromise beyond the isolated file.

No additional remediation actions were required.

---

## Lessons Learned

- Automated detection and quarantine controls functioned as expected.
- Hash reputation analysis remains an effective validation method for suspicious files.
- Continue monitoring for recurring Malware/PUP detections on endpoint devices.
- Maintain regular review of endpoint protection policies to ensure effective containment.

---

## Final Disposition

> **Closed – Threat Contained by Security Controls**

### Conclusion

The alert was determined to be a low-severity Malware/PUP detection. Security controls successfully prevented execution by automatically quarantining the file. Reputation analysis confirmed the file was malicious, and no evidence of system compromise, data exposure, or further malicious activity was identified during the investigation.
