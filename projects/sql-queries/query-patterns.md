# Patrones SQL: filtros seguros y análisis

- **Base de datos/motor:** [SQLite / PostgreSQL / MySQL y versión]
- **Conjunto de datos:** Solo sintético — [describe el generador o el origen]
- **Objetivo:** Demostrar filtros explícitos, agregación y construcción segura de consultas.

## Esquema sintético

```sql
CREATE TABLE lab_events (
    event_id INTEGER PRIMARY KEY,
    event_type TEXT NOT NULL,
    severity TEXT NOT NULL,
    created_at TEXT NOT NULL,
    source_label TEXT NOT NULL
);
```

## Ejemplos de consultas defensivas

Selecciona solo los campos necesarios y limita el intervalo de tiempo:

```sql
SELECT event_id, event_type, severity, created_at
FROM lab_events
WHERE created_at >= :start_time
  AND created_at < :end_time
  AND severity IN (:severity_one, :severity_two)
ORDER BY created_at DESC
LIMIT :row_limit;
```

Resume la cantidad de eventos por severidad:

```sql
SELECT severity, COUNT(*) AS event_count
FROM lab_events
WHERE created_at >= :start_time
  AND created_at < :end_time
GROUP BY severity
ORDER BY event_count DESC;
```

> Vincula los valores usando la API de consultas parametrizadas del controlador de base de datos. La sintaxis de marcadores varía según el controlador; nunca construyas SQL concatenando entradas no confiables.

## Notas de seguridad

- Cuando sea posible, usa una cuenta de solo lectura y con mínimo privilegio para el análisis.
- Evita `SELECT *` si solo necesitas algunas columnas.
- Valida y vincula los valores suministrados por usuarios; usa listas permitidas para identificadores que no puedan parametrizarse.
- Aplica límites de filas y tiempo para reducir la recopilación accidental de datos.
- No registres credenciales ni resultados de consulta que contengan valores sensibles.

## Resultados

- **Esperado:** [Filas o agregaciones previstas]
- **Observado:** [Resultado sintético]
- **Validación:** [Cómo se verificaron los resultados]

```text
[Agrega una salida sintética y no sensible]
```

## Capturas

![Resultado sanitizado del laboratorio SQL](../../assets/screenshots/REEMPLAZAR-POR-IMAGEN-SANITIZADA.png)

## Lecciones aprendidas

[Explica el plan de consulta, casos límite, controles de acceso y limitaciones.]
