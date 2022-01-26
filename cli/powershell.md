# PowerShell

## Troubleshooting With PowerShell

### Testing SMTP Email Functionality

```PowerShell
Send-MailMessage -To 'user.name@provider.com' -From 'user.name@provider.com' -SMTPServer 'fully.qualified.domain.name' -Subject 'test' -Body 'test' -useSSL -Credential $(Get-Credential)
```  
^ `-useSSL` is required if email transport requires STARTTLS  
^ `-Credential` is required if email transport requires credentials. $(Get-Credential) will prompt for credentials

---

## AWS Commandline Tools

* [AWS Commandline Tools](aws/readme.md)

## Syncing a Remote Profile

## Customisation

* [oh my posh](https://ohmyposh.dev)

## Links

* [PowerShell Gallery](https://www.powershellgallery.com) - the PowerShell module Repository
* [Windows Terminal](https://github.com/microsoft/terminal)

## List of Accepted Verbs

### Common Verbs

| Verb        | Group          |
|-------------|----------------|
| Add         | Common         |
| Clear       | Common         |
| Close       | Common         |
| Copy        | Common         |
| Enter       | Common         |
| Exit        | Common         |
| Find        | Common         |
| Format      | Common         |
| Get         | Common         |
| Hide        | Common         |
| Join        | Common         |
| Lock        | Common         |
| Move        | Common         |
| New         | Common         |
| Open        | Common         |
| Optimize    | Common         |
| Pop         | Common         |
| Push        | Common         |
| Redo        | Common         |
| Remove      | Common         |
| Rename      | Common         |
| Reset       | Common         |
| Resize      | Common         |
| Search      | Common         |
| Select      | Common         |
| Set         | Common         |
| Show        | Common         |
| Skip        | Common         |
| Split       | Common         |
| Step        | Common         |
| Switch      | Common         |
| Undo        | Common         |
| Unlock      | Common         |
| Watch       | Common         |

### Data Verbs

| Verb        | Group          |
|-------------|----------------|
| Backup      | Data           |
| Checkpoint  | Data           |
| Compare     | Data           |
| Compress    | Data           |
| Convert     | Data           |
| ConvertFrom | Data           |
| ConvertTo   | Data           |
| Dismount    | Data           |
| Edit        | Data           |
| Expand      | Data           |
| Export      | Data           |
| Group       | Data           |
| Import      | Data           |
| Initialize  | Data           |
| Limit       | Data           |
| Merge       | Data           |
| Mount       | Data           |
| Out         | Data           |
| Publish     | Data           |
| Restore     | Data           |
| Save        | Data           |
| Sync        | Data           |
| Unpublish   | Data           |
| Update      | Data           |

### Lifecycle Verbs

| Verb        | Group          |
|-------------|----------------|
| Approve     | Lifecycle      |
| Assert      | Lifecycle      |
| Complete    | Lifecycle      |
| Confirm     | Lifecycle      |
| Deny        | Lifecycle      |
| Disable     | Lifecycle      |
| Enable      | Lifecycle      |
| Install     | Lifecycle      |
| Invoke      | Lifecycle      |
| Register    | Lifecycle      |
| Request     | Lifecycle      |
| Restart     | Lifecycle      |
| Resume      | Lifecycle      |
| Start       | Lifecycle      |
| Stop        | Lifecycle      |
| Submit      | Lifecycle      |
| Suspend     | Lifecycle      |
| Uninstall   | Lifecycle      |
| Unregister  | Lifecycle      |
| Wait        | Lifecycle      |

### Diagnostic Verbs

| Verb        | Group          |
|-------------|----------------|
| Debug       | Diagnostic     |
| Measure     | Diagnostic     |
| Ping        | Diagnostic     |
| Repair      | Diagnostic     |
| Resolve     | Diagnostic     |
| Test        | Diagnostic     |
| Trace       | Diagnostic     |

### Communication Verbs

| Verb        | Group          |
|-------------|----------------|
| Connect     | Communications |
| Disconnect  | Communications |
| Read        | Communications |
| Receive     | Communications |
| Send        | Communications |
| Write       | Communications |

### Security Verbs

| Verb        | Group          |
|-------------|----------------|
| Block       | Security       |
| Grant       | Security       |
| Protect     | Security       |
| Revoke      | Security       |
| Unblock     | Security       |
| Unprotect   | Security       |

### Other Verbs

| Verb        | Group          |
|-------------|----------------|
| Use         | Other          |
