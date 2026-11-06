# Monitor de construcción y conglomerados

Avisos por correo, con los documentos adjuntos, de lo que publican estas empresas:

| País | Empresas | Fuente | Asunto del correo |
|---|---|---|---|
| Perú | Cementos Pacasmayo, Ferreycorp, Unacem | SMV (y BVL de respaldo) | `[HI] CPACASC1 – ...` |
| Chile | Salfacorp, Sigdo Koppers | CMF – hechos esenciales | `[HE] SALFACORP – ...` |
| Chile | Salfacorp, Sigdo Koppers | CMF – estados financieros (consolidado IFRS) | `[EEFF] SK – Estados financieros 3T26 – ...` |
| Colombia | Grupo Sura, Grupo Argos, Cementos Argos, Celsia, Corficolombiana, Promigas | SIMEV – información relevante | `[IR] GRUPOARGOS – ...` |

Es independiente del monitor de minería: otro repositorio, otros destinatarios y su propio `seen.json`.

Avisos de falla: `[MONITOR] La fuente X no responde...` si una fuente falla 12 revisiones seguidas (y otro cuando se recupera).

## Archivos
- `monitor_construccion.py`: el programa.
- `requirements.txt`: librerías que instala GitHub.
- `.github/workflows/monitor.yml`: horario y pasos.
- `seen.json`: lo ya avisado (lo crea y actualiza el monitor solo; no editar).

## Agregar o quitar empresas
En `monitor_construccion.py`, al inicio: `EMPRESAS` (Perú), `EMPRESAS_CMF` (Chile) y `EMPRESAS_COL` (Colombia).
Los destinatarios se cambian en **Settings → Secrets and variables → Actions → EMAIL_TO** (lista completa separada por comas).
