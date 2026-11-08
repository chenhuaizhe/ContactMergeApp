# Permisos y solución de problemas

- **Resumen e idiomas**: [Resumen en español](../readme/README.es.md) | [English Overview](../../README.md)
- **Guías**: [Inicio rápido](quick-start.md) | [Copia de seguridad y recuperación](recovery.md) | **Permisos y solución de problemas** | [Preguntas frecuentes (FAQ)](faq.md)
- **Idioma / Language**: **Español** | [English](../en/permissions-troubleshooting.md)

Esta guía abarca los permisos de acceso a Contactos en el iPhone, en qué se diferencia **ContactMerge+ Cleaner** de las funciones de duplicados integradas de Apple, cómo manejar de forma segura las cuentas sincronizadas y las transferencias de teléfono, las dudas sobre compras y reembolsos, y cómo contactar con soporte de manera segura.

## Permiso de Contactos en el iPhone

- **Necesario para escanear y fusionar**: ContactMerge+ Cleaner necesita acceso a Contactos para detectar y fusionar duplicados en tu iPhone. El procesamiento se realiza localmente en tu dispositivo: tu agenda no se sube a servidores del desarrollador y el desarrollador no ofrece un servicio de copia de seguridad en la nube (independientemente de la sincronización de contactos con iCloud o Google o de las copias de seguridad del sistema iOS que controles desde tus propios ajustes).
- **Acceso completo frente a acceso limitado en iOS**: Según tu versión de iOS, Apple te permite controlar a qué contactos puede acceder una app —incluidos el acceso completo o el acceso limitado a contactos seleccionados— desde los ajustes de privacidad y contactos de iOS (en inglés, `Settings > Privacy & Security > Contacts`; los nombres exactos de los menús pueden variar según el idioma o la región de iOS; consulta la guía oficial de Apple: [Control access to Contacts on iPhone (en inglés)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **Si el escaneo está bloqueado o parecen faltar contactos**:
  - Revisa el nivel de permiso de Contactos concedido a ContactMerge+ Cleaner en los ajustes de iOS. Un acceso incompleto o limitado puede restringir qué contactos puede ver la app —**no** elimina tus contactos—, aunque no se garantiza que la app admita todos los flujos de acceso limitado.
  - Si la opción no aparece disponible o sigue comportándose de forma inesperada tras revisar los ajustes de iOS, contacta con el [Soporte oficial (en inglés)](https://contactmerge.app/support).
- **Qué no debes hacer**: Nunca desactives y vuelvas a activar la sincronización de cuentas, ni elimines cuentas, ni borres contactos, ni vuelvas a importar archivos `.vcf` para solucionar problemas de permisos.

## ContactMerge+ Cleaner frente a las herramientas de duplicados integradas de Apple

La app **Contactos** de Apple incluye funciones propias de detección de duplicados y enlace de tarjetas que funcionan de manera distinta a ContactMerge+ Cleaner (consulta la guía de Apple: [Merge or hide duplicate contacts on iPhone (en inglés)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)):

- **`View Duplicates` en Contactos de Apple**: Cuando está disponible, Apple muestra un aviso de duplicados (`View Duplicates`) debajo de tu tarjeta personal (`My Card`) para revisar y fusionar los duplicados detectados. Si ese aviso de Apple no aparece —por ejemplo, cuando los números usan distintos formatos de prefijo internacional o en algunas agendas grandes—, conviene distinguir ese comportamiento del sistema de un problema de permisos de la app. Esta documentación no afirma cuáles son las reglas internas de detección de Apple, ni un umbral garantizado de cantidad de contactos (como 1000 contactos), ni un tiempo fijo de espera, ni una solución general de fusionar todo de golpe (`Merge All`).
- **Contactos enlazados / vista unificada frente a tarjetas fusionadas**: Enlazar contactos manualmente (`Link Contacts`) en la app **Contactos** de Apple unifica cómo se muestran las tarjetas en una sola vista sin fusionar las tarjetas de origen subyacentes, y los cambios realizados en una tarjeta unificada pueden propagarse a las cuentas conectadas.
- **En qué se diferencia ContactMerge+ Cleaner**: ContactMerge+ Cleaner escanea localmente en tu dispositivo y separa los candidatos en `Ready to merge` y `Needs review` para que puedas inspeccionar primero una vista previa de fusión (comprobando al mismo tiempo las Notas en la app **Contactos** de Apple). No promete velocidades específicas de escaneo, límites de tamaño de agenda ni la reparación automática de daños previos en la agenda.
- Guías web oficiales relacionadas:
  - [iOS View Duplicates and Country Code Formatting (en inglés)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (en inglés)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migración, sincronización de cuentas y cómo evitar borrados accidentales

Configurar un iPhone nuevo, usar Trasladar a iOS (Move to iOS), importar archivos o conectar varias cuentas (como iCloud y Google) suele dejar al descubierto duplicados antiguos repartidos entre cuentas, sin que eso signifique que tu dispositivo falle:

- **Deja que termine la sincronización inicial y haz primero una copia de seguridad**: Espera a que finalice la migración del dispositivo o la sincronización inicial de las cuentas antes de evaluar los duplicados (esto no garantiza por sí solo que desaparezcan los duplicados, pero evita confusiones a mitad de la sincronización). Identifica qué cuenta almacena tus contactos y crea una copia de seguridad independiente y fechada antes de modificar nada.
- **Revisa con detenimiento**: Inspecciona las vistas previas de fusión (especialmente los grupos `Needs review`) y guarda primero en la app **Contactos** de Apple cualquier Nota de tarjetas no principales; si sales de la app para ver o editar contactos, regresa y vuelve a comprobar los candidatos actuales y la vista previa antes de confirmar.
- **Evitar borrados destructivos es obligatorio**: Quitar una cuenta de Contactos se comporta de forma diferente a eliminar contactos individuales, y borrar contactos de una cuenta sincronizada de correo o en la nube puede eliminarlos permanentemente en todos los dispositivos sincronizados (únicamente como contexto informativo, consulta [Add or remove accounts in Contacts on iPhone (en inglés)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) y el [aviso sobre eliminación de contactos de Apple (en inglés)](https://support.apple.com/en-us/111793)). **No** elimines contactos de origen, no toques `"Delete from My iPhone"` (eliminar del iPhone), no actives ni desactives la sincronización ni reimportes archivos `.vcf` repetidamente como atajo de limpieza; si no tienes seguridad de qué hacer, detente y consulta con el [Soporte oficial (en inglés)](https://contactmerge.app/support).
- Guías oficiales por escenario:
  - [Duplicate Contacts After Setting Up a New iPhone (en inglés)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts (en inglés)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync (en inglés)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (en inglés)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (en inglés)](https://contactmerge.app/guides/merge-contacts-safely)

## Desbloqueo Pro, restauración de compras y reembolsos

- **Pago único (sin suscripción)**: Pro es una compra única no consumible en el App Store cuyo precio regional muestra directamente Apple; **no** sigas instrucciones de cancelación de suscripciones para esta app. Desbloquea los grupos de más de 3 contactos y la fusión por lotes para grupos `Ready to merge` confirmados (`Needs review` se sigue revisando de uno en uno).
- **Restaurar Pro**: Comprueba que tu iPhone haya iniciado sesión con la **misma cuenta de Apple (Apple Account)** utilizada en la compra original y revisa la guía oficial de Apple: [If you can't find or use your in-app purchases (en inglés)](https://support.apple.com/en-us/108096). Como la ruta exacta del botón de restauración dentro de la app no está verificada en esta documentación, no adivinamos nombres de menús, no recomendamos volver a comprar Pro ni garantizamos la restauración automática; si la restauración falla, contacta con el [Soporte oficial (en inglés)](https://contactmerge.app/support) o con el Soporte de Apple.
- **Solicitudes de reembolso**: Apple gestiona la facturación del App Store y decide si una compra cumple los requisitos de reembolso según el país o la región; **los reembolsos no están garantizados**. Las solicitudes de reembolso utilizan el proceso oficial de Apple en [reportaproblem.apple.com (en inglés)](https://reportaproblem.apple.com) (consulta [Request a refund for apps or content that you bought from Apple (en inglés)](https://support.apple.com/en-us/118223)), y el desarrollador no puede garantizar su aprobación.

## Contacto con soporte y protección de tu privacidad

- **Soporte**: [Soporte oficial (en inglés)](https://contactmerge.app/support)
- **Datos útiles y seguros que puedes compartir**: Tu versión de la app ContactMerge+ Cleaner, tu versión de iOS, qué esperabas frente a lo que observaste, si la pantalla corresponde a un control del sistema de Apple o a ContactMerge+ Cleaner, el tipo de cuenta implicado (por ejemplo, iCloud o Google, **sin** incluir tu correo ni el identificador de tu cuenta) y una cantidad aproximada de contactos si resulta relevante.
- **Reglas estrictas de privacidad y ocultación de datos**:
  - Nunca subas listas privadas de contactos, archivos `.vcf` (vCard), contraseñas, datos de pago ni recibos de compra en reportes o consultas públicas (Issues) (gestiona cualquier detalle de facturación únicamente por los canales seguros oficiales de Apple o, cuando corresponda, por un canal oficial privado de soporte).
  - Oculta todos los nombres reales, números de teléfono, direcciones de correo electrónico, fotos, direcciones postales, notas e identificadores antes de compartir capturas de pantalla; usa datos de demostración ficticios siempre que sea posible.

## Enlaces relacionados

- [Inicio rápido: escanear y fusionar contactos de forma segura](quick-start.md)
- [Copia de seguridad, deshacer e historial de recuperación](recovery.md)
- [Preguntas frecuentes (FAQ)](faq.md)
- [Sitio web oficial (en inglés)](https://contactmerge.app)
- [Política de privacidad (en inglés)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Estado de la documentación

Revisado el 8 de noviembre de 2026. Las pantallas, las etiquetas y el comportamiento pueden variar según la versión instalada de la app y la versión de iOS.
