# Orca Profiles

Colección de perfiles personalizados para **OrcaSlicer**, pensada para cargar ajustes listos como punto de partida y reducir el tiempo de configuración manual.

## Qué incluye este repositorio

- `machine/`: perfil de máquina para `Creality Ender-3 Pro 0.4 nozzle - ED`
- `filament/`: perfiles de filamento como `Creality CR-PETG`, `Creality CR-PETG (Ajustado)`, `Creality CR-PETG (Ajustado V2)` y `Sain Smart TPU`
- `process/`: perfil de proceso `0.20mm Standard @Creality Ender3 Pro 0.4 - Custom`

Cada perfil se guarda como:

- `*.json`: ajustes del perfil
- `*.info`: metadatos de OrcaSlicer

## Para quién es

Este repositorio está orientado a usuarios de OrcaSlicer que quieran usar perfiles ya ajustados para una **Creality Ender-3 Pro** con boquilla de `0.4 mm`, especialmente para PETG y TPU.

## Cómo usarlos en OrcaSlicer

1. Descarga o clona este repositorio.
2. Localiza el tipo de perfil que necesitas: máquina, filamento o proceso.
3. Importa los archivos en OrcaSlicer o copia los perfiles a tu biblioteca local.
4. Selecciona la combinación adecuada de máquina, filamento y proceso.
5. Revisa los ajustes clave antes de imprimir.

## Instalación manual

Si prefieres copiar los perfiles directamente, mantén juntos los pares `.json` y `.info` dentro de la carpeta correspondiente de OrcaSlicer.

Rutas habituales de perfiles de usuario:

- Windows: `%AppData%\\OrcaSlicer\\user\\default\\`
- macOS: `~/Library/Application Support/OrcaSlicer/user/default/`
- Linux: `~/.config/OrcaSlicer/user/default/`
- Linux (Flatpak): `~/.var/app/io.github.softfever.OrcaSlicer/config/OrcaSlicer/user/default/`

Dentro de esa ubicación, coloca cada archivo en su categoría:

- `machine/` para perfiles de impresora
- `filament/` para perfiles de material
- `process/` para perfiles de proceso

Si tu instalación usa otro directorio o varios perfiles de usuario, verifica la ruta exacta desde la configuración local de OrcaSlicer.

## Qué revisar antes de imprimir

- Que el perfil de máquina coincida con tu impresora y extrusor.
- Que el filamento seleccionado corresponda al material real cargado.
- Que las temperaturas de boquilla y cama sean adecuadas para tu lote de material.
- Que la retracción, ventilación y soportes encajen con tu montaje.
- Que la herencia (`inherits`) apunte a un perfil base disponible en tu instalación.

## Recomendación

Usa estos perfiles como base, no como ajuste universal. Haz una prueba corta antes de una impresión larga y guarda tus variantes si cambias temperatura, flujo o retracción.
