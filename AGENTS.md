# AGENTS.md - Proyecto BMW M135i 2017 (N55 EWG)

## Datos del Auto y ECU
- **Modelo**: BMW M135i (F20/F21) Año 2017.
- **Motor**: N55B30O0 (Electronic Wastegate - EWG).
- **Centralita (ECU)**: Bosch MEVD17.2.G.
- **Software**: MHD Flasher (F-Series).

## Modificaciones y Mapa
- **Escape**: Downpipe instalado.
- **Mapa Objetivo**: MHD Stage 2 (93 oct / 98 RON).
- **Opciones MHD**: Supresión de fallo de catalizador (CEL) activa, válvula de escape abierta en Sport.

## Carpetas del Proyecto
- `/xdf/`: Archivos de definición para TunerPro (`dmacpro91/BMW-XDFs`).
- `/bins/stock/`: Respaldo del mapa original de fábrica (NO MODIFICAR).
- `/bins/custom/`: Mapas modificados listos para flashear.
- `/logs/`: Archivos `.csv` exportados desde la app MHD.

## Reglas para el Agente de IA
1. **Proteger el archivo original**: Nunca modificar nada dentro de `/bins/stock/`.
2. **Revisar Logs (`.csv`)**: Al analizar logs de MHD con downpipe, revisar siempre:
   - Que el boost real (`Boost`) siga al objetivo (`Boost target`) sin picos peligrosos.
   - Que la temperatura de admisión (`IAT`) no suba demasiado (por tener intercooler original).
   - Que no haya retrasos de encendido (`Timing Corrections`) ni caídas de presión de bomba (`HPFP Act.`).
