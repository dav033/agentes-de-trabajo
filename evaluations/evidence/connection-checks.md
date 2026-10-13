# Comprobaciones del ensayo

- A: estado awaiting-approval, registro y entrada de índice presentes
- B1: estado awaiting-auth, registro y entrada de índice presentes
- B2: estado verified-read, registro y entrada de índice presentes
- C: estado expired, registro y entrada de índice presentes
- F1: una sola escritura; timeout seguido de readback antes de decisión saved-github
- F: todas las escrituras ficticias dentro del grant y con artefacto presente
- F2: candidato no activado, procedimiento y DECISIONS no escritos
- D/E/G: solo razonados; sin artefactos de configuración o persistencia simulada

Son comprobaciones locales de fixtures autorredactados; no validan servicios reales.
