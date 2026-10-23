# Informe de evaluación de seguridad: [Nombre del sistema o laboratorio]

> **Clasificación:** Copia pública para portafolio — sanitizada  
> **Fecha de evaluación:** [AAAA-MM-DD]  
> **Autor/a:** [Nombre / alias]  
> **Estado:** [Borrador | Revisado | Completo]

## Resumen ejecutivo

[Explica brevemente el objetivo, la postura general, los riesgos principales y las acciones recomendadas más importantes, sin incluir información sensible.]

## Autorización y alcance

- **Referencia de autorización:** [Descripción o referencia redactada]
- **Activos dentro del alcance:** [Activos de laboratorio o sistemas aprobados; sanitiza identificadores]
- **Fuera del alcance:** [Exclusiones explícitas]
- **Ventana de evaluación:** [Inicio/fin, zona horaria]
- **Restricciones:** [Límites de frecuencia, técnicas prohibidas, restricciones de disponibilidad]

## Entorno y metodología

- **Entorno:** [SO, arquitectura, tipo de despliegue]
- **Herramientas y versiones:** [Herramienta — versión]
- **Metodología:** [Estándares o proceso utilizado]
- **Manejo de datos:** [Sintéticos/anonimizados; retención y limpieza]

## Resumen de resultados

| Severidad | Cantidad | Resumen |
|---|---:|---|
| Crítica | [0] | [Resumen] |
| Alta | [0] | [Resumen] |
| Media | [0] | [Resumen] |
| Baja / Informativa | [0] | [Resumen] |

## Hallazgos

### [HALLAZGO-001] [Título claro y conciso]

- **Severidad:** [Crítica / Alta / Media / Baja / Informativa]
- **Componente afectado:** [Identificador sanitizado]
- **Estado:** [Abierto / Aceptado / Corregido / Pendiente de nueva prueba]
- **Confianza:** [Alta / Media / Baja]

**Observación**  
[Qué se observó y cómo se validó. No publiques valores sensibles.]

**Impacto**  
[Consecuencia técnica o de negocio realista.]

**Evidencia**  
[Evidencia mínima y sanitizada. Redacta tokens, datos personales, direcciones internas y metadatos identificables.]

```text
[Agrega evidencia segura y mínima. No incluyas credenciales ni resultados sensibles sin procesar.]
```

**Mitigación**  
[Acción correctiva específica, priorizada, y guía de configuración segura.]

**Validación**  
[Cómo confirmar la corrección en un entorno autorizado.]

**Referencias**  
- [Aviso del proveedor / estándar / documentación]

## Capturas y resultados del laboratorio

<!-- Inserta solo imágenes sanitizadas. Confirma que no muestren secretos, usuarios, hosts ni datos privados. -->

![Evidencia sanitizada de la evaluación](../../assets/screenshots/REEMPLAZAR-POR-IMAGEN-SANITIZADA.png)

## Limitaciones

[Tiempo, accesos, cobertura de pruebas y otras limitaciones; indica qué no se evaluó.]

## Plan de mitigación

| Hallazgo | Acción | Responsable | Fecha objetivo | Verificación |
|---|---|---|---|---|
| [HALLAZGO-001] | [Acción] | [Rol] | [Fecha] | [Método de nueva prueba] |

## Limpieza y lecciones aprendidas

[Describe la limpieza realizada, el riesgo residual y las mejoras al proceso.]

## Apéndice: notas de reproducción segura

[Incluye pasos reproducibles solo para un laboratorio aislado o un objetivo autorizado. Agrega configuración y desmontaje del entorno; omite secretos e información sensible.]
