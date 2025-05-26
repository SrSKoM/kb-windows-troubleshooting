# Cómo eliminar una entrada de arranque en Windows (usando bcdedit)

1. Abrir el símbolo del sistema como administrador
    1. Si ya estás dentro de Windows, presiona:
    ```bash
    Tecla Windows + X → Símbolo del sistema (Admin) o PowerShell (Admin)
    ```
    
    2. Escribe:
    ```bash
    bcdedit
    ```

2. Identifica las entradas de arranque
Verás algo como esto:

```bash
Windows Boot Manager
--------------------
identifier              {bootmgr}
...

Windows Boot Loader
-------------------
identifier              {current}
device                  partition=C:
description             Windows 10
...

Windows Boot Loader
-------------------
identifier              {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}
device                  partition=D:
description             Windows 10
...

```

- El que dice {current} o el que tenga la partición correcta (en tu caso volumen x) es el que se debe conservar.
- El otro es el que vamos a eliminar.

3. Eliminar la entrada innecesaria
    1. Copia el identifier de la entrada que no quieres (por ejemplo: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}).
    2. Ejecuta:
    ```bash
    bcdedit /delete {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}
    ```
    (Sustitúyelo por el GUID real que copiaste).

4. Establecer la entrada correcta como predeterminada (opcional)
Por si quieres asegurarte de que siempre arranque con esa:

```bash
bcdedit /default {current}
```
O usa el identificador de la entrada que vas a conservar.

5. Evita el retraso del menú
Si quieres que arranque sin mostrar ningún menú:

```bash
bcdedit /timeout 0
```
