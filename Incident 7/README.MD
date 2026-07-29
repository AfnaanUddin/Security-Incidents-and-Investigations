Incident Report: Discord.exe Detection via Custom IOA Policy

## Executive Summary

A CrowdStrike Falcon alert was generated following the execution of **Discord.exe** on a Windows endpoint. The detection was triggered by a **Custom Indicator of Attack (IOA)** rule designed to block the use of Discord within the environment due to organizational policy restrictions.

Investigation confirmed that the application was installed through a legitimate software installation process using **winget** and that the detected executable was a valid Discord installation. No malicious activity, persistence mechanisms, or compromise indicators were identified. The detection correctly identified a policy violation, and the application was blocked in accordance with organizational security requirements.

---

## Incident Details

| Field | Value |
|---------|---------|
| **Incident Title** | Discord.exe |
| **Severity** | Medium |
| **Alert Source** | CrowdStrike Falcon |
| **Detection Type** | Custom Intelligence via Indicator of Attack (IOA) |
| **Affected Asset** | Windows Endpoint |
| **Status** | Closed |

---

## Key Artifacts

| Artifact | Value |
|-----------|-----------|
| **File Name** | Discord.exe |
| **SHA256 Hash** | 3e43ea0c286ef660dfeb2f76b51c4f22462e1752595256387d3cf736f68ca341 |
| **File Path** | `\Device\HarddiskVolume3\Users\ToorA\AppData\Local\Discord\app-1.0.9242\Discord.exe` |
| **Command Line** | `"C:\Users\ToorA\AppData\Local\Discord\app-1.0.9242\Discord.exe" --squirrel-firstrun` |

---

## Investigation Timeline

### Actions Performed

1. Reviewed CrowdStrike detection details and associated process tree.
2. Identified the detection as a Custom IOA alert.
3. Analyzed the process execution chain associated with the Discord installation.
4. Reviewed command-line arguments associated with application execution.
5. Validated file reputation through VirusTotal.
6. Assessed execution activity against organizational security policies.
7. Reviewed endpoint activity for evidence of suspicious behavior beyond the detected application.
8. Confirmed the alert aligned with the intended purpose of the custom detection rule.

---

## Evidence Reviewed

- CrowdStrike Detection Details
- CrowdStrike Process Tree
- Endpoint Process Activity
- VirusTotal Hash Reputation Analysis
- Custom IOA Rule Metadata
- Installation and Execution Logs

---

## Findings

✅ User initiated the installation of Discord using **winget**.

✅ Execution chain observed:

```text
winget.exe
    ↓
DiscordSetup.exe
    ↓
Update.exe
    ↓
Discord.exe --squirrel-firstrun
```

✅ Command-line parameter `--squirrel-firstrun` is consistent with normal Discord installation and first-run execution behavior.

✅ VirusTotal reputation analysis did not identify the executable as malicious.

✅ Detection was triggered by the CrowdStrike custom IOA rule **"Blocking Discord.exe (v2)"**.

✅ Discord is prohibited under organizational security policy and subject to automated blocking controls.

✅ No suspicious child processes, persistence mechanisms, privilege escalation attempts, or malicious activity were identified.

✅ Activity was determined to be legitimate software installation behavior that violated organizational software usage policy.

---

## Verdict

| Category | Assessment |
|-----------|-----------|
| **Classification** | True Positive |
| **Confidence Level** | High |
| **Threat Status** | Policy Violation Confirmed |

---

## Impact Assessment

| Category | Assessment |
|-----------|-----------|
| **Impact Level** | Low |
| **Data Exposure** | Not observed |
| **System Compromise** | Not confirmed |
| **Business Impact** | Low |
| **Containment Status** | Application Blocked |

### Justification

The Discord executable was determined to be a legitimate application and not malware. However, the software is prohibited by organizational policy and was correctly identified by the custom CrowdStrike IOA control. No evidence of compromise, unauthorized access, or malicious execution was observed during the investigation.

---

## Resolution

The alert was investigated using CrowdStrike telemetry, process execution logs, command-line analysis, and reputation validation.

Analysis confirmed that Discord was installed through a legitimate installation workflow and executed using expected first-run parameters. No security threat beyond the policy violation was identified.

In accordance with organizational policy, the application was blocked and/or quarantined through security controls. No additional remediation actions were required.

---

## Lessons Learned

- Custom IOA rules are effective for enforcing organizational software restrictions.
- Legitimate applications can generate security alerts when they violate internal policy requirements.
- Process tree analysis provides valuable context for differentiating legitimate software installation from malicious activity.
- Software installation activity should be validated against approved application inventories.
- Endpoint controls should continue monitoring for unauthorized communication and collaboration tools.
- Maintaining clear software usage policies reduces risk and improves consistency in incident handling.

---

## Final Disposition

> **Closed – True Positive (Unauthorized Software Detected and Blocked)**

### Conclusion

The detection successfully identified an unauthorized application that violated organizational software policy. Although Discord itself was determined to be legitimate and non-malicious, its execution represented a policy compliance issue requiring enforcement action. Security controls functioned as intended, the application was blocked, and no further risk to the environment was identified. The incident was therefore classified as a **True Positive** and closed.
