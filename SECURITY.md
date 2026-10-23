# Lista de verificación de seguridad y privacidad

Antes de cada commit o publicación, confirma lo siguiente:

- [ ] No hay contraseñas, claves de API, tokens de acceso, claves privadas, cookies ni cadenas de conexión.
- [ ] No se exponen nombres reales, correos, direcciones IP, nombres de host, registros de clientes ni otros datos identificables sin permiso explícito.
- [ ] Las capturas están recortadas y revisadas para detectar pestañas del navegador, nombres de usuario, historial de terminal, metadatos y secretos.
- [ ] Los registros, capturas de paquetes, exportaciones de bases de datos y evidencias de incidentes son sintéticos o están sanitizados de forma segura; nunca subas evidencia sin procesar.
- [ ] Los objetivos y actividades de prueba contaban con autorización explícita; no se prueban sistemas de terceros sin alcance autorizado por escrito.
- [ ] Los hallazgos evitan detalles explotables innecesarios e incluyen mitigaciones y pautas de validación.
- [ ] Se revisó el historial del repositorio: eliminar un secreto del último archivo no lo elimina del historial de Git.

Si se expone un secreto, revócalo o rótalo de inmediato. No confíes en `.gitignore` para proteger archivos que ya están bajo seguimiento. Ante una exposición pública accidental, sigue el proceso de respuesta del proveedor y, cuando corresponda, elimina los datos del historial del repositorio.

**Este repositorio es material público de portafolio. Considera que todo contenido publicado será permanentemente público.**
