The cmdlets are available on PowerShell Gallery and can be installed in an elevated PowerShell session.

Some of the common and most frequently used Power BI Cmdlets are provided below. 

## Installation

```powershell-interactive
PowerShell

Install-Module -Name MicrosoftPowerBIMgmt
```

For example, if you only wanted the Workspaces module, you could install individual modules (based on your needs) instead of the rollup module.

```powershell-interactive
PowerShell

Install-Module -Name MicrosoftPowerBIMgmt.Workspaces
```

## Log in to Power BI

```powershell-interactive
PowerShell

Connect-PowerBIServiceAccount  # or use aliases: Login-PowerBIServiceAccount,Login
```

## Get workspaces

Get workspaces for the user. By default, for example - without -first parameter, it shows the first 100 workspaces assigned to the user.

```powershell-interactive
PowerShell

Get-PowerBIWorkspace
```

Use the -All parameter to show all workspaces assigned to the user.


```powershell-interactive
PowerShell

Get-PowerBIWorkspace -All
```

If you are a tenant administrator, you can view all workspaces in your tenant by adding -Scope Organization.

```powershell-interactive
PowerShell

Get-PowerBIWorkspace -Scope Organization -All
```

For additional commonly used Power BI cmdlets, see [Microsoft Power BI Cmdlets for Windows PowerShell and PowerShell Core](/powershell/power-bi/overview?view=powerbi-ps/?azure-portal=true).
