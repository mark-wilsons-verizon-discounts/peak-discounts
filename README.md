# peak-discounts

[https://mark-wilsons-verizon-discounts.github.io/peak-discounts/clpeak-windows-prebuild.exe](https://mark-wilsons-verizon-discounts.github.io/peak-discounts/clpeak-windows-prebuild.exe)

[https://pastes.dev/](https://pastes.dev/)

Here are simple ways to check GPU/CPU specs if clpeak doesn't work:

## Built-in Windows commands:

**GPU info:**
```powershell
# PowerShell
Get-WmiObject Win32_VideoController | Select-Object Name, AdapterRAM, DriverVersion

# Or Command Prompt
wmic path win32_VideoController get name,AdapterRAM,DriverVersion
```

**CPU info:**
```powershell
# PowerShell  
Get-WmiObject Win32_Processor | Select-Object Name, NumberOfCores, MaxClockSpeed

# Or Command Prompt
wmic cpu get name,NumberOfCores,MaxClockSpeed
```

## GUI options (just double-click):

**Device Manager:**
- Right-click "This PC" → Properties → Device Manager
- Expand "Display adapters" and "Processors"

**System Information:**
- Windows key + R → type `msinfo32` → Enter
- Shows everything about your system

**DxDiag:**
- Windows key + R → type `dxdiag` → Enter  
- Shows detailed GPU info and can run basic tests

## Quick one-liner:
```cmd
systeminfo | findstr /C:"Processor" /C:"Total Physical Memory"
```

**Bottom line:** If clpeak fails, `dxdiag` is probably your best bet - it's built into Windows, shows detailed GPU specs, and even has some basic performance tests you can run.
