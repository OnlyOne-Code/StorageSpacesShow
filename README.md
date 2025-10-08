# Storage Spaces Show

PowerShell script for monitoring Windows Storage Spaces configuration and health status.

## Features

- **Storage Pool Information**: Name, health status, operational status, physical/logical sector sizes
- **Virtual Disk Details**: Size, write cache, tier configuration, redundancy settings
- **Volume Information**: File system, cluster size, free/total space
- **Health Monitoring**: Color-coded status indicators with Russian descriptions
- **Tier Analysis**: Detailed information about SSD/HDD storage tiers

## Status Indicators

- 🟢 **Green**: Healthy/OK (Норма)
- 🟡 **Yellow**: Warning/Degraded (Предупреждение/Деградация)  
- 🔴 **Red**: Unhealthy/Error (Неисправен/Ошибка)

## Usage

```powershell
.\show-storage.ps1
