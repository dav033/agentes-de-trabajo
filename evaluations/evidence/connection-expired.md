---
schema_version: 1
id: sales-demo-read
state: expired
---
# Ventas Demo — SIMULACIÓN AISLADA
- Propósito: consultar pedidos del agente de borradores.
- Entorno: hosted Work FICTICIO.
- Proveedor/documentación: Ventas Demo, directorio/documentación FICTICIOS.
- Cuenta: ventas-prueba (fixture).
- Plugin ID: sales-demo-read, exacto según directorio ficticio; no endpoint descubierto.
- Referencia de configuración/secreto: ninguna guardada.
- Operaciones deseadas: orders.read; alcance mínimo de consulta.
- Capacidad observada: Lectura ficticia actual devuelve authorization_expired; ayer verified-read.
- Autorización de instalación: ninguna en A; en B-C el fixture solo acredita instalación existente.
- Autorización comercial: consulta solicitada; no emisión, modificación ni envío.
- Verificación: 2026-10-12, exclusivamente fixture; no acredita conexión real.
- Escritura: no probada.
- Siguiente acción: Autenticación del propietario y nueva lectura; el modo dependiente queda blocked.
- Persistencia del escenario: sin grant remoto suministrado; archivo local del ensayo.
- Rollback: no hubo cambios de configuración reales ni ficticios aplicados en A-C.
