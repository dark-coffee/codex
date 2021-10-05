# Windows 11

## Installing

To install on a non-supported system:

1. Create USB installation media using the creation tool, and boot to the drive.
2. Once the installation wizard has loaded, hit `SHIFT + F10` to launch the command prompt.
3. Launch `regedit`
4. Inside the registry editor, navigate to `HKLM/Setup`.
5. Create a new key named `LabConfig`
6. Within the newly created key, create three DWORD entries:

| Entry Name       | Value |
|------------------|-------|
| `BypassCPUCheck` | 1     |
| `BypassRAMCheck` | 1     |
| `BypassTPMCheck` | 1     |

7. Exit regedit and CMD, then proceed with the installation.
