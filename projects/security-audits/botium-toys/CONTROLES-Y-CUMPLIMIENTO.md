# Controles y revisión de cumplimiento: Botium Toys

> **Fuente del estado:** PDF de evaluación aportado por el usuario. Los estados siguientes son lo que el documento reporta; no se verificaron mediante pruebas técnicas independientes. El informe adjunto evalúa 14 controles y marca uno como implementado. El detalle disponible no permite auditar por cuenta propia las evidencias, metodología o cálculos del informe.

## Alcance descrito por el documento

El PDF incluye el comercio electrónico, terminales de punto de venta (POS), redes de oficinas y almacenes, y entornos de datos de tarjetas y datos personales que el documento afirma que procesa la organización. También afirma que se recopilan datos de salud y de menores. Esos tipos de datos y flujos no aparecen demostrados con evidencia adjunta; deben confirmarse antes de tratarlos como inventario validado o base de análisis regulatorio.

## Matriz de 14 controles

| # | Control | Dominio | Estado reportado en el PDF | Prioridad sugerida para validación / acción |
|---:|---|---|---|---|
| 1 | Mínimo privilegio (RBAC) | Organizativo / técnico | No implementado | Alta: revisar permisos en cuentas, carpetas, bases de datos y accesos de terceros; retirar privilegios excesivos. |
| 2 | Recuperación ante desastres y continuidad | Organizativo | No implementado | Alta: definir objetivos de recuperación, responsables, dependencias y ejercicios; enlazar con respaldos probados. |
| 3 | Política de contraseñas y autenticación | Organizativo / técnico | No implementado | Alta: revisar autenticación, MFA, recuperación y protección contra intentos abusivos de acuerdo con el riesgo y buenas prácticas vigentes. |
| 4 | Separación de funciones | Organizativo | No implementado | Alta: identificar conflictos entre administración, TI y finanzas; definir aprobaciones y controles compensatorios. |
| 5 | Firewall | Técnico | No implementado | Alta: confirmar la configuración y cobertura de perímetro, redes internas, tienda, POS, almacén y servicios publicados; diseñar reglas y segmentación. |
| 6 | Sistema de detección de intrusiones (IDS) | Técnico | No implementado | Alta: establecer fuentes de telemetría, alertas, responsables, retención y respuesta; evaluar capacidades IDS/EDR/SIEM según arquitectura. |
| 7 | Respaldos | Técnico / organizativo | No implementado | Alta: implantar copias programadas con acceso restringido y protección ante alteración; probar restauración y recuperación. |
| 8 | Protección antimalware / EDR | Técnico | No implementado | Alta: validar cobertura gestionada de servidores, POS y estaciones; configurar actualizaciones, alertas y contención. |
| 9 | Supervisión, mantenimiento e intervención manual de sistemas heredados | Técnico / organizativo | Sí implementado | Mantener evidencia del proceso y responsables; evaluar cobertura, registros, vulnerabilidades, soporte y límites de la intervención manual. |
| 10 | Cifrado de datos | Técnico | No implementado | Alta: descubrir datos y flujos; definir cifrado en tránsito y reposo, gestión de claves y excepciones según requisitos aplicables. Validar mediante revisión técnica. |
| 11 | Gestor corporativo de contraseñas/secretos | Técnico | No implementado | Alta: seleccionar solución controlada para credenciales privilegiadas, acceso, recuperación y auditoría; eliminar secretos expuestos. |
| 12 | Cerraduras y acceso físico a oficinas, tienda y almacén | Físico | No implementado | Alta: validar áreas críticas, controles de llaves, bajas de acceso, visitantes y registros. |
| 13 | Videovigilancia CCTV | Físico | No implementado | Media/alta: analizar cobertura y gestión de grabaciones; valorar privacidad, señalización, acceso y retención conforme a la ley aplicable. |
| 14 | Detección y prevención de incendios | Físico | No implementado | Media/alta: inspeccionar sistemas, mantenimiento, alertas, evacuación y protección de infraestructura con responsables competentes. |

**Nota de reconciliación:** una referencia pública secundaria consultada durante la elaboración inicial marcaba el firewall como implementado. El PDF que aportaste lo marca como no implementado. Esta matriz sigue el PDF del usuario y conserva la discrepancia en el informe principal; debe resolverse con evidencia de configuración antes de cerrar el hallazgo.

## Revisión de cumplimiento: qué puede concluirse y qué falta

### PCI DSS

El PDF sostiene que son aplicables los entornos e-commerce y POS y que el cumplimiento es deficiente. Que se acepten pagos con tarjeta hace pertinente evaluar PCI DSS, pero no basta por sí solo para declarar un incumplimiento confirmado ni para fijar una multa. Se necesita definir el entorno de datos de tarjetas (CDE), flujos de datos, sistemas conectados o que pueden afectar su seguridad, proveedores, segmentación y las obligaciones de validación con adquirente/marca de pago. PCI DSS establece requisitos técnicos y operativos para proteger datos de pago.[1]

