
# Windows Event Log Analysis

## Project Overview

This project documents a practical investigation using Windows Event Viewer and Microsoft Windows Security on a Windows 11 computer.

The objective is to practise identifying system events, interpreting error messages cautiously, reviewing security alerts, recording troubleshooting actions, and verifying outcomes using available evidence.

## Objectives

- Review a Windows system error in Event Viewer.
- Investigate a Windows Update installation failure.
- Review a Microsoft Defender security detection and its remediation status.
- Record antivirus scan results and current protection status.
- Document findings, limitations, and recommended next steps.

## Tools Used

- Windows Event Viewer
- Windows Update
- Windows Security
- Microsoft Defender Antivirus
- Windows 11

## Summary of Findings

### 1. Windows Update Installation Failure

A System log event from `WindowsUpdateClient`, Event ID `20`, recorded a failure to install a Microsoft Defender security intelligence update.

- Error code: `0x80240016`
- Affected update: `KB2267602`
- Initial interpretation: Another update or servicing operation may have prevented installation.
- Follow-up observation: Windows Update later displayed **"You're up to date."**
- Limitation: This does not independently confirm that the exact update mentioned in the original event installed successfully.

### 2. Microsoft Defender Security Detection

Windows Security detected an item identified as `Tool:AndroidOS/Multiverze` associated with a downloaded ZIP file.

- Initial status: Remediation incomplete in an older Protection history entry.
- Subsequent status: Threat removed.
- Follow-up quick scan: Zero threats found.
- Follow-up full scan: Zero threats found across 945,947 scanned files.
- Latest reported status: No current threats.

The detection and removal are documented as Windows Security findings. The detection name alone does not establish whether the original file was malicious or a false positive.

## Investigation Approach

The investigation followed a cautious troubleshooting process:

1. Collect information from Windows Event Viewer and Windows Security.
2. Record the exact event identifiers, error codes, and displayed statuses.
3. Review relevant security history.
4. Follow the available protective remediation action.
5. Run antivirus scans and review their results.
6. Recheck Windows Update and document the observed status.
7. Distinguish confirmed findings from possible explanations.

## Limitations

- A historical error event does not necessarily indicate a current problem.
- A successful scan reporting zero threats does not guarantee that every possible security issue has been ruled out.
- A current Windows Update status of "You're up to date" does not independently verify the outcome of every previously failed update.
- No root cause is claimed where the available evidence is insufficient.

## Learning Outcomes

This project demonstrates practical experience with:

- Windows system log investigation
- Basic Windows Update troubleshooting
- Antivirus alert review and remediation verification
- Evidence-based technical documentation
- Careful interpretation of error messages
- Recording limitations and follow-up actions

## Project Status

Investigation findings documented; final report review and GitHub publication pending.
