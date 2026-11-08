# Inicio rápido: escanear y fusionar contactos de forma segura

- **Resumen e idiomas**: [Resumen en español](../readme/README.es.md) | [English Overview](../../README.md)
- **Guías**: **Inicio rápido** | [Copia de seguridad y recuperación](recovery.md) | [Permisos y solución de problemas](permissions-troubleshooting.md) | [Preguntas frecuentes (FAQ)](faq.md)
- **Idioma / Language**: **Español** | [English](../en/quick-start.md)

Esta guía explica cómo encontrar, revisar y fusionar contactos duplicados en tu iPhone con **ContactMerge+ Cleaner**.

ContactMerge+ Cleaner procesa tus contactos localmente en tu dispositivo, no sube tu agenda a servidores del desarrollador y no ofrece un servicio de copia de seguridad en la nube del desarrollador. (La sincronización de contactos de iOS o de tus cuentas —como iCloud o Google— y las copias de seguridad del sistema o del dispositivo son mecanismos independientes controlados por la configuración de tus propias cuentas y de iOS.) Encontrarás información del producto y enlaces de descarga en el [Sitio web oficial (en inglés)](https://contactmerge.app).

## Antes de empezar

- **Crea una copia de seguridad independiente y fechada (recomendado)**: Exportar un archivo `.vcf` (vCard) es opcional —no es obligatorio exportar uno antes de fusionar—, pero se recomienda encarecidamente conservar una copia de seguridad independiente y con fecha, sobre todo antes de tu primera limpieza. Asegúrate de que la copia cubra las cuentas reales donde están almacenados tus contactos y contenga los registros que esperas. La sincronización de cuentas (como iCloud o Google) no es una copia de seguridad independiente, ya que las fusiones pueden sincronizarse con otros dispositivos conectados. Consulta [Copia de seguridad, deshacer e historial de recuperación](recovery.md) y [Backup Contacts Before Merge on iPhone (en inglés)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Deja que terminen las transferencias y sincronizaciones iniciales**: Si acabas de configurar un iPhone nuevo, usaste Trasladar a iOS (Move to iOS) o añadiste una cuenta de correo o en la nube, espera a que finalice la sincronización en segundo plano antes de escanear y fusionar (esperar evita cambios a mitad de la sincronización, aunque por sí solo no garantiza que desaparezcan los duplicados ya existentes).

## Flujo paso a paso para fusionar contactos

1. **Concede permiso a Contactos**: Permite el acceso a Contactos cuando iOS lo solicite. Si no aparece ningún aviso o la visibilidad parece incompleta, consulta [Permisos y solución de problemas](permissions-troubleshooting.md).
2. **Escanea tu agenda**: Ejecuta un escaneo en ContactMerge+ Cleaner para ver los grupos candidatos de contactos duplicados.
3. **Abre un grupo y revisa la vista previa**: Toca un grupo de duplicados, inspecciona la vista previa de fusión (`Merge Preview`) y elige qué tarjeta de contacto debe mantenerse como contacto principal (tarjeta base).
4. **Comprueba las Notas en la app Contactos de Apple y verifica los campos antes de confirmar**:
   - Las Notas importantes de los contactos no principales (las demás tarjetas que se fusionarán) **no** se leen ni se copian en el contacto principal, y no se pueden restaurar después.
   - **Comprueba las Notas en la app Contactos de Apple, no en la vista previa**: ContactMerge+ Cleaner no puede leer las Notas de los contactos. Nunca asumas que un contacto no tiene Notas solo porque no aparezca ninguna en la vista previa de ContactMerge+ Cleaner; abre la app **Contactos** de Apple para revisar esas tarjetas y copiar cualquier Nota importante en el contacto principal antes de fusionar.
   - **Vuelve a revisar tras consultar o editar fuera de la app**: Si sales de ContactMerge+ Cleaner para ver o editar contactos en la app **Contactos** de Apple, regresa después y vuelve a comprobar los candidatos duplicados actuales y la vista previa de fusión antes de confirmar. No des por sentado que una lista de candidatos o una vista previa ya abierta se actualiza o vuelve a escanear automáticamente.
   - **Verifica la identidad y los campos esperados**: Confirma la fusión únicamente cuando las tarjetas pertenezcan claramente a la misma persona en la vida real y la vista previa conserve los campos que esperas.

### Ejemplo: resultados del escaneo y vista previa de fusión

<img src="../../assets/scan-results-demo.png" alt="Demostración en simulador con interfaz en inglés (no es una captura localizada al español; capturada el 2026-11-03) de los resultados del escaneo en Duplicate Contacts con contactos ficticios de ejemplo que muestra Undo Last Contact Merge, Ready to merge y Needs review; las pantallas y los textos pueden variar según la versión de la app o de iOS" width="420">

*Resultados del escaneo — Demostración en simulador con contactos ficticios de ejemplo (interfaz en inglés, no es una captura localizada al español; capturada el 2026-11-03). Las pantallas, el diseño y los textos pueden variar según la versión instalada de la app o la versión de iOS.*

<img src="../../assets/merge-preview-demo.png" alt="Demostración en simulador con interfaz en inglés (no es una captura localizada al español; capturada el 2026-11-03) de Merge Preview con contactos ficticios de ejemplo que muestra los motivos de coincidencia, el aviso Check and preserve notes in Contacts y la selección del contacto principal mientras la segunda fila de contacto queda debajo del área visible de desplazamiento; las pantallas y los textos pueden variar según la versión de la app o de iOS" width="420">

*Vista previa de fusión y selección del contacto principal — Demostración en simulador con contactos ficticios de ejemplo (interfaz en inglés, no es una captura localizada al español; capturada el 2026-11-03; la segunda fila de contacto queda debajo del área visible de desplazamiento, por lo que no se ven ambas tarjetas a la vez). Las pantallas, el diseño y los textos pueden variar según la versión instalada de la app o la versión de iOS.*

## Cómo entender las categorías: `Ready to merge` frente a `Needs review`

ContactMerge+ Cleaner clasifica los grupos candidatos de duplicados en dos secciones según los indicios de coincidencia disponibles (esta documentación describe hábitos seguros de revisión sin afirmar umbrales exactos de ejecución interna ni reglas exactas de normalización):

- **`Ready to merge` (listos para fusionar)**:
  - Cada par de contactos del grupo superó comprobaciones estrictas basadas en indicios sólidos entre todos los pares.
  - **Sigue siendo necesario revisar la vista previa**: Compartir nombre o número de teléfono por sí solo no demuestra que dos tarjetas correspondan a la misma persona. Revisa siempre la vista previa y comprueba si hay Notas en la app **Contactos** de Apple antes de confirmar.
  - Apto para la fusión por lotes de Pro tras tu confirmación.
- **`Needs review` (requiere revisión)**:
  - Las tarjetas presentan indicios más débiles o contradictorios; por ejemplo, un número de teléfono compartido en casa o en el trabajo, variaciones en el nombre, fechas de cumpleaños en conflicto o coincidencias parciales.
  - Ver `Needs review` es una medida de seguridad conservadora y no un error de escaneo: las diferencias en el nombre no significan automáticamente que sean dos personas distintas, mientras que un número compartido o un nombre idéntico pueden corresponder a distintos familiares o compañeros de trabajo.
  - Debe inspeccionarse y confirmarse manualmente grupo por grupo. Los grupos de `Needs review` no pueden entrar en la fusión por lotes de Pro. Si dos tarjetas representan a personas diferentes, déjalas sin fusionar.

## Funciones de la versión gratuita (Free) frente a Pro

- **Free**:
  - Escanea y consulta todos los grupos de duplicados detectados.
  - Fusiona un grupo de duplicados cada vez, con hasta 3 contactos dentro de ese grupo (no incluye fusión por lotes de varios grupos).
- **Pro**:
  - Desbloqueo de pago único en el App Store sin suscripción; Apple muestra directamente el precio regional correspondiente a tu tienda.
  - Desbloquea la fusión de grupos de más de 3 contactos y la fusión por lotes de grupos `Ready to merge` tras tu confirmación (los grupos `Needs review` siguen requiriendo revisión manual individual).
  - Ninguna de las dos versiones promete velocidades específicas de escaneo ni capacidad ilimitada de agenda.
  - Para restaurar una compra o consultar el proceso de reembolso de Apple, revisa las [Preguntas frecuentes (FAQ)](faq.md#q15) o escribe al [Soporte oficial (en inglés)](https://contactmerge.app/support).

## Guías relacionadas y soporte

- [Copia de seguridad, deshacer e historial de recuperación](recovery.md)
- [Permisos y solución de problemas](permissions-troubleshooting.md)
- [Preguntas frecuentes (FAQ)](faq.md)
- [How to Merge Contacts Safely (en inglés)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (en inglés)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Soporte oficial (en inglés)](https://contactmerge.app/support)
- [Política de privacidad (en inglés)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Estado de la documentación

Revisado el 8 de noviembre de 2026. Las pantallas, las etiquetas y el comportamiento pueden variar según la versión instalada de la app y la versión de iOS.
