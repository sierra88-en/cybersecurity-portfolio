# Laboratorio: permisos y propiedad de archivos en Linux

- **Fecha:** [AAAA-MM-DD]
- **Distribución/versión:** [Por ejemplo, Ubuntu 24.04 LTS]
- **Entorno:** [VM o contenedor desechable; sin sistemas de producción]
- **Objetivo:** Comprender propiedad, bits de permisos, mínimo privilegio y verificación.

## Conceptos

[Explica permisos de usuario/grupo/otros, notación simbólica y octal, acceso a directorios y la importancia del mínimo privilegio.]

## Procedimiento

Usa un laboratorio desechable. Revisa cada comando antes de ejecutarlo; los comandos privilegiados pueden alterar el acceso al sistema.

```bash
# Inspecciona la identidad y un archivo del laboratorio (reemplaza los marcadores)
id
ls -l -- ./sample.txt
stat -- ./sample.txt

# Solo como ejemplo: asigna propietario/grupo y permisos restrictivos a un archivo del laboratorio
# sudo chown <usuario-lab>:<grupo-lab> ./sample.txt
# chmod 640 ./sample.txt
```

## Verificación y resultados

- **Esperado:** [Describe propietario y acceso previstos]
- **Observado:** [Registra resultados sanitizados]
- **Comando de verificación:** `stat -- ./sample.txt`

```text
[Agrega una salida sanitizada; no incluyas usuarios ni rutas que identifiquen un sistema real.]
```

## Capturas

![Resultado sanitizado del laboratorio de permisos](../../assets/screenshots/REEMPLAZAR-POR-IMAGEN-SANITIZADA.png)

## Lecciones aprendidas y limpieza

[Qué cambió, qué podría salir mal, cómo revertirlo de forma segura y qué limpieza se realizó.]
