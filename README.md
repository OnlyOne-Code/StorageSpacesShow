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
.\StorageSpacesShow.ps1
```

## Example

```text
=== Storage Pool Information ===
Name: Library StoragePool
Health Status: Healthy (Норма)
Operational Status: OK (Норма)
Physical Sector Size: 4096 bytes
Logical Sector Size: 512 bytes

Physical Disks (6):
  ATA Samsung SSD 870
    Media Type: SSD
    Size: 465.76 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)
  ATA HGST HTS721010A9
    Media Type: HDD
    Size: 931.51 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)
  ATA WDC WD10JPLX-00M
    Media Type: HDD
    Size: 931.51 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)
  ATA WDC WD10JPLX-00M
    Media Type: HDD
    Size: 931.51 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)
  ATA WDC WD10JPLX-00M
    Media Type: HDD
    Size: 931.51 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)
  ATA WDC WD10JPLX-00M
    Media Type: HDD
    Size: 931.51 GB
    Physical Sector Size: 512 bytes
    Logical Sector Size: 512 bytes
    Operational Status: OK (Норма)
    Health Status: Healthy (Норма)

=== Virtual Disk Information ===
Name: Library VirtualDisk
Health Status: Healthy (Норма)
Operational Status: OK (Норма)
Access: Read/Write (Чтение/Запись)
Detached Reason: None (Нет)
Size: 3658 GB
Write Cache Size: 24 GB
Is Tiered: True
Storage Pool: Library StoragePool

Детальная информация по Tiers:
Tier: Library VirtualDisk-HDDTier
  Media Type: HDD
  Resiliency Setting: Parity
  Interleave: 16384
  Physical Disk Redundancy: 1
  Size: 3530 GB
  Number of Columns: 5
Tier: Library VirtualDisk-SSDTier
  Media Type: SSD
  Resiliency Setting: Simple
  Interleave: 65536
  Physical Disk Redundancy: 0
  Size: 128 GB
  Number of Columns: 1

=== Volume Information ===
Drive Letter: I
Volume Name: Library
File System: NTFS
Cluster Size: 64 KB
Total Size: 3657.98 GB
Free Space: 1664.85 GB
```
