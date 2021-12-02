# Windows 10

## Activation

Sometimes you need to activate a licence on a VM for temporary use.  
Here's how to do it:

1. Open an administrative command prompt.
2. Enter ```slmgr.vbs /upk```. This uninstalls the currently intalled product key (if one exists).  
3. Enter ```slmgr.vbs /ipk [product key]```. This installs the product key for the required version.  
4. Enter ```slmgr.vbs /ato```. This attempts online activation.