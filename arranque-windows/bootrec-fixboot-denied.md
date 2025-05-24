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
