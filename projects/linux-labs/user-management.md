# Laboratorio: gestión de usuarios y grupos en Linux

- **Fecha:** [AAAA-MM-DD]
- **Distribución/versión:** [Distribución y versión]
- **Entorno:** [VM o contenedor desechable]
- **Objetivo:** Practicar el ciclo de vida de cuentas, membresía de grupos y revisión de accesos.

## Notas de seguridad

Realiza este ejercicio únicamente en un laboratorio desechable con acceso de consola para recuperación. Nunca cambies ni elimines cuentas de producción siguiendo esta plantilla. No publiques usuarios reales ni bases de cuentas del sistema.

## Procedimiento

```bash
# Inspecciona la identidad actual y los grupos
id
getent group <grupo-lab>

# Comandos de ejemplo para el ciclo de vida; revísalos antes de usar.
# Las acciones privilegiadas están comentadas.
# sudo useradd --create-home <usuario-lab>
# sudo usermod --append --groups <grupo-lab> <usuario-lab>
# id <usuario-lab>
# sudo userdel --remove <usuario-lab>   # solo para una cuenta desechable del laboratorio
```

## Resultados

- **Esperado:** [Estado esperado de la cuenta y los grupos]
- **Observado:** [Resultado sanitizado]
- **Revisión de accesos:** [Explica cómo se evaluó el mínimo privilegio]

```text
[Salida sanitizada de comandos]
```

## Capturas

![Resultado sanitizado de gestión de usuarios](../../assets/screenshots/REEMPLAZAR-POR-IMAGEN-SANITIZADA.png)

## Lecciones aprendidas y limpieza

[Consideraciones del ciclo de vida de cuentas, verificación y confirmación de limpieza.]
