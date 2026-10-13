# Agentes de trabajo

Una skill principal para personas no técnicas: describes el trabajo, defines un agente con ayuda de ChatGPT Work y lo mejoras con el uso. Conserva contexto, decisiones, procedimientos y conexiones en el mismo repositorio.

Puedes decir:

- «Quiero un agente que me ayude a preparar facturas».
- «Sigamos con el agente de compras».
- «Solo para este cliente, cambia el formato».
- «Ahora quiero que consulte los pedidos en mi sistema».
- «Qué quedó pendiente, qué aprendió y qué conexión le falta».

La skill hace preguntas breves, propone una primera versión y la prueba con un caso. Recuerda aprendizajes confirmados dentro del permiso de guardado acordado. Para cambiar procesos, reglas de negocio o permisos prepara una propuesta y pide aprobación cuando todavía no la tiene.

## Conexiones proactivas

Al crear o retomar un agente, comprueba qué herramientas necesita y cuáles funcionan. Reutiliza conexiones existentes, busca plugins o MCP relevantes cuando falta una capacidad, prepara la configuración y recuerda el estado y el próximo paso. Aplica cambios ya autorizados y verifica el resultado; los nuevos accesos y permisos requieren aprobación. El inicio de sesión se realiza en el servicio correspondiente, sin guardar contraseñas ni tokens en GitHub.

Una conexión instalada puede seguir sin autenticar; leer datos no demuestra permiso de escritura. La skill mantiene esas diferencias y continúa con el trabajo que pueda hacer mientras falta acceso.

## Prepararlo en ChatGPT Work

1. Habilita la carpeta [de la skill](skills/agentes-de-trabajo/SKILL.md) mediante el mecanismo de skills que admita tu aplicación. En la documentación oficial, las skills independientes se admiten en escritorio; para distribuirlas entre superficies se usa un plugin. No basta con subir este repositorio para que quede instalada.
2. Selecciona este repositorio o una copia privada para tu usuario/equipo y permite su lectura desde el entorno de Work. Completa [WORKSPACE.md](WORKSPACE.md) con el destino real; no copies el permiso del autor a otro despliegue.
3. Conecta GitHub mediante una integración disponible que permita las operaciones necesarias. Si falta escritura, la skill puede preparar cambios y marcar el guardado pendiente. El nombre del servicio no garantiza que sus herramientas permitan escribir.
4. Si quieres guardado automático, autoriza una vez el repositorio, la rama, las carpetas y las operaciones concretas. Ese permiso no autoriza enviar facturas, cambiar reglas o instalar servicios.
5. Invoca «Agentes de trabajo» con el selector de skills y describe tu primera tarea. Comprueba una prueba y un guardado real antes de depender de la continuidad entre sesiones.

La instalación y los permisos concretos dependen de la cuenta y el entorno. Una configuración MCP local no configura por sí sola Work alojado. No hay servicio de ejecución ni programación en segundo plano en este paquete.

Documentación oficial consultada el 12 de octubre de 2026: [skills](https://learn.chatgpt.com/docs/build-skills), [plugins](https://learn.chatgpt.com/docs/plugins) y [MCP](https://learn.chatgpt.com/docs/extend/mcp). Revisa esas fuentes para los pasos vigentes de tu entorno.

## Qué se guarda

| Ubicación | Contenido |
|---|---|
| [skills/agentes-de-trabajo](skills/agentes-de-trabajo/SKILL.md) | Coordinadora, referencias y plantillas. |
| [agents/INDEX.md](agents/INDEX.md) | Registro y carpetas de los agentes que crees. |
| [connections/INDEX.md](connections/INDEX.md) | Conexiones requeridas, verificaciones y pasos pendientes. |
| [WORKSPACE.md](WORKSPACE.md) | Propietario, destino y permisos de guardado. |
| [examples/invoice-drafts](examples/invoice-drafts/SKILL.md) | Ejemplo ficticio, separado de agentes activos. |
| [evaluations](evaluations/CASES.md) | Casos de evaluación y resultados reales de esta versión. |

Este paquete se distribuye públicamente y contiene instrucciones reutilizables y datos ficticios. Para trabajar con memoria real, usa una copia privada por usuario o equipo. Quien tenga acceso al repositorio podrá leer su memoria; las carpetas no son un límite de privacidad. Conserva referencias y decisiones útiles, no facturas completas, credenciales ni conversaciones enteras. El archivo .gitignore ayuda a excluir archivos habituales, pero no sustituye la revisión antes de guardar.

Consulta [los resultados de validación](evaluations/RESULTS.md) para distinguir las pruebas locales realizadas de la instalación en ChatGPT Work y las conexiones reales que quedan pendientes. Subir el paquete a GitHub no instala la skill ni conecta Work automáticamente.
