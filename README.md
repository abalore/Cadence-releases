<p align="center">
  <img src="cadence.svg" alt="Cadence" width="128" height="128">
</p>

<h1 align="center">Cadence</h1>

<p align="center">
  Emulador de <b>Amstrad CPC</b> escrito en C++ y Qt 6, con debugger y ensamblador integrados.
</p>

<p align="center">
  <a href="https://github.com/abalore/Cadence-releases/releases/latest"><b>⬇️  Descargar la última versión</b></a>
</p>

---

Este repositorio contiene únicamente las **descargas** (binarios precompilados) de Cadence.

## Descargas

Ve a la **[página de releases](https://github.com/abalore/Cadence-releases/releases/latest)** y descarga el fichero de tu plataforma:

| Plataforma | Fichero | Cómo ejecutar |
|---|---|---|
| **Linux** | `Cadence-<ver>-x86_64.AppImage` | `chmod +x Cadence-*.AppImage && ./Cadence-*.AppImage` |
| **Windows** | `cadence-windows-x64.zip` | Descomprime y ejecuta `cadence.exe` |
| **macOS** (Apple Silicon) | `Cadence-<ver>-macOS-arm64.dmg` | Abre el `.dmg`, arrastra a *Aplicaciones*. Ver nota abajo. |

Todos los binarios son **autocontenidos**: Qt 6, PortAudio y el resto de dependencias van incluidas.

### Nota para macOS

El `.app` está firmado *ad-hoc* (sin certificado de Apple Developer), por lo que Gatekeeper lo bloqueará la primera vez. Para abrirlo:

- **Botón derecho → Abrir** sobre la app (y confirma en el diálogo), **o**
- desde terminal: `xattr -cr /Applications/cadence.app`

## Cómo usarlo

| Tecla | Acción | | Tecla | Acción |
|---|---|---|---|---|
| `F1` | Insertar cinta | | `F6` | Abrir el ensamblador |
| `Shift+F1` | Rebobinar cinta | | `F9` | *Unlock speed* |
| `Ctrl+F1` | Extraer cinta | | `F10` | Emulación de joystick |
| `F2` | Insertar disco (A) | | `F11` | Pantalla completa |
| `Ctrl+F2` | Extraer disco (A) | | `Ctrl+F11` | Smoothing |
| `F3` | Insertar cartucho | | `Shift+F11` | Monitor verde |
| `Ctrl+F3` | Extraer cartucho | | `F12` | Reset |
| `F5` | Abrir el debugger | | `Ctrl+0`…`Ctrl+5` | Persistencia de fósforo |

Una vez insertado un medio:

- **Cinta**: `RUN"` (o `RUN"name` para un fichero concreto).
- **Disco**: `RUN"DISC` para el cargador por defecto, o `CAT` para listar.
- **Cartucho**: arranca automáticamente al insertarlo.

También puede cargarse media desde archivos **`.zip`**.

---

## Autor

© Abalore, 2026.