### GDPR / RGPD

El PDF afirma que se procesan datos de la UE, incluso datos de salud y de menores, y concluye incumplimiento total. Esas categorías necesitan evidencia: inventario, propósito, base jurídica, origen, usuarios, retención, proveedores y ubicación. La aplicabilidad territorial también requiere analizar si se ofrecen bienes/servicios a personas en la UE o se monitorea su comportamiento, entre otros hechos relevantes. No es prudente declarar una conclusión jurídica cerrada a partir de una tabla sin esa documentación.

El artículo 33 exige, en los casos cubiertos, que el responsable notifique a la autoridad competente sin demora indebida y, cuando sea factible, dentro de 72 horas desde que tenga conocimiento, salvo que sea improbable que la brecha genere riesgo para los derechos y libertades. Si la notificación se retrasa, se explican los motivos; la información puede entregarse por fases. El encargado debe notificar al responsable sin demora indebida. El artículo 34 regula por separado la comunicación a las personas cuando se cumplan sus condiciones, incluida la probabilidad de alto riesgo.[2] Por eso no debe resumirse como una obligación automática de avisar a toda persona afectada siempre dentro de 72 horas.

Las cifras de sanciones y la aplicación de la normativa española (LOPDGDD/AEPD) incluidas en el PDF no se trasladan a este portafolio como exposición confirmada de Botium Toys. La autoridad competente, la norma aplicable, la infracción y la sanción dependen de hechos y jurisdicción; una sanción no se puede calcular automáticamente a partir de la ausencia de un control.

### SOC 1 y SOC 2

El PDF califica cuatro criterios como no implementados y deriva un resultado de “0 de 4”. Esa cuenta no constituye por sí sola una auditoría SOC ni acredita que Botium Toys “falle el 100%” de una obligación universal. SOC es una familia de informes de atestación: su alcance depende del servicio, los criterios, el periodo y los usuarios previstos. SOC 1 se relaciona con controles pertinentes a la información financiera de entidades usuarias; SOC 2 se relaciona con criterios de servicios de confianza. La necesidad de un informe depende de contratos, clientes y modelo de servicios; no es una ley general que toda empresa deba certificar.[3]

## Riesgos que sí conviene priorizar

Según el estado reportado en el PDF, la combinación de acceso sin mínimo privilegio, ausencia de firewall reportada, falta de detección, cifrado y respaldos, controles débiles sobre endpoints y deficiencias físicas justificaría una validación prioritaria. Los impactos potenciales incluyen acceso indebido a datos, interrupción de ventas, pérdida de integridad de registros y recuperación lenta. Son escenarios de riesgo, no incidentes ocurridos ni pérdidas financieras medidas.

El PDF aporta costos promedio de brechas, duración de incidentes, ahorros por cifrado y montos de multas. No se adoptan aquí como estimación de impacto para Botium Toys: el archivo no aporta un modelo cuantitativo específico, datos de exposición, supuestos, análisis de sensibilidad ni una fuente verificable que permita aplicarlos a esta empresa ficticia. Para cuantificar el riesgo se necesita metodología transparente, datos pertinentes y validación del dueño del riesgo.

## Plan de validación y remediación

1. **Resolver discrepancias y preservar evidencia:** confirmar el estado del firewall y las demás filas con diagramas, políticas, configuraciones, muestras de cuentas, registros y entrevistas autorizadas.
2. **Establecer alcance de datos:** documentar e-commerce, POS, flujos de pagos, datos personales efectivamente tratados, proveedores, segmentación y responsabilidades.
3. **Tratar primero controles de exposición alta:** acceso privilegiado, segmentación de red/firewall, autenticación y protección de credenciales, cifrado contextual, endpoint y monitoreo.
4. **Asegurar recuperación:** respaldos protegidos y probados, plan de continuidad y recuperación, procedimientos de respuesta y simulacros.
5. **Validar controles físicos y legado:** verificar cerraduras, visitantes, videovigilancia respetuosa de privacidad, prevención de incendios y compensaciones para sistemas heredados.
6. **Cerrar hallazgos con evidencia:** asignar responsables, fechas, riesgo residual y pruebas de eficacia. La clasificación final debe basarse en impacto y probabilidad validados, no en el rótulo del documento por sí solo.

## Referencias

[1]: https://www.pcisecuritystandards.org/standards/pci-dss/ "PCI Security Standards Council, PCI DSS"
[2]: https://eur-lex.europa.eu/eli/reg/2016/679/oj "Reglamento General de Protección de Datos, artículos 33 y 34"
[3]: https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services "AICPA, System and Organization Controls suite"
