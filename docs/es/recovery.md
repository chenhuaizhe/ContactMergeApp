# Copia de seguridad, deshacer e historial de recuperación

- **Resumen e idiomas**: [Resumen en español](../readme/README.es.md) | [English Overview](../../README.md)
- **Guías**: [Inicio rápido](quick-start.md) | **Copia de seguridad y recuperación** | [Permisos y solución de problemas](permissions-troubleshooting.md) | [Preguntas frecuentes (FAQ)](faq.md)
- **Idioma / Language**: **Español** | [English](../en/recovery.md)

Esta guía explica las prácticas recomendadas de copia de seguridad antes de fusionar, cómo funcionan la opción de deshacer y la recuperación local en **ContactMerge+ Cleaner**, y los límites que conviene conocer antes de fusionar contactos.

## Copia de seguridad independiente antes de fusionar

- **Exportación opcional a `.vcf`**: Exportar un archivo `.vcf` (vCard) es opcional; ContactMerge+ Cleaner no te obliga a exportar un archivo antes de fusionar.
- **Copia de seguridad independiente y fechada recomendada**: Se recomienda encarecidamente conservar una copia de seguridad independiente y con fecha antes de fusionar, especialmente antes de tu primera limpieza o de una fusión por lotes. ContactMerge+ Cleaner no ofrece un servicio de copia de seguridad en la nube del desarrollador ni exporta automáticamente archivos externos de respaldo.
- **Comprueba qué cubre tu copia de seguridad**: Asegúrate de que tu respaldo cubra la cuenta de origen real donde están guardados tus contactos (como iCloud o Google, y no una cuenta vacía) e incluya la cantidad de contactos y los datos que esperas. La sincronización de cuentas no equivale a una copia de seguridad independiente, porque los cambios realizados durante la limpieza pueden sincronizarse con tus demás dispositivos conectados.
- **Evita intentos de restauración destructivos**: No vuelvas a importar archivos `.vcf` repetidamente ni realices una restauración completa del dispositivo a ciegas para corregir un problema menor de contactos; hacerlo puede multiplicar los duplicados o sobrescribir ediciones más recientes.
- **Lecturas adicionales**: Consulta [Backup Contacts Before Merge on iPhone (en inglés)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) y [How to Merge Contacts Safely (en inglés)](https://contactmerge.app/guides/merge-contacts-safely).

## Comprueba y guarda las Notas en la app Contactos de Apple

Las Notas importantes de los contactos no principales (las demás tarjetas que se fusionan en la tarjeta principal) **no** se leen ni se copian durante una fusión. Antes de confirmar cualquier fusión:

- **Revisa las Notas en la app Contactos de Apple, no en la vista previa**: ContactMerge+ Cleaner no puede leer las Notas de los contactos. Nunca asumas que un contacto no tiene Notas solo porque no aparezca ninguna en la vista previa de ContactMerge+ Cleaner; abre la app **Contactos** de Apple para revisar esas tarjetas y copia manualmente cualquier Nota importante en el contacto principal (o en otro lugar seguro) antes de fusionar.
- **Vuelve a comprobar tras salir de la app**: Si sales de ContactMerge+ Cleaner para consultar o editar contactos en la app **Contactos** de Apple, regresa después y vuelve a revisar los candidatos duplicados actuales y la vista previa de fusión antes de confirmar. No des por sentado que una lista de candidatos o una vista previa ya abierta se actualiza o lanza un nuevo escaneo automáticamente.
- **Las Notas no se pueden recuperar después**: Dado que ContactMerge+ Cleaner no puede leer las Notas, las Notas de las tarjetas no principales no pueden restaurarse más adelante mediante `Undo Last Contact Merge` ni `Recovery History`.

## Cómo revertir cambios recientes en la app

ContactMerge+ Cleaner incluye dos funciones de recuperación local en el dispositivo con límites de alcance estrictos:

- **`Undo Last Contact Merge` (fusión más reciente)**:
  - Actúa únicamente sobre la última fusión individual realizada.
  - **Ubicación verificada en pantalla**: Para buscar la opción de deshacer tras tu última fusión, abre o regresa a la pantalla de resultados de escaneo `Duplicate Contacts` y revisa cerca de la parte superior de la pantalla, encima de la sección `Ready to merge`, en busca de `Undo Last Contact Merge`.
  - **Advertencias de verificación y versión**: Esta ubicación del control se ha verificado a partir de la captura en simulador de la versión en inglés con fecha `2026-11-03`, y no mediante una prueba en vivo de la versión que tengas instalada (sin afirmar cómo luce la interfaz en tu versión actual). Los textos y el diseño pueden variar según la versión de la app o de iOS, y esta guía no afirma en qué momento exacto está habilitado el control durante tu sesión, ni que se haya probado en vivo la reversión completa en tu compilación, ni que se revierta cada propiedad interna del contacto (tampoco presupone un cuadro de confirmación específico).
- **`Recovery History` (historial de recuperación)**:
  - Utiliza un registro de recuperación local guardado por la app en tu iPhone.
  - Conserva **como máximo 3 registros de fusión y como máximo 3 registros de eliminación** (son límites independientes por tipo de acción, no una garantía de que haya 6 registros disponibles en todo momento).
  - Las entradas permanecen en el dispositivo durante **unos 30 días**; las entradas más antiguas o las desplazadas al superar el límite de 3 registros de ese tipo de acción no se pueden restaurar.
  - **Ruta de navegación no verificada**: El punto de entrada, la navegación por pantallas y los pasos de selección de registros para `Recovery History` no aparecen en las capturas aprobadas, por lo que esta guía marca la ruta de navegación como no verificada en lugar de adivinar nombres de menús para la versión que tengas instalada. Si no logras localizar `Recovery History`, contacta con el [Soporte oficial (en inglés)](https://contactmerge.app/support).

## Límites importantes de la recuperación en el dispositivo

Ten presente lo que `Undo Last Contact Merge` y `Recovery History` **no** ofrecen:

- **No es una restauración completa del sistema**: Las Notas de los contactos no se pueden leer ni restaurar desde tarjetas no principales, y es posible que los identificadores originales del sistema y los enlaces entre contactos no se restauren. La app tampoco puede reparar daños previos arbitrarios en la agenda causados por otras herramientas o importaciones.
- **Sin copia en la nube del desarrollador; independiente de la sincronización de cuentas y de las copias del sistema**:
  - El procesamiento de contactos y el registro de recuperación permanecen en tu dispositivo dentro de la app; el desarrollador no sube tu agenda a sus servidores ni ofrece un servicio de respaldo en la nube.
  - **La sincronización de cuentas y las copias de iOS son independientes**: La sincronización de contactos de iOS o de cuentas (como iCloud o Google) y las copias de seguridad del sistema o del dispositivo son mecanismos separados controlados por tus propios ajustes de cuenta y de iOS. Esta documentación **no** promete que una fusión quede al margen de la sincronización con iCloud o Google, ni promete si las copias de seguridad del sistema incluyen o excluyen los datos de la app.
  - La recuperación no está garantizada si desinstalas la app o si pierdes o cambias tu iPhone.
- **Precaución conservadora si los contactos se editan después**: Como recomendación conservadora de seguridad —no como un bloqueo estricto verificado dentro de la app—, no se puede garantizar la recuperación si los contactos afectados fueron editados o sobrescritos por sincronización posteriormente (en la app **Contactos** de Apple, en otra app, en otro dispositivo o mediante sincronización de cuentas). Evita editar los contactos fusionados si aún podrías querer deshacer esa fusión.
- **Nunca intentes solucionar problemas eliminando contactos de origen ni quitando cuentas**: Eliminar contactos almacenados en una cuenta sincronizada de correo o en la nube puede borrarlos de forma permanente en todos tus dispositivos (consulta la [advertencia sobre eliminación de contactos de Apple (en inglés)](https://support.apple.com/en-us/111793) y la [guía de administración de cuentas de Apple (en inglés)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). No toques `"Delete from My iPhone"` (eliminar del iPhone), no desactives ni vuelvas a activar la sincronización de cuentas ni elimines cuentas para solucionar un problema con una fusión; si tienes dudas, detente y consulta primero con soporte.

## Cómo solicitar soporte de forma segura

- Escribe a través del [Soporte oficial (en inglés)](https://contactmerge.app/support) indicando tu versión de ContactMerge+ Cleaner, tu versión de iOS, si estás viendo una pantalla de Contactos de Apple o una pantalla de ContactMerge+ Cleaner, el tipo de cuenta implicado (como iCloud o Google, sin compartir el identificador de tu cuenta) y qué esperabas que ocurriera frente a lo que sucedió.
- **Protege tu privacidad**: Nunca publiques listas de contactos, archivos `.vcf`, contraseñas, datos de pago ni recibos de compra en reportes o consultas públicas (Issues). Oculta todos los nombres reales, números de teléfono, correos electrónicos, fotos, direcciones postales, notas e identificadores antes de compartir cualquier captura de pantalla, o utiliza únicamente datos de demostración ficticios.

## Enlaces relacionados

- [Inicio rápido: escanear y fusionar contactos de forma segura](quick-start.md)
- [Permisos y solución de problemas](permissions-troubleshooting.md)
- [Preguntas frecuentes (FAQ)](faq.md)
- [Sitio web oficial (en inglés)](https://contactmerge.app)
- [Política de privacidad (en inglés)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Estado de la documentación

Revisado el 8 de noviembre de 2026. Las pantallas, las etiquetas y el comportamiento pueden variar según la versión instalada de la app y la versión de iOS.
