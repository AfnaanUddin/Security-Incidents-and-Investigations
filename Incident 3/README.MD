Incident Report: Microsoft Defender ATP Detected 'Trojan:Script/Wacatac.C!ml' Malware

## Executive Summary

On **May 19**, Microsoft Defender ATP generated a security alert that was forwarded to Rapid7, indicating the presence of a malicious APK file on an Android mobile device. The threat was identified as **Trojan:Script/Wacatac.C!ml** and classified as malware based on its SHA256 hash reputation.

Investigation confirmed the file was malicious through VirusTotal analysis. The user was contacted to validate activity related to the file and was instructed to remove it from the device. Follow-up scanning did not identify any active threats, and no evidence of additional affected devices was discovered.

---

## Incident Details

| Field | Value |
|---------|---------|
| **Incident Title** | Microsoft Defender ATP detected 'Trojan:Script/Wacatac.C!ml' malware |
| **Severity** | Medium |
| **Alert Source** | Microsoft Defender ATP → Rapid7 |
| **Affected Asset** | Android Mobile Device |
| **Detection Type** | Malware |
| **File Status** | Deleted |
| **Detection Date** | May 19 |

---

## Investigation Timeline

### Actions Performed

1. Reviewed the alert to understand the threat classification, source, and associated indicators.
2. Gathered information related to the affected asset, including device details, IP address, associated user, and file hash.
3. Obtained the SHA256 hash associated with the detected file.
4. Conducted hash reputation analysis using VirusTotal.
5. Confirmed the file was classified as malicious and detected by multiple security vendors.
6. Contacted the user to determine whether the file had been downloaded, installed, or executed.
7. Performed an additional Microsoft Defender scan to validate whether the threat remained present on the device.
8. Instructed the user to remove the malicious file from the Android device.

---

## Findings

✅ Malware detected on an **Android mobile device** through Microsoft Defender ATP.

✅ SHA256 hash reputation analysis confirmed the file was **malicious** and detected by multiple security vendors.

✅ The file was located within an **APK package directory**, indicating association with a third-party Android application.

✅ No process execution data or network telemetry was available within the scope of the investigation.

✅ No additional affected endpoints or related malware detections were identified.

---

## Impact Assessment

| Category | Assessment |
|-----------|-----------|
| **Impact Level** | Medium |
| **Execution Status** | Not Confirmed |
| **Data Exposure** | No evidence observed in available logs |
| **System Compromise** | Not confirmed due to limited telemetry |
| **Business Impact** | Low to Moderate |
| **Containment Status** | Successfully Contained |

---

## Resolution

The malicious APK file was removed from the Android device through user action following security guidance.

The SHA256 hash was validated through VirusTotal and confirmed as malicious. A follow-up scan using Microsoft Defender did not identify any remaining threats on the device.

The file hash should be considered for blocking within the environment, and mobile security controls should continue monitoring for similar detections.

---

## Lessons Learned

- User-installed applications remain a common source of malware infections on mobile devices.
- Hash reputation analysis continues to be an effective method for validating suspicious files.
- User engagement is critical when responding to threats on personal or mobile endpoints.
- Mobile devices should be continuously monitored through MDM and EDR solutions where available.
- Consider implementing additional controls to restrict installation of unapproved applications.

---

## Final Disposition

> **Closed – Threat Contained**

### Conclusion

A Microsoft Defender ATP alert identified a malicious APK file on an Android mobile device. Investigation confirmed the file was malicious through VirusTotal reputation analysis. The user was contacted, the file was removed from the device, and subsequent scanning did not reveal any active threats. Due to limited mobile telemetry, execution and compromise could not be conclusively verified; however, no evidence of additional malicious activity was observed during the investigation. The incident was successfully contained and closed.
