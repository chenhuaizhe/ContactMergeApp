# Preguntas frecuentes (FAQ)

- **Resumen e idiomas**: [Resumen en español](../readme/README.es.md) | [English Overview](../../README.md)
- **Guías**: [Inicio rápido](quick-start.md) | [Copia de seguridad y recuperación](recovery.md) | [Permisos y solución de problemas](permissions-troubleshooting.md) | **Preguntas frecuentes (FAQ)**
- **Idioma / Language**: **Español** | [English](../en/faq.md)

Respuestas prácticas para utilizar **ContactMerge+ Cleaner** de forma segura en el iPhone, con indicación del comportamiento verificado y de los límites según la versión.

## Copias de seguridad y detección de duplicados (`q01`–`q06`)

<a id="q01"></a>
### 1. ¿Necesito una copia de seguridad `.vcf` antes de fusionar o basta con `Recovery History`?

Exportar un archivo `.vcf` es opcional —la app no exige exportar uno antes de fusionar—, pero se recomienda encarecidamente conservar una copia de seguridad independiente y fechada antes de tu primera limpieza o de una limpieza grande. `Recovery History` es únicamente un registro local limitado en el dispositivo (como máximo 3 registros de fusión y como máximo 3 registros de eliminación durante unos 30 días), no puede restaurar Notas de tarjetas no principales y no cuenta con copia en la nube del desarrollador. La sincronización de cuentas (iCloud o Google) no equivale a una copia independiente porque las fusiones pueden sincronizarse entre dispositivos. Asegúrate de que tu copia cubra la cuenta real que guarda tus contactos e incluya los registros esperados, y evita reimportar archivos `.vcf` repetidamente o restaurar todo el dispositivo a ciegas. Consulta [Copia de seguridad y recuperación](recovery.md) y [Backup Contacts Before Merge on iPhone (en inglés)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. ¿Qué significa `Ready to merge` y aun así debo revisar la vista previa?

`Ready to merge` significa que cada par de tarjetas dentro del grupo superó comprobaciones estrictas basadas en indicios sólidos entre todos los pares. Aun así, abre siempre la vista previa antes de confirmar: coincidir en nombre o número de teléfono por sí solo no demuestra que dos tarjetas representen a la misma persona, y la app no puede leer las Notas de los contactos. Selecciona tu tarjeta principal, revisa la app **Contactos** de Apple por si hay Notas en las tarjetas no principales, comprueba que se conserven los campos esperados en la vista previa y luego confirma (o incluye los grupos `Ready to merge` en una fusión por lotes de Pro confirmada). Consulta [Inicio rápido](quick-start.md) y [How to Merge Contacts Safely (en inglés)](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. ¿Por qué aparece un grupo en `Needs review` y puedo fusionarlo por lotes?

`Needs review` indica indicios más débiles o contradictorios, como un número de teléfono doméstico compartido, nombres distintos, fechas de cumpleaños en conflicto o coincidencias parciales. Es una medida de protección y no un error de escaneo. Los grupos de `Needs review` deben inspeccionarse y confirmarse manualmente de uno en uno, y no pueden entrar en la fusión por lotes de Pro. Si tienes dudas o las tarjetas corresponden a personas distintas, déjalas sin fusionar. Consulta [Inicio rápido](quick-start.md).

<a id="q04"></a>
### 4. ¿Debo fusionar cuando los nombres difieren o cuando dos tarjetas tienen exactamente el mismo nombre?

Ninguno de los dos casos es automático. Las diferencias en el nombre (como un apodo frente al nombre completo) no significan automáticamente que sean personas distintas, mientras que dos nombres idénticos pueden pertenecer a dos familiares o compañeros de trabajo diferentes. Esta documentación no afirma reglas exactas de uso de mayúsculas ni de normalización de texto durante la comparación interna. En la vista previa, compara los datos que se muestran efectivamente allí (como nombres, números de teléfono y correos electrónicos cuando estén presentes), y nunca des por hecho que un campo o una Nota está vacío en la tarjeta de contacto solo porque no aparezca en la vista previa. Abre las tarjetas originales en la app **Contactos** de Apple para comprobar la empresa o empleador, otros datos adicionales de identidad y cualquier Nota que quieras conservar; si sales para consultar o editar tarjetas allí, regresa y vuelve a comprobar los candidatos actuales y la vista previa antes de confirmar (no des por sentado que las vistas abiertas se actualizan automáticamente). Consulta [Inicio rápido](quick-start.md).

<a id="q05"></a>
### 5. Dos personas distintas comparten un teléfono de casa o de oficina. ¿Qué debo hacer?

**No** las fusiones. Es habitual que familiares que comparten teléfono fijo, parejas que comparten un número de emergencia o compañeros con la misma línea principal de recepción aparezcan como candidatos, por lo general en `Needs review`. Fusionarlos combinaría a personas distintas en una sola tarjeta. Deja a las personas diferentes sin fusionar y confirma únicamente cuando todas las tarjetas del grupo representen a la misma persona. Consulta [Inicio rápido](quick-start.md).

<a id="q06"></a>
### 6. ¿Por qué unas fechas de cumpleaños distintas marcaron un grupo para revisión?

Las fechas de cumpleaños en conflicto entre tarjetas (mencionadas en registros históricos de soporte y de la versión 1.3.6 junto con los conflictos de nombre) son una señal práctica para revisar manualmente, más que un umbral algorítmico exacto publicado. Unas fechas distintas pueden indicar que dos familiares comparten datos de contacto o que hay un error de escritura en una tarjeta antigua. Revisa ambas tarjetas en la vista previa y en la app **Contactos** de Apple antes de decidir. Consulta [Inicio rápido](quick-start.md).

## Cuentas, transferencias y Contactos de Apple (`q07`–`q11`)

<a id="q07"></a>
### 7. ¿Cómo funciona la app con la sincronización de contactos de iCloud o Google?

Los contactos se procesan localmente en tu iPhone sin subirse a servidores del desarrollador y sin respaldo en la nube del desarrollador. Sin embargo, la sincronización de iCloud o Google y las copias de seguridad del sistema iOS son mecanismos independientes controlados por tus ajustes, por lo que las fusiones confirmadas pueden sincronizarse en tus dispositivos conectados. Nunca desactives y actives la sincronización, ni quites cuentas, ni toques `"Delete from My iPhone"`, ni borres contactos de origen sincronizados para solucionar problemas: eliminar contactos de cuentas de correo o en la nube puede borrarlos permanentemente en todos tus dispositivos (consulta la [guía de cuentas de Apple (en inglés)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) y la [advertencia de eliminación de Apple (en inglés)](https://support.apple.com/en-us/111793)). Identifica primero tu cuenta y haz una copia de seguridad; si tienes dudas, detente y escribe al [Soporte oficial (en inglés)](https://contactmerge.app/support). Consulta [iCloud Duplicate Contacts After Sync (en inglés)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. ¿Por qué aparecieron duplicados tras configurar un iPhone nuevo o usar Trasladar a iOS?

Configurar un iPhone nuevo, usar Trasladar a iOS (Move to iOS), importar archivos o conectar varias cuentas suele dejar a la vista duplicados antiguos procedentes de distintas fuentes; no significa que el teléfono esté defectuoso ni demuestra una única causa garantizada. Deja que terminen la migración y la sincronización inicial en segundo plano antes de escanear (esperar no garantiza por sí solo eliminar duplicados, pero evita cambios a mitad de la sincronización), haz una copia de seguridad independiente y luego revisa las vistas previas siguiendo [Inicio rápido](quick-start.md). Consulta [Duplicate Contacts After Setting Up a New iPhone (en inglés)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone) y [Move to iOS Duplicate Contacts (en inglés)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. No aparece `View Duplicates` de Apple: ¿en qué se diferencia ContactMerge+ Cleaner?

En la app **Contactos** de Apple, el aviso `View Duplicates` aparece debajo de `My Card` cuando está disponible, mientras que enlazar contactos manualmente (`Link Contacts`) unifica la vista sin fusionar las tarjetas subyacentes (y las ediciones en una tarjeta unificada pueden propagarse a las cuentas de origen; consulta la [guía sobre duplicados de Apple (en inglés)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). La ausencia de `View Duplicates` es ajena a los permisos de la app: no existe un umbral garantizado de 1000 contactos, ni un tiempo de espera fijo, ni una solución segura de fusionar todo de golpe (`Merge All`). Concede acceso a Contactos en ContactMerge+ Cleaner para escanear localmente y revisar las vistas previas. Consulta [Permisos y solución de problemas](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. ¿Pueden existir duplicados con el mismo número con y sin prefijo internacional?

Sí: una tarjeta puede guardar un número local mientras otra incluye el prefijo del país (como `+1`), algo que el aviso integrado de duplicados de Apple puede no señalar como coincidencia exacta. Sin afirmar reglas internas exactas de normalización telefónica, ContactMerge+ Cleaner te permite comparar los números completos en la vista previa de fusión. Comprueba que ambos correspondan a la misma persona y que se conserve el formato esperado antes de confirmar. Consulta [iOS View Duplicates and Country Code Formatting (en inglés)](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. ¿Puede ContactMerge+ Cleaner manejar listas grandes de contactos?

Puedes escanear agendas grandes localmente incluso cuando no aparece `View Duplicates` de Apple, revisando los resultados divididos en `Ready to merge` y `Needs review`. No obstante, la app no promete velocidades específicas de escaneo ni capacidad ilimitada. Deja que termine la sincronización en segundo plano, crea una copia de seguridad independiente y fechada, y prueba fusionando primero un solo grupo. Consulta [Permisos y solución de problemas](permissions-troubleshooting.md) y [View Duplicates Missing on a Large Contact List (en inglés)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Deshacer, historial de recuperación y Notas de contactos (`q12`–`q14`)

<a id="q12"></a>
### 12. ¿Dónde está `Undo Last Contact Merge` y qué alcance tiene?

`Undo Last Contact Merge` actúa únicamente sobre tu última fusión individual. En la captura aprobada del simulador en inglés con fecha `2026-11-03`, aparece cerca de la parte superior de los resultados de `Duplicate Contacts`, encima de `Ready to merge`. Dado que esta referencia procede de esa captura fechada en simulador y no de una prueba en vivo de tu versión instalada (sin afirmar cómo luce la interfaz de tu versión actual), su estado activo, etiquetas y avisos pueden variar, y no equivale a una restauración completa (las Notas de tarjetas no principales no se pueden restaurar y es posible que los identificadores o enlaces originales del sistema no vuelvan a su estado anterior). Consulta [Copia de seguridad y recuperación](recovery.md).

<a id="q13"></a>
### 13. ¿Cuáles son los límites de `Recovery History` y cómo se abre?

`Recovery History` guarda **como máximo 3 registros de fusión y como máximo 3 registros de eliminación** durante **unos 30 días en tu dispositivo** (límites independientes por tipo, no 6 registros garantizados). Las entradas más antiguas o que superen el cupo no se pueden restaurar, ni se garantiza la recuperación tras desinstalar la app o perder el dispositivo. **Ruta no verificada**: su punto de entrada y los pasos para elegir registros no se muestran en las capturas aprobadas, por lo que no adivinamos rutas de menús; escribe al [Soporte oficial (en inglés)](https://contactmerge.app/support) si necesitas ayuda con tu versión. Consulta [Copia de seguridad y recuperación](recovery.md).

<a id="q14"></a>
### 14. ¿Por qué revisar las Notas en Contactos de Apple y qué más limita la recuperación?

ContactMerge+ Cleaner no puede leer las Notas de los contactos: las Notas de tarjetas no principales **no** se copian al fusionar ni se pueden restaurar mediante la opción de deshacer o `Recovery History`. Que no aparezcan Notas en la vista previa nunca significa que una tarjeta no las tenga; revísalas y cópialas antes en la app **Contactos** de Apple. Si consultas o editas contactos fuera de la app, regresa y vuelve a comprobar los candidatos actuales y la vista previa (las vistas abiertas pueden no actualizarse solas). Es posible que los identificadores y enlaces del sistema no se restauren y, por precaución conservadora, editar contactos o recibir cambios por sincronización después puede impedir una recuperación limpia. Consulta [Copia de seguridad y recuperación](recovery.md).

## Gratis frente a Pro, compras y soporte (`q15`–`q18`)

<a id="q15"></a>
### 15. ¿Qué incluye la versión gratuita (Free) frente a Pro?

**Free** incluye escanear, ver todos los grupos candidatos y fusionar un grupo cada vez con hasta 3 contactos dentro de ese grupo (sin fusión por lotes de varios grupos). **Pro** es un desbloqueo de pago único en el App Store **sin suscripción**, al precio regional que muestra Apple. Pro desbloquea los grupos de más de 3 contactos y la fusión por lotes para grupos `Ready to merge` confirmados (`Needs review` se mantiene siempre de uno en uno). Consulta [Inicio rápido](quick-start.md).

<a id="q16"></a>
### 16. ¿Cómo restauro mi compra Pro?

Pro es una compra no consumible. Confirma que tu iPhone utilice la **misma cuenta de Apple (Apple Account)** con la que hiciste la compra original y revisa la guía de Apple: [If you can't find or use your in-app purchases (en inglés)](https://support.apple.com/en-us/108096). Como la ruta exacta de restauración dentro de la interfaz de la app no está verificada aquí, no adivinamos etiquetas de menús de ajustes o de actualización a Pro, no recomendamos volver a comprar ni garantizamos una restauración automática. Si Pro sigue bloqueado, contacta con el [Soporte oficial (en inglés)](https://contactmerge.app/support) o con el Soporte de Apple. Consulta [Permisos y solución de problemas](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. ¿Cómo funcionan los reembolsos de Apple y hay alguna suscripción que cancelar?

Pro es una compra de pago único, no una suscripción; no sigas instrucciones de cancelación de suscripciones para esta app. Apple gestiona toda la facturación del App Store y decide si corresponde un reembolso según el país o la región; **los reembolsos no están garantizados**. Las solicitudes de reembolso se tramitan mediante el proceso oficial de Apple en [reportaproblem.apple.com (en inglés)](https://reportaproblem.apple.com) (consulta la [guía de reembolsos de Apple (en inglés)](https://support.apple.com/en-us/118223)), y el desarrollador no puede garantizar su aprobación. Consulta [Permisos y solución de problemas](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. ¿Cómo reviso permisos, protejo mi privacidad y contacto con soporte de forma segura?

Revisa los ajustes de privacidad y contactos de iOS (en inglés, `Settings > Privacy & Security > Contacts`, cuyo nombre exacto puede variar según el idioma o la región de iOS; consulta la [guía de acceso a Contactos de Apple (en inglés)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)); el acceso limitado solo restringe la visibilidad para la app sin borrar contactos, aunque no se garantizan todos los flujos de acceso limitado. El procesamiento es local y no sube datos a servidores del desarrollador (independientemente de tu sincronización con iCloud o Google y de las copias de iOS; consulta la [Política de privacidad (en inglés)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). Al escribir al [Soporte oficial (en inglés)](https://contactmerge.app/support), indica versiones de la app y de iOS, si ves un control de Apple o una pantalla de la app, tipo de cuenta (sin ID), recuento aproximado y comportamiento esperado frente al observado; nunca publiques listas de contactos, archivos `.vcf`, datos personales reales, contraseñas ni recibos de compra. Consulta [Permisos y solución de problemas](permissions-troubleshooting.md).

## Estado de la documentación

Revisado el 8 de noviembre de 2026. Las pantallas, las etiquetas y el comportamiento pueden variar según la versión instalada de la app y la versión de iOS.
