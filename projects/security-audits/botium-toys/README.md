# Auditoría interna de seguridad: Botium Toys

> **Tipo de ejercicio:** Caso académico de una empresa ficticia  
> **Estado:** Evaluación de escritorio basada en el escenario y las hojas de trabajo disponibles; no es una auditoría de una organización real  
> **Alcance del portafolio:** Ejemplo público, sin datos reales ni evidencia técnica  
> **Marco de referencia:** NIST Cybersecurity Framework (CSF) 2.0

## Contexto y objetivo

Botium Toys es una empresa ficticia de Estados Unidos con una ubicación física que funciona como oficina, tienda y almacén. Sus ventas en línea crecieron dentro y fuera del país. El ejercicio plantea una auditoría interna para entender los riesgos para operaciones y activos, mejorar los controles y revisar requisitos relacionados con pagos y clientes de la Unión Europea.

El caso proporciona un inventario de activos administrados por TI, pero no evidencia técnica que permita confirmar cómo están configurados o funcionando. Por ello, este trabajo distingue los datos expresos del escenario de los supuestos de la lista de control. Los controles marcados «por implementar» se tratan como brechas de la hoja didáctica, no como hallazgos confirmados mediante pruebas de una empresa real.

## Alcance y activos considerados

El inventario del caso incluye equipos locales y de empleados; aplicaciones y servicios de contabilidad, telecomunicaciones, bases de datos, seguridad, comercio electrónico e inventario; acceso a Internet y red interna; acceso de proveedores; servicios de centro de datos; almacenamiento y retención de datos; lectores de credenciales; y sistemas heredados que requieren supervisión manual.

La hoja de trabajo usada como referencia menciona también como sistemas bajo revisión contabilidad, detección en endpoints, firewalls, IDS y SIEM. Antes de una evaluación real, se debe confirmar si esos componentes existen, quién los opera, dónde están alojados y cuáles procesan datos de tarjetas o datos personales.

**Fuera del alcance de este ejercicio:** pruebas activas, escaneo de sistemas reales, entrevistas con personal, revisión de configuraciones, muestreo de registros, validación de controles, análisis de contratos y determinación legal de cumplimiento. No se afirma que haya ocurrido una intrusión ni que se hayan impuesto o vayan a imponerse multas.

## Objetivos de auditoría

1. Organizar la evaluación con el NIST CSF y mejorar la gestión del riesgo cibernético.
2. Inventariar activos, datos, dependencias de terceros y sistemas heredados.
3. Identificar brechas de controles administrativos, técnicos y físicos.
4. Priorizar mitigaciones para proteger confidencialidad, integridad, disponibilidad y continuidad operativa.
5. Determinar qué análisis adicional se requiere para PCI DSS y GDPR, de acuerdo con el flujo real de datos y el papel de la empresa.

El NIST CSF 2.0 ofrece resultados de alto nivel para gestionar riesgo —Govern, Identify, Protect, Detect, Respond y Recover—; no es por sí mismo una certificación ni sustituye los requisitos legales o de PCI DSS.[1]

## Hallazgos principales del ejercicio

La lista de controles disponible como referencia secundaria indica que el firewall ya está implementado. Esa publicación es un ejemplo público de un estudiante, no la hoja oficial del curso. En ella se identifican como pendientes controles de mínimo privilegio, separación de funciones, continuidad y recuperación ante desastres, políticas de contraseñas y accesos, gestión de cuentas, IDS, cifrado, respaldos, gestión de contraseñas, antivirus y supervisión de sistemas heredados. También señala controles físicos por mejorar, como CCTV, cerraduras, gabinetes con llave para equipo de red y detección/prevención de incendios.[5]

La prioridad alta para las brechas de acceso, cifrado, respaldo y detección es razonable como prioridad inicial por su relación con cuentas, información sensible, pagos y continuidad. Sin embargo, la prioridad final debe surgir de evidencia, probabilidad, impacto, exposición, controles compensatorios y tolerancia al riesgo; no solo de la plantilla.

## Recomendaciones prioritarias

### Inmediatas: 0–30 días

- Confirmar responsables, inventario y flujos de datos. Identificar dónde se reciben, procesan, transmiten o almacenan datos de pago y datos personales; validar si el proveedor de pagos reduce el alcance PCI DSS y qué responsabilidades permanecen en Botium Toys.
- Revisar cuentas privilegiadas, cuentas de exempleados y accesos de proveedores. Retirar accesos innecesarios, aplicar mínimo privilegio y establecer revisiones periódicas con aprobación documentada.
- Crear o validar un plan de respuesta a incidentes y un procedimiento para reportar, escalar y documentar incidentes de seguridad y privacidad.
- Proteger datos sensibles con cifrado adecuado en tránsito y en reposo, gestión de claves y controles de acceso; confirmar mediante pruebas y revisión de arquitectura.
- Confirmar que los respaldos existen, están aislados o protegidos contra alteración, y pueden restaurarse. Realizar una prueba documentada de restauración.

