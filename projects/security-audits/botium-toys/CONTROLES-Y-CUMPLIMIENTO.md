# Lista de controles y cumplimiento: Botium Toys

> **Caso didáctico ficticio.** Esta matriz es una reconstrucción a partir del escenario adjunto y de un ejemplo público elaborado por un estudiante; no es una plantilla oficial del curso.[1] La columna de estado no representa una verificación técnica independiente. «Pendiente según el caso» significa que la referencia didáctica indica que el control necesita implementarse; no constituye evidencia de que una organización real carezca de él.

## Clave de estado y prioridad

- **Estado:** «Indicado como existente» o «Indicado como pendiente» según la información didáctica disponible. «Por validar» cuando la hoja no permite establecer una conclusión.
- **Prioridad:** evaluación inicial propuesta para el ejercicio. Alta = reducir primero riesgo material; Media = planificar después de controles de mayor exposición; Baja = mejora de apoyo. La prioridad real requiere validar impacto, probabilidad y controles compensatorios.

## Controles administrativos

| Control | Tipo / propósito | Estado según el ejercicio | Prioridad | Recomendación / evidencia para validar |
|---|---|---|---|---|
| Mínimo privilegio | Preventivo; limita accesos de personal y proveedores a lo necesario para su función. | Pendiente | Alta | Definir roles, retirar privilegios innecesarios y revisar permisos. Muestrear cuentas y autorizaciones. |
| Plan de recuperación ante desastres | Correctivo; restaura sistemas, datos, instalaciones y conectividad. | Pendiente | Alta | Definir RTO/RPO, dependencias, responsables y procedimientos; realizar ejercicio y prueba de restauración. |
| Política de contraseñas y autenticación | Preventivo; establece requisitos de autenticación y controles frente a acceso indebido. | Pendiente | Alta | Alinear configuración con riesgos, habilitar MFA para accesos privilegiados/remotos cuando proceda y probar controles de bloqueo/recuperación. Evitar reglas que fomenten prácticas inseguras. |
| Política de control de acceso | Preventivo; protege confidencialidad e integridad. | Pendiente | Alta | Documentar concesión, revisión, revocación, acceso remoto y emergencias; obtener aprobaciones y verificar registros. |
| Gestión del ciclo de vida de cuentas | Preventivo; limita riesgos de cuentas obsoletas o indebidas. | Pendiente | Alta | Vincular altas, cambios y bajas a procesos de RR. HH.; verificar revocación oportuna y revisar cuentas inactivas. |
| Separación de funciones | Preventivo; reduce fraude o abuso al evitar concentración incompatible de privilegios. | Pendiente | Alta | Identificar funciones incompatibles, revisar conflictos y establecer controles compensatorios documentados. |

## Controles técnicos

| Control | Tipo / propósito | Estado según el ejercicio | Prioridad | Recomendación / evidencia para validar |
|---|---|---|---|---|
| Firewall | Preventivo; filtra tráfico de red no autorizado. | Indicado como existente | Mantener / validar | Revisar reglas, cambios, segmentación, exposición y registros; probar que las reglas corresponden al flujo autorizado. La existencia por sí sola no demuestra eficacia. |
| Sistema de detección de intrusiones (IDS) | Detectivo; identifica actividad anómala o indicios de intrusión. | Pendiente | Alta | Evaluar fuentes, cobertura, alertas, responsables, retención y pruebas de detección. Considerar capacidades equivalentes integradas si satisfacen los objetivos. |
| Cifrado | Preventivo; reduce exposición de datos sensibles durante transmisión y almacenamiento. | Pendiente | Alta | Inventariar datos y flujos, aplicar cifrado moderno en tránsito y en reposo según riesgo, proteger claves y verificar configuraciones y excepciones. |
| Respaldos | Correctivo; permiten recuperar datos y servicios. | Pendiente | Alta | Definir alcance, frecuencia, retención y protección contra borrado o alteración; verificar restauración y controles de acceso a copias. |
| Gestión de contraseñas / secretos | Preventivo; centraliza custodia, acceso y ciclo de vida de credenciales. | Pendiente | Alta | Usar una solución aprobada, limitar acceso, habilitar MFA, evitar secretos en código y rotar ante exposición. |
| Protección antimalware / endpoint | Detectivo y correctivo; identifica y contiene amenazas conocidas. | Pendiente | Alta | Confirmar cobertura de endpoints y servidores, actualizaciones, políticas, alertas y respuesta; evaluar EDR si se justifica. |
| Supervisión y mantenimiento de sistemas heredados | Preventivo/detectivo/correctivo; compensa riesgos de plataformas difíciles de actualizar. | Pendiente | Alta | Inventariar versiones y soporte; aislar, limitar accesos, monitorear, documentar intervención manual y planificar reemplazo. |
| Registro, centralización y monitoreo | Detectivo; facilita investigar eventos y alertar a tiempo. | Por validar | Alta | Confirmar si hay SIEM u otra capacidad, cobertura de fuentes, sincronización de tiempo, retención, integridad, alertas y atención efectiva. |

## Controles físicos

