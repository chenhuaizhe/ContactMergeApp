# ContactMerge+ Cleaner — Documentación del producto y soporte

Documentación pública oficial del producto y guías de soporte para **ContactMerge+ Cleaner** en iPhone. Este repositorio contiene únicamente documentación para usuarios; no es un repositorio del código fuente de la aplicación.

ContactMerge+ Cleaner procesa tus contactos localmente en tu dispositivo, no sube tu agenda a servidores del desarrollador y el desarrollador no ofrece un servicio de copia de seguridad en la nube. (La sincronización de contactos de iOS o de tus cuentas —como iCloud o Google— y las copias de seguridad del sistema o del dispositivo son mecanismos independientes controlados por la configuración de tus propias cuentas y de iOS.)

- **Sitio web**: [Sitio web oficial (en inglés)](https://contactmerge.app)
- **App Store**: [Descargar en el App Store (en inglés)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Soporte**: [Soporte oficial (en inglés)](https://contactmerge.app/support)
- **Idiomas**: [English](../../README.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | **Español** | [Português (Brasil)](README.pt-BR.md) | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [繁體中文](README.zh-Hant.md)

## Inicio rápido en 4 pasos

1. **Haz una copia de seguridad y concede permiso a Contactos**: Conserva una copia de seguridad independiente y con fecha antes de realizar limpiezas importantes (la exportación a `.vcf` es opcional), deja que termine cualquier transferencia de teléfono o sincronización inicial y permite el acceso a Contactos cuando iOS te lo solicite.
2. **Escanea**: Ejecuta un escaneo para detectar posibles grupos de contactos duplicados en tu iPhone.
3. **Revisa la vista previa, elige el contacto principal y comprueba las Notas en Contactos**: Abre un grupo de duplicados, revisa la vista previa de fusión (`Merge Preview`), selecciona el contacto principal que se conservará como tarjeta base y consulta la app **Contactos** de Apple para comprobar si hay Notas que quieras guardar.
4. **Vuelve a comprobar y confirma con cuidado**: Si saliste de la app para ver o editar contactos en la app **Contactos** de Apple, regresa y vuelve a revisar primero los candidatos duplicados actuales y la vista previa. Confirma únicamente cuando las tarjetas pertenezcan claramente a la misma persona y la vista previa conserve los campos que esperas.

<img src="../../assets/scan-results-demo.png" alt="Demostración en simulador con interfaz en inglés (no es una captura localizada al español; capturada el 2026-11-03) de los resultados del escaneo en Duplicate Contacts con contactos ficticios de ejemplo que muestra Undo Last Contact Merge, Ready to merge y Needs review; las pantallas y los textos pueden variar según la versión de la app o de iOS" width="420">

*Demostración en simulador con contactos ficticios de ejemplo (interfaz en inglés, no es una captura localizada al español; capturada el 2026-11-03). Las pantallas, el diseño y los textos pueden variar según la versión instalada de la app o la versión de iOS.*

## Límites de seguridad clave

- **`Ready to merge` frente a `Needs review`**:
  - `Ready to merge` (listos para fusionar) significa que cada par de contactos dentro del grupo superó comprobaciones estrictas de coincidencia basadas en indicios sólidos entre todos los pares. Aun así, revisa siempre la vista previa antes de confirmar: compartir el mismo nombre o número de teléfono por sí solo no demuestra que dos tarjetas correspondan a la misma persona.
  - `Needs review` (requiere revisión) indica indicios más débiles o contradictorios (como un número de teléfono familiar compartido, nombres distintos, fechas de cumpleaños en conflicto o coincidencias parciales). Es una medida de seguridad y no un error; inspecciona cada grupo de `Needs review` manualmente de uno en uno (no pueden incluirse en la fusión por lotes de Pro) y nunca fusiones tarjetas que representen a personas distintas.
- **Comprueba y guarda las Notas en la app Contactos de Apple antes de fusionar**:
  - Las Notas de los contactos no principales (las demás tarjetas que se van a fusionar) **no** se leen ni se copian en el contacto principal, y no se pueden recuperar más adelante.
  - Dado que ContactMerge+ Cleaner no puede leer las Notas, nunca des por hecho que un contacto no tiene Notas solo porque no aparezcan en la vista previa de fusión. Revisa y copia las Notas importantes directamente en la app **Contactos** de Apple antes de fusionar; si consultas o editas contactos allí, vuelve a ContactMerge+ Cleaner y revisa de nuevo los candidatos duplicados actuales y la vista previa antes de confirmar (no des por sentado que las vistas abiertas se actualizan automáticamente).
- **Deshacer y recuperación local en el dispositivo**:
  - `Undo Last Contact Merge` (deshacer la última fusión de contactos) actúa únicamente sobre la fusión individual más reciente (consulta [Copia de seguridad, deshacer e historial de recuperación](../es/recovery.md) para ver la ubicación verificada en pantalla y las advertencias según la versión).
  - `Recovery History` (historial de recuperación) es un registro local guardado por la app en el dispositivo que conserva **como máximo 3 registros de fusión y como máximo 3 registros de eliminación** durante **unos 30 días en el dispositivo** (su ruta exacta de navegación dentro de la app no está verificada en esta documentación; consulta la [Guía de recuperación](../es/recovery.md)).
  - **No es una restauración completa del sistema**: Las Notas de tarjetas no principales no se pueden restaurar, y es posible que los identificadores y enlaces originales del sistema tampoco se restauren. El desarrollador no ofrece un servicio de copia de seguridad en la nube (esto es independiente de tu propia sincronización con iCloud o Google y de las copias de seguridad del sistema iOS, por lo que las fusiones pueden sincronizarse en tus cuentas). Por precaución conservadora, la recuperación no está garantizada tras ediciones posteriores de los contactos, la desinstalación de la app o la pérdida del dispositivo.
- **Copia de seguridad independiente y seguridad de las cuentas**: Exportar un archivo `.vcf` es opcional, pero se recomienda conservar una copia de seguridad independiente y fechada que cubra las cuentas reales donde guardas tus contactos antes de tu primera limpieza (la sincronización de cuentas no equivale a una copia de seguridad independiente). Nunca elimines contactos de origen, no toques `"Delete from My iPhone"` (eliminar del iPhone) ni actives, desactives o elimines cuentas como paso para solucionar problemas.

## Gratis (Free) frente a Pro

- **Free**: Escanea tus contactos, consulta todos los grupos de duplicados y fusiona un grupo de duplicados cada vez (con hasta 3 contactos dentro de ese grupo). No incluye la fusión por lotes de varios grupos.
- **Pro**: Desbloqueo mediante pago único en el App Store, sin suscripción; Apple muestra directamente el precio correspondiente a tu región. Desbloquea los grupos de más de 3 contactos y la fusión por lotes para grupos `Ready to merge` tras tu confirmación (los grupos `Needs review` siempre se revisan de uno en uno).
- **Restauración de compras y facturación**: Para restaurar una compra Pro existente con la misma cuenta de Apple (Apple Account) o conocer el proceso de reembolso de Apple (Apple decide si procede según el país o la región mediante el proceso oficial en [reportaproblem.apple.com (en inglés)](https://reportaproblem.apple.com); la elegibilidad no está garantizada y el desarrollador no puede garantizar su aprobación), consulta las [Preguntas frecuentes (FAQ)](../es/faq.md#q16) o contacta con el [Soporte oficial (en inglés)](https://contactmerge.app/support).

## Guías de uso

- [Inicio rápido: escanear y fusionar contactos de forma segura](../es/quick-start.md)
- [Copia de seguridad, deshacer e historial de recuperación](../es/recovery.md)
- [Permisos y solución de problemas](../es/permissions-troubleshooting.md)
- [Preguntas frecuentes (FAQ)](../es/faq.md)

## Soporte oficial y privacidad

- **Soporte**: [Soporte oficial (en inglés)](https://contactmerge.app/support)
- **Privacidad**: [Política de privacidad (en inglés)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Aviso de privacidad y ocultación de datos**: Nunca compartas listas privadas de contactos, archivos `.vcf` (vCard), contraseñas, datos de pago ni recibos de compra en reportes o consultas públicas (Issues). Antes de compartir cualquier captura de pantalla, oculta todos los nombres reales, números de teléfono, direcciones de correo electrónico, fotos, direcciones postales, notas e identificadores de cuenta; utiliza datos de demostración ficticios siempre que sea posible.

## Estado de la documentación

Revisado el 8 de noviembre de 2026. Las pantallas, las etiquetas y el comportamiento pueden variar según la versión instalada de la app y la versión de iOS.