### Corto plazo: 30–90 días

- Formalizar gestión del ciclo de vida de cuentas, autenticación robusta, políticas de acceso y separación de funciones; implementar una bóveda o administrador de secretos/contraseñas aprobado cuando aplique.
- Establecer registro centralizado y monitoreo de endpoints, red y servicios relevantes. Evaluar IDS/EDR/SIEM de acuerdo con el tamaño y capacidad del equipo, con alertas atendidas y un proceso de escalamiento.
- Mantener protección antimalware, gestión de parches, configuración segura y un plan documentado de atención para sistemas heredados y fuera de soporte.
- Aprobar un plan de continuidad y recuperación ante desastres con objetivos de recuperación, responsables, dependencias, copias de seguridad y ejercicios de prueba.
- Evaluar controles físicos de acceso, protección de gabinetes y equipos, vigilancia y detección de incendios; documentar quién revisa alertas y cómo se conserva evidencia.

### Continuo

- Mantener un registro de riesgos, excepciones, responsables, fechas objetivo y evidencia de cierre.
- Revisar contratos, accesos y controles de proveedores, incluyendo centros de datos y servicios de pago.
- Repetir evaluaciones y pruebas de eficacia después de cambios relevantes y a intervalos definidos por el riesgo.

## Cumplimiento y límites

La aplicabilidad del GDPR depende del tratamiento y del contexto; el escenario dice que la empresa vende a clientes de la UE, por lo que debe analizarse si ofrece bienes a personas en la UE o monitorea su comportamiento y qué roles de responsable/encargado asume. No basta con la ubicación de la empresa para concluir el alcance legal. Si hay una brecha de datos personales notificable, el artículo 33 establece notificación a la autoridad competente sin demora indebida y, cuando sea factible, dentro de 72 horas desde que el responsable tenga conocimiento, salvo la excepción indicada por el artículo; el encargado debe notificar al responsable sin demora indebida.[2]

PCI DSS se considera porque el escenario señala pagos en línea y en tienda. El alcance depende de si Botium Toys almacena, procesa o transmite datos de titulares de tarjeta o puede afectar la seguridad del entorno de datos de tarjetas. La marca de pago, adquirente y otros programas aplicables definen obligaciones de validación. Se requiere confirmar el flujo de pago, la segmentación, proveedores y el método de validación antes de afirmar cumplimiento.[3]

SOC 1 y SOC 2 son informes de atestación que pueden ser relevantes para generar confianza o evaluar proveedores; no deben describirse como leyes o requisitos universales. SOC 1 se relaciona con controles pertinentes al control interno sobre información financiera, mientras SOC 2 aborda criterios de servicios de confianza pertinentes para seguridad, disponibilidad, integridad de procesamiento, confidencialidad o privacidad. La necesidad de obtenerlos depende de relaciones y necesidades contractuales del negocio.[4]

## Conclusión

El escenario describe una empresa en crecimiento que debe formalizar gobierno de seguridad, inventario, acceso, protección de datos, detección y recuperación. La lista de trabajo apunta a brechas importantes, pero sin pruebas no se puede afirmar que los controles estén ausentes ni declarar incumplimiento. La acción más valiosa es validar el estado real y el alcance de datos, y luego ejecutar mitigaciones priorizadas con responsables y pruebas de eficacia.

## Archivos de este proyecto

- [Lista de verificación de controles](CONTROLES-Y-CUMPLIMIENTO.md): controles administrativos, técnicos y físicos, estado y prioridad.

El archivo de actividad aportado no incluye las hojas de trabajo enlazadas ni las cinco preguntas del curso. Por eso este entregable documenta el análisis del escenario y la lista de controles disponible públicamente, pero no responde el cuestionario ni afirma reproducir una hoja oficial completa.

## Referencias

[1]: https://www.nist.gov/cyberframework "NIST Cybersecurity Framework 2.0"
[2]: https://eur-lex.europa.eu/eli/reg/2016/679/oj "Reglamento General de Protección de Datos, artículo 33"
[3]: https://www.pcisecuritystandards.org/standards/pci-dss/ "PCI Security Standards Council, PCI DSS"
[4]: https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services "AICPA, System and Organization Controls suite" 
[5]: https://github.com/ChrisJabb21/Botium-Toys-Internal-Security-Audit "Ejemplo público de auditoría Botium Toys de un estudiante" 
