# Si bootrec /fixboot te da "Acceso denegado", usa este comando alternativo:

## 🔨 Recrear BCD manualmente:
1. Inicia DiskPart:
```bash
diskpart
```
2. Lista discos y selecciona el principal:
```bash
list disk
select disk 0
```
3. Lista particiones y selecciona la EFI (100–300 MB, FAT32):
```bash
list partition
select partition X
assign letter=V:
exit
```
## ✅ ¿Cuál es la partición EFI?

La partición EFI (o ESP: EFI System Partition) es una partición especial del sistema que contiene los archivos necesarios para iniciar (bootear) Windows o cualquier sistema operativo compatible con UEFI.

## 🔍 Características típicas de la partición EFI:

| Característica      | Valor típico                              |
| ------------------- | ----------------------------------------- |
| Tamaño              | Entre **100 MB y 300 MB**                 |
| Sistema de archivos | **FAT32**                                 |
| Tipo                | **Partición del sistema EFI** o "Sistema" |
| Etiqueta (nombre)   | A veces llamada "ESP" o "Sistema"         |


## ❌ ¿Puede ser la partición "Principal"?

No. La partición principal o "Primary" usualmente contiene el sistema operativo, es decir, el disco C:.
La EFI es otra partición, más pequeña, que se usa exclusivamente para el arranque.

## 📦 ¿Cómo identificar la partición EFI correctamente?

Si usas diskpart (desde CMD):

1. Ejecuta:
```bash
diskpart
list disk
select disk 0
list partition
```
2. Verás algo así:
```bash
Partition 1   System    260 MB   FAT32
Partition 2   Primary    118 GB   NTFS
Partition 3   Recovery   500 MB
```
✅ Aquí, la partición "System", 260 MB, FAT32 → es la EFI.

## ✅ Resumen
| ¿Es la partición EFI?           | Respuesta |
| ------------------------------- | --------- |
| ¿Es de 100–300 MB?              | ✅ Sí      |
| ¿Está en FAT32?                 | ✅ Sí      |
| ¿Dice “Sistema” o “System”?     | ✅ Sí      |
| ¿Es la de 100 GB o más?         | ❌ No      |
| ¿Es la “Principal” o “Primary”? | ❌ No      |
