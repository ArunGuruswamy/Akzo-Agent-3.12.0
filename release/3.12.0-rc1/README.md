# Akzo Master SDD Agent 3.12.0 release candidate (proposed)

Akzo SDD Agent â€” Developed and maintained by Arun RG

| File | What it is |
|---|---|
| `Akzo-Agent-3.12.0.zip` | The package: the same 58 files as the source at tag `v3.12.0-rc1` (checked file by file against the tag), plus `release-manifest.json` (SHA-256 of every file). `install.ps1` refuses a package whose files differ or whose manifest names another version. |
| `Akzo-Agent-3.12.0.zip.sha256` | Checksum of the zip |

SHA-256 of the zip: `002B28B059676DE490EBCA24C32411EC2B894A22DFCCC7DE59F92E65F97960C0`

Check it with `Get-FileHash Akzo-Agent-3.12.0.zip -Algorithm SHA256`. A hash shows the file is unchanged since it was built, not who built or approved it.

What changed: verified PR review comments become lessons (`lesson -Action add`), stored per repository in `%USERPROFILE%\.akzo-agent\learning\`. Equivalent comments group into one lesson; unverified, instruction-like, business-specific, and contradicting feedback is never promoted. After the developer approves a lesson once, `task` lists it for every new plan and `review` reports a repeat of the mistake as an error naming the existing component. `trace` reports whether test results are older than the code and a readiness per acceptance criterion; stale results never verify a change. Built on 3.11.0. See `CHANGELOG.md`.

Validation: 397 regression checks and 14 window checks passed (run from Windows PowerShell), including an end-to-end test in which a duplicate validation service caught in one PR review is prevented in the next PBI. The zip installed into an empty profile and verified (version 3.12.0 everywhere); an install made from the 3.11.0 zip upgraded and verified with task files, lessons, and custom review rules unchanged.

Status: proposed release candidate. Corporate readiness is NOT VERIFIED; see `corporate-security-report.html`. Live Copilot behavior and lessons from real DAB, CDMS, and Angular PR reviews are NOT VERIFIED (not available on this machine).