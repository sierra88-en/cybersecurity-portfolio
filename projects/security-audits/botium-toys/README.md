# Auditoría de controles y cumplimiento: Botium Toys

> **Tipo:** Caso de estudio académico sobre una empresa ficticia.
> **Fuente base:** PDF de alcance, objetivos y evaluación de riesgos proporcionado por el usuario.
> **Estado:** Análisis documental; no se ejecutaron pruebas técnicas independientes.
> **Uso:** Ejemplo público de portafolio, no asesoría legal ni dictamen de cumplimiento.

## Alcance y objetivos reportados

El documento adjunto define un alcance más detallado que el escenario breve: plataforma de comercio electrónico, terminales POS, red de oficinas y almacenes/distribución, y los entornos que —según ese documento— procesan, transmiten o almacenan datos de tarjetas, información personal y datos sensibles. Propone evaluar controles técnicos, organizativos y físicos, revisar PCI DSS, GDPR/RGPD y temas relacionados con SOC 1/SOC 2, y priorizar mitigaciones para la dirección de TI.[A]

El PDF además afirma que Botium Toys maneja información de salud y de menores y presenta justificaciones detalladas de fallas. Estos puntos son **afirmaciones de la fuente**, no hechos corroborados en el escenario inicial ni mediante evidencia independiente. La aplicabilidad y el inventario de datos deben verificarse con diagramas de flujo, sistemas, contratos y responsables reales antes de concluir nada.

## Resultado del checklist del PDF

El documento proporcionado evalúa 14 controles y marca 13 como no implementados y uno como implementado: el mantenimiento, monitoreo e intervención manual de sistemas heredados. Entre los controles marcados como no implementados se encuentra el firewall. Esto contradice una referencia pública secundaria consultada antes, que lo describía como existente. Para este caso del portafolio prevalece el PDF que aportaste; la discrepancia queda documentada y el estado se presenta como **reportado por el documento**, no verificado técnicamente.

Consulta la [matriz de controles y revisión de cumplimiento](CONTROLES-Y-CUMPLIMIENTO.md) para ver los 14 controles, la aplicabilidad que requiere confirmación, las acciones sugeridas y las cautelas sobre afirmaciones legales y económicas.

## Evaluación y cautelas importantes

- **NIST CSF:** El CSF sirve para organizar resultados de ciberseguridad y gestión de riesgos; no es una certificación ni, por sí solo, un estándar legal de cumplimiento.[1]
- **GDPR/RGPD:** Hay que confirmar los hechos de tratamiento y el ámbito territorial antes de concluir aplicabilidad. El artículo 33 dispone que, cuando corresponda, el responsable notifique a la autoridad sin demora indebida y, cuando sea factible, dentro de 72 horas desde que tenga conocimiento; hay excepciones y requisitos específicos. El encargado debe notificar al responsable sin demora indebida. La comunicación a las personas se analiza bajo el artículo 34, con condiciones propias.[2]
- **PCI DSS:** La pertinencia parece razonable si hay pagos con tarjeta, pero el alcance debe determinarse con los flujos de datos, sistemas, proveedores, segmentación y obligaciones de la adquirente/marca. PCI DSS es un estándar de seguridad de datos de pago, no una multa legal única cuyo importe pueda inferirse sin conocer contrato, jurisdicción y programa de cumplimiento.[3]
- **SOC 1/SOC 2:** Son informes de atestación, no leyes ni requisitos universales de que toda empresa mantenga controles para “aprobar” una auditoría SOC. Su uso depende del servicio, de las necesidades de clientes y de contratos; deben acotarse el sistema y criterios pertinentes.[4]
- **Cifrado:** No se debe traducir una recomendación de cifrado como una obligación universal de usar un algoritmo o versión de protocolo específicos en todos los activos. La selección debe basarse en el tipo de dato, arquitectura, amenazas, requisitos aplicables y gestión de claves.
- **Cifras de riesgo y sanciones:** El PDF contiene estimaciones de costo de brechas y multas. No las reproduzco como exposición financiera de Botium Toys: no se incluyen datos verificables de pérdidas, pólizas, ingresos, jurisdicción o cálculo para esta empresa ficticia. Una multa no es automática por una brecha; depende de hechos, obligaciones y proceso de la autoridad.
- **Autoridad española:** La mención de la AEPD y de la ley española no demuestra que esa autoridad sea competente para un negocio estadounidense con clientes en la UE. La autoridad competente se determina con los hechos y reglas jurisdiccionales aplicables.

## Recomendaciones ejecutivas

1. **Validar el estado y el alcance:** confirmar el inventario de activos, el flujo de pagos, el alcance del entorno de datos de tarjetas, los datos personales realmente tratados, proveedores, localizaciones y evidencia que sustenta los estados “Sí/No”. Resolver la contradicción del firewall.
2. **Reducir exposición crítica:** restringir y revisar accesos privilegiados, proteger credenciales, segmentar redes y proteger endpoints, POS y sistemas expuestos. Validar los controles mediante pruebas autorizadas.
3. **Mejorar continuidad y detección:** diseñar respaldos protegidos con pruebas de restauración, recuperación ante desastres, registro centralizado, monitoreo y respuesta a alertas. No asumir que el mantenimiento manual del legado compensa la falta de controles automáticos.
4. **Formalizar respuesta y privacidad:** crear un proceso de respuesta a incidentes que incluya clasificación, escalamiento, conservación de evidencia y análisis de notificación. Definir responsables y revisar obligaciones con asesoría competente.
5. **Priorizar con evidencia:** convertir las brechas confirmadas en un registro con riesgo, propietario, fecha objetivo, dependencias, control compensatorio y evidencia de cierre. Tratar las prioridades del PDF como propuesta, no como resultado de un cálculo validado.

## Archivos

- [Matriz de controles y cumplimiento](CONTROLES-Y-CUMPLIMIENTO.md)

## Referencias

[A]: Documento proporcionado por el usuario, *Botium Toys: Scope, Goals, and Risk Assessment Report* (PDF de 15 páginas, adjunto en esta conversación). Se usa como fuente de las afirmaciones atribuidas al caso; sus conclusiones no fueron verificadas de forma independiente.
[1]: https://www.nist.gov/cyberframework "NIST Cybersecurity Framework 2.0"
[2]: https://eur-lex.europa.eu/eli/reg/2016/679/oj "Reglamento General de Protección de Datos, artículos 33 y 34"
[3]: https://www.pcisecuritystandards.org/standards/pci-dss/ "PCI Security Standards Council, PCI DSS"
[4]: https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services "AICPA, System and Organization Controls suite"
