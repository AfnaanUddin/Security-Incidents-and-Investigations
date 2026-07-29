# 🚨 Incident Report: Potentially Unwanted Program (PUP) / Adware Detection

![Severity](https://imgbadge/Severity-Low-green
![Status](https://img.shields.io/badge/Status-Closed[Source](https://img.shields.io/be-CrowdStrike-blue
![Asset](https://img.shields.io/badge/Asset-ange

## Executive Summary

On **June 1 at 08:55 AM**, CrowdStrike generated a security alert indicating that a file had been written to a server's file system. The file was identified as a **Potentially Unwanted Program (PUP) / Adware** based on its SHA256 hash reputation.

The security solution automatically quarantined the file upon detection, preventing execution or further activity. Subsequent reputation analysis confirmed the file was malicious. No signs of additional compromise or suspicious activity were identified on the affected server.

---

## Incident Details

| Field | Value |
|---------|---------|
| **Incident Title** | Potentially Unwanted Program / Adware Detection |
| **Severity** | Low |
| **Alert Source** | CrowdStrike |
| **Affected Asset** | Server |
| **Detection Type** | Adware / Potentially Unwanted Program (PUP) |
| **Status** | Closed |
| **Detection Time** | June 1, 08:55 AM |

---

## Investigation Timeline

### Actions Performed

1. Reviewed the CrowdStrike alert and confirmed the file had been written to the server's file system.
2. Verified that the security solution automatically quarantined the file.
3. Obtained the associated SHA256 hash.
4. Conducted hash reputation analysis using VirusTotal.
5. Confirmed the file was classified as malicious and detected by multiple security vendors.
6. Reviewed host details and validated that no additional suspicious activity was present.

---

## Findings

✅ File identified as **Adware/PUP** through hash reputation analysis.

✅ Security controls successfully **quarantined the file before execution**.

✅ VirusTotal confirmed the file was **malicious** and flagged by multiple vendors.

✅ The affected asset was a **server**.

✅ No evidence of lateral movement, persistence, or additional compromise was identified.

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

A SHA256 reputation check performed through VirusTotal confirmed the file was malicious. Review of the affected host did not reveal any indicators of compromise beyond the isolated file.

No additional remediation actions were required.

---

## Lessons Learned

- Automated detection and quarantine controls functioned as expected.
- Hash reputation analysis remains an effective validation method for suspicious files.
- Continue monitoring for recurring PUP/Adware detections on server assets.
- Maintain regular review of endpoint protection policies to ensure effective containment.

---

## Final Disposition

> **Closed – Threat Contained by Security Controls**

### Conclusion

The alert was determined to be a low-severity Adware/PUP detection. Security controls successfully prevented execution by automatically quarantining the file. Reputation analysis confirmed the file was malicious, and no evidence of system compromise, data exposure, or further malicious activity was identified during the investigation.
