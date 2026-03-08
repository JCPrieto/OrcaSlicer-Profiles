# Orca Profiles

Repositorio de perfiles personalizados para **OrcaSlicer**, organizados por tipo de ajuste para facilitar su mantenimiento y reutilización.

## Estructura

- `machine/`: perfiles de impresora y extrusor.
- `filament/`: perfiles de material y variantes ajustadas.
- `process/`: perfiles de proceso de impresión.

Cada perfil suele tener dos archivos con el mismo nombre base:

- `*.json`: configuración del perfil.
- `*.info`: metadatos asociados usados por OrcaSlicer.

## Perfiles incluidos

- Máquina: `Creality Ender-3 Pro 0.4 nozzle - ED`
- Filamentos: `Creality CR-PETG`, `Creality CR-PETG (Ajustado)`, `Creality CR-PETG (Ajustado V2)`, `Sain Smart TPU`
- Proceso: `0.20mm Standard @Creality Ender3 Pro 0.4 - Custom`

## Uso

1. Abre OrcaSlicer.
2. Importa o copia los perfiles correspondientes.
3. Verifica que las herencias (`inherits`) apunten al perfil base esperado.
4. Revisa temperaturas, retracción, ventilación y soportes antes de imprimir.

## Validación recomendada

Antes de subir cambios, conviene validar los archivos localmente:

```bash
jq . filament/*.json machine/*.json process/*.json
git diff -- filament/ machine/ process/
git status --short
```

## Convenciones

- Mantener juntos los pares `.json` y `.info`.
- Respetar la indentación existente en JSON de 4 espacios.
- Usar nombres descriptivos alineados con el campo `name` interno del perfil.

## Objetivo

Centralizar perfiles ajustados para una **Creality Ender-3 Pro** con boquilla de `0.4 mm`, incluyendo configuraciones de materiales y procesos listos para afinar y reutilizar.
