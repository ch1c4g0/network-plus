

# Configuring a Radius server to use with VPN setups

I currently have Windows Server Core 2025 installed on my Proxmox host. This machine is going to run a Radius server to provide Authentication, Authorization, and Accounting for my VPN configurations.

## Initial Installation

When attempting to install the NPS tools, I received an error.

```
PS C:\Users\Administrator> Install-WindowsFeature NPAS -IncludeManagementTools
Install-WindowsFeature : ArgumentNotValid:    The role, role service, or feature name is    not valid: 'NPAS'. The name was not found. At line:1 char:1 + Install-WindowsFeature NPAS
-IncludeManagementTools
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~
    + CategoryInfo          : InvalidArgumen
   t: (NPAS:String) [Install-WindowsFeature
  ], Exception
    + FullyQualifiedErrorId : NameDoesNotExi
   st,Microsoft.Windows.ServerManager.Comma
  nds.AddWindowsFeatureCommand

Success Restart Needed Exit Code      Feature
                                       Result
------- -------------- ---------      -------
False   No             InvalidArgs    {}
```

After reading Microsofts documentation on Radius Servers and Radius Proxy Servers, I noticed that you cannot install NPAS on Server Core. You need a GUI to be able to use it. Because of this, I had to go back to the drawing board.

