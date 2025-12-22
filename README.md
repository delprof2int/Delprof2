# Delprof2 v1.6.0

Download latest version from Releases:       
https://github.com/delprofx/Delprof2/releases/tag/v1.6.0

## Introduction

Delprof2 is a lightweight command-line utility for safely removing local Windows user profiles in enterprise, classroom, and lab environments. Unlike “delete the folder” approaches, it removes both the profile directory under \Users and the related registry data (ProfileList entries), reducing orphaned SIDs, broken logons, and wasted disk space on shared endpoints, RDS hosts, and VDI pools.

Built for advanced operators, Delprof2 supports precise targeting and automation. You can purge profiles based on age or last-use thresholds, exclude critical accounts (e.g., administrator, default, service identities), and apply include/exclude name patterns to protect VIP or break-glass profiles. A dry-run style preview plus verbose logging makes it suitable for change-controlled maintenance windows and for integration into PowerShell, scheduled tasks, SCCM/Intune packages, or GPO startup scripts.

Delprof2 is commonly used to reclaim storage, reduce profile bloat, and keep “golden” images clean between sessions. It also complements roaming profiles and folder redirection scenarios where local caches should be periodically reset to eliminate corruption and configuration drift.

Operationally, the tool is designed to handle edge cases such as missing profile paths, stale registry references, and permissions constraints, while minimizing risk: it can detect and skip currently loaded profiles and, when necessary, schedule cleanup actions to complete after reboot. For repeatable operations, it offers consistent exit codes and structured output that can be parsed by monitoring and job-control systems.
