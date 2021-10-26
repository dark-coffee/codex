# Amazon Web Services

## PowerShell CLI Tools

### Installing

AWS have created a tools management utility, **AWS.Tools.Installer**, which allows you to Install, Update, and Manage the subsets of AWS tools. Any of the tools you can install using the installer, can also be installed from the PowerShell gallery using the tool name, in the format AWS.Tools.[name].

To install the AWS PowerShell CLI Tools Installer:

```powershell
Install-Module AWS.Tools.Installer
```

To install the common toolset:

```powershell-interactive
Install-AWSToolsModule Common
```

To install the S3 toolset:

```powershell
Install-AWSToolsModule S3
```

### Configuring a Profile

To store credentials for later use, you can setup a profile. To use the profile in another command, call the `-ProfileName` paremeter, and supply the **friendly name** of your profile.

```powershell
Set-AWSCredential `
    -AccessKey [access key]
    -SecretKey [secret access key]
    -StoreAs [friendly name]
```
