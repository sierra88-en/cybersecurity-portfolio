# Laboratorio: administración por consola y línea base de Linux

- **Fecha:** [AAAA-MM-DD]
- **Distribución/versión:** [Distribución y versión]
- **Entorno:** [VM aislada; con snapshot disponible]
- **Objetivo:** Revisar servicios, actualizaciones, registros y la postura básica de seguridad del host.

## Verificaciones realizadas

```bash
# Ejemplos de inspección de solo lectura
uname -a
systemctl --failed
ss -tulpen
journalctl --since "24 hours ago" --no-pager | tail -n 100
```

[Documenta el estado de actualizaciones, servicios expuestos, revisión de registros, sincronización de hora, firewall y revisión de configuración SSH, según corresponda. Sanitiza los resultados sensibles.]

## Cambios realizados

| Cambio | Justificación | Riesgo / reversión | Verificación |
|---|---|---|---|
| [Cambio] | [Motivo] | [Reversión] | [Cómo se verificó] |

## Resultados

- **Línea base:** [Resumen]
- **Cambios:** [Resumen]
- **Verificación:** [Comandos y resultado esperado]

```text
[Únicamente salida sanitizada]
```

## Capturas

![Resultado sanitizado del laboratorio de consola](../../assets/screenshots/REEMPLAZAR-POR-IMAGEN-SANITIZADA.png)

## Lecciones aprendidas y limpieza

[Documenta el impacto en servicios, consideraciones de reinicio/recuperación y restablecimiento del laboratorio.]