| Control | Tipo / propósito | Estado según el ejercicio | Prioridad | Recomendación / evidencia para validar |
|---|---|---|---|---|
| Caja fuerte con control de tiempo | Disuasivo; limita acceso físico a activos guardados. | Pendiente | Baja / media | Determinar si el riesgo y el tipo de activo justifican este control; validar custodia y acceso. |
| Iluminación adecuada | Disuasivo; mejora visibilidad y reduce zonas ocultas. | Pendiente | Baja / media | Inspeccionar áreas de oficina, tienda, almacén y perímetro según riesgo. |
| Videovigilancia CCTV | Preventivo/detectivo; apoya disuasión e investigación. | Pendiente | Media / alta | Evaluar cobertura, acceso a grabaciones, retención, señalización y obligaciones de privacidad; no instalar sin revisión legal aplicable. |
| Gabinetes con llave para equipo de red | Preventivo; reduce manipulación física no autorizada. | Pendiente | Media / alta | Inspeccionar cuartos y racks; verificar llaves, control de acceso y registro de visitantes. |
| Señalización del proveedor de alarma | Disuasivo; comunica presencia de un sistema de alarma. | Pendiente | Baja | Evaluar como medida complementaria; no sustituye detección ni respuesta real. |
| Cerraduras | Preventivo; protege espacios y activos físicos. | Pendiente | Alta | Revisar puertas, ventanas, almacén, oficina, telecomunicaciones y administración de llaves; probar el proceso de baja de accesos. |
| Detección y prevención de incendios | Detectivo/preventivo; reduce daño a personas, inventario e infraestructura. | Pendiente | Media | Validar equipos, mantenimiento, inspecciones, plan de evacuación y requisitos locales con responsables competentes. |

## Lista de cumplimiento y aplicabilidad

| Marco / estándar | Evaluación para el escenario | Próximos pasos / límites |
|---|---|---|
| GDPR / RGPD | **Requiere análisis de aplicabilidad.** La actividad describe ventas a clientes de la UE. Debe confirmarse si la empresa ofrece bienes a personas en la UE o monitorea su comportamiento, qué datos personales procesa y si actúa como responsable o encargado. | Mapear datos y flujos, bases y propósitos de tratamiento, derechos, proveedores, transferencias, retención, seguridad y respuesta a brechas. El artículo 33 exige al responsable notificar a la autoridad sin demora indebida y, cuando sea factible, en un máximo de 72 horas desde que tenga conocimiento, salvo que sea improbable que exista riesgo para los derechos y libertades; el encargado notifica al responsable sin demora indebida. La notificación a las personas se rige por condiciones distintas del artículo 34. |
| PCI DSS | **Relevante; alcance por determinar.** La actividad indica que la empresa acepta pagos en línea y en tienda. El alcance depende de si almacena, procesa o transmite datos de titulares/autenticación de tarjeta, o si sus sistemas pueden afectar al entorno de datos de tarjetas. | Documentar flujos, terminales, comercio electrónico, proveedor de pagos, segmentación y responsabilidades compartidas. Confirmar obligaciones de validación con adquirente/marca de pago. No afirmar conformidad por tener controles individuales. |
| SOC 1 | **Condicional; no es una ley general.** Puede ser relevante si clientes o partes interesadas necesitan aseguramiento sobre controles de una organización de servicios pertinentes a la información financiera. | Determinar si Botium Toys brinda servicios que afectan el control financiero de clientes o si necesita evaluar informes de proveedores. Delimitar propósito y audiencia. |
| SOC 2 | **Condicional; no es una certificación legal universal.** Puede apoyar la comunicación de controles de una organización de servicios frente a criterios de servicios de confianza. | Evaluar demanda de clientes, contratos y proveedores. Si se busca un examen, definir sistema, periodo, criterios, alcance y auditor independiente competente. No presentar un SOC report de proveedor como prueba automática de cumplimiento propio. |

## Resultado y seguimiento

La hoja didáctica identifica brechas en controles administrativos y técnicos, y mejoras físicas; solo el firewall aparece como existente. Antes de cerrar un hallazgo en una organización real, solicitar evidencia apropiada: políticas aprobadas, inventarios, configuraciones, registros, tickets de acceso, resultados de recuperación, cobertura de endpoints, contratos, diagramas de flujo y registros de inspección.

| ID | Acción | Prioridad sugerida | Responsable | Evidencia de cierre |
|---|---|---|---|---|
| BT-01 | Confirmar inventario de activos, propietarios, datos tratados y límites del CDE. | Alta | TI / Seguridad / Pagos | Inventario y diagramas aprobados |
| BT-02 | Revisar privilegios, cuentas de proveedores y bajas de usuarios. | Alta | TI / RR. HH. | Muestreo de accesos y aprobaciones |
| BT-03 | Implementar y probar respaldos y recuperación. | Alta | Operaciones TI | Informe de restauración y objetivos documentados |
| BT-04 | Validar cifrado, gestión de claves y protección de datos. | Alta | Seguridad / Ingeniería | Revisión de configuración y excepciones aprobadas |
| BT-05 | Asegurar monitoreo, alertas y respuesta de endpoints/red. | Alta | Operaciones de Seguridad | Prueba de alerta y evidencia de atención |
| BT-06 | Formalizar plan de respuesta y continuidad; ejercitarlos. | Alta | Seguridad / Continuidad | Resultados de ejercicios y acciones correctivas |
| BT-07 | Evaluar controles físicos y mantenimiento del sistema de incendios. | Media/alta | Instalaciones | Inspección, registros y cierre de brechas |
| BT-08 | Completar evaluación de aplicabilidad GDPR y alcance PCI DSS. | Alta | Privacidad / Pagos / Legal | Análisis documentado y validación correspondiente |

## Referencias

[1]: https://github.com/ChrisJabb21/Botium-Toys-Internal-Security-Audit "Ejemplo público de auditoría Botium Toys de un estudiante"
