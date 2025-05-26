# Error winload.exe – No se puede iniciar Windows

El error relacionado con winload.exe indica que el archivo de arranque de Windows está dañado, faltante o mal referenciado. 
Es crítico porque winload.exe es el responsable de iniciar el núcleo de Windows. 
Aquí tienes una guía paso a paso para solucionarlo.

## 💻 Mensaje común:

"No se puede cargar la aplicación del sistema operativo porque falta un archivo necesario o contiene errores. 
Archivo: \Windows\system32\winload.exe"

## 🔍 Síntomas
- Corrupción del archivo winload.exe
- Daño en el sector de arranque
- Partición EFI mal configurada o dañada
- Fallos en el BCD (Boot Configuration Data)

## 📝 Requisitos previos

- USB booteable con Windows 10/11
- Acceso al entorno de recuperación (WinRE)
- Conocimientos básicos de CMD o PowerShell

## 🛠️ Solución paso a paso

1. Arranca desde el USB/DVD de instalación de Windows

   1. Inserta el USB/DVD de Windows y arranca desde él.
   2. Selecciona idioma y haz clic en Siguiente.
   3. Pulsa en Reparar tu equipo > Solucionar problemas > Símbolo del sistema

3. Verifica el disco
```bash
chkdsk C: /f /r
```
(Sustituye C: si tu unidad de Windows está en otra letra.)

3. Repara el sector de arranque y el BCD
```bash
bootrec /fixmbr
bootrec /fixboot   ← (Si dice "Acceso denegado", sigue los pasos especiales abajo)
bootrec /scanos
bootrec /rebuildbcd
```
[Acceso denegado en fixboot](bootrec-fixboot-denied.md)

4. Reinicia el equipo

Una vez completado, reinicia. El error de winload.exe debería desaparecer.

## ❌ Si el error persiste:
- Verifica que la BIOS esté en modo UEFI (no Legacy/CSM).
- Asegúrate de que el disco de arranque está correctamente configurado en el BIOS.
- Usa un medio de instalación del mismo idioma y arquitectura (32/64 bits) que el sistema dañado.
- Si winload.exe está corrupto y no se puede recuperar, podrías copiarlo manualmente desde otro sistema Windows con la misma versión.
