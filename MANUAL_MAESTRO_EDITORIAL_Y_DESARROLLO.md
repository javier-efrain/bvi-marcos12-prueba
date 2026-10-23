# BVI · Manual maestro editorial y de desarrollo
Versión 1.0 — 23 de octubre de 2026

**Documento operativo único para nuevos estudios de Mi Biblia Web.** Complementa, sin reemplazar, los originales del respaldo `BVI_MARCOS12_RESTAURACION_MAESTRA_V1.zip`, especialmente `GUIA_EDITORIAL.md`, `PENDIENTES_CONOCIDOS.md` y las redacciones y revisiones en `fuentes/`. Cuando haya contradicciones, no sobrescribir contenido aprobado: documentar la diferencia y consultar al propietario.

## 1. Propósito y principios
Construir una Biblia visual interactiva en español que facilite la comprensión bíblica con recursos históricos, geográficos y educativos. Fidelidad textual, histórica y arqueológica por encima del impacto estético. Distinguir hechos comprobados, reconstrucciones probables e hipótesis. La versión bíblica de referencia prevista es RVC, sujeta a licencia; el prototipo actual NO contiene una edición bíblica RVC autorizada.

## 2. Experiencia editorial aprobada
- Cada relato/estudio conserva su texto íntegro y se divide en **Contexto, Exégesis y Aplicación**.
- Las secciones se leen en páginas breves mediante **Anterior/Siguiente** y accesos directos; no convertirlas en listas verticales extensas ni resumir contenido para que entre.
- Encabezado con título, referencia y portada cinematográfica **horizontal 16:9** sin texto incrustado cuando pueda renderizarse en HTML.
- En modo visual, visor educativo **2:3** siempre accesible, con zoom, arrastre, restablecer y pantalla completa cuando corresponda.
- Alternancia **Con recursos / Solo texto** sin abandonar el capítulo. En el prototipo Solo texto oculta recursos pero muestra texto del estudio; no fingir que es el texto bíblico completo.
- Recursos junto al pasaje pertinente; infografías solo si explican algo. Evitar generar recursos decorativos por obligación.
- Diseñar primero para móvil. Respetar accesibilidad, controles comprensibles, texto alternativo y navegación por teclado.
- Mapas cuando aporten geografía real: marcadores y botones sincronizados, panel informativo, mostrar/ocultar puntos, zoom y desplazamiento sin desalinear posiciones.
- No agregar modo Devocional hasta diseñarlo y aprobarlo expresamente.

## 3. Flujo simplificado: una aprobación editorial y una integración
**Etapa A — Estudio:** redactar Contexto, Exégesis y Aplicación con el estilo ya aprobado. Verificar referencias, contexto, idiomas originales e interpretaciones controvertidas. Una revisión editorial consolidada y correcciones en bloque. Presentar al propietario para aprobación.

**Etapa B — Recursos:** comprobar primero la biblioteca existente; producir portada horizontal y un recurso 2:3 si son útiles. Revisar precisión histórica, etiquetas, ortografía y correspondencia con versículos. Presentar para aprobación. No iterar por detalles menores salvo que alteren sentido o comprensión.

**Etapa C — Integración:** preparar un único conjunto de cambios sobre una rama de trabajo en `javier-efrain/bvi-marcos12-prueba`. Mantener texto, metadatos y archivos visuales separados; actualizar manifiestos coherentemente. Nunca editar directamente `main` ni `javier-efrain/mi-biblia-web` sin autorización específica. No crear más repositorios ni utilizar Netlify Drop como circuito normal.

**Etapa D — Validación y publicación:** probar navegación, botones, imágenes, errores de consola, anchura móvil y capturas reales de escritorio/móvil. Las pruebas automatizadas no sustituyen la aprobación visual. Mostrar un único enlace de revisión; solo después de aprobación fusionar/publicar mediante GitHub. Guardar un respaldo fechado de la versión efectivamente publicada.

## 4. Biblioteca visual
Para cada recurso registrar ID único, título, tipo, libro/capítulo/versículos, período, ubicación si aplica, descripción educativa, estado de revisión, archivo original, optimizado web y fundamentos históricos. No reutilizar una portada para una escena distinta sin explicarlo. No afirmar autenticidad de monedas, edificios, personajes o paisajes hipotéticos.

## 5. Criterios mínimos de aceptación
1. Texto íntegro; títulos, referencias y paginación correctos.
2. Modos visual/solo texto funcionan sin perder la página.
3. Portada y visor con proporciones y contenido adecuados; sin imágenes rotas.
4. Sin desplazamiento horizontal de toda la página en pantallas de 390/393 px.
5. Botones Anterior/Siguiente pulsables con tacto, teclado y mouse.
6. Zoom y arrastre del recurso no impiden desplazamiento normal del documento.
7. Revisión visual de escritorio y móvil; evidencias antes de publicar.
8. Sin datos sintéticos ni material provisional presentado como definitivo.
9. Respaldos y rama principal intactos hasta autorización.

## 6. Estado y pendientes verificables (V1)
- Respaldo fiel V1: 31 archivos originales más documentación; commit `27a0cc1e57ce19716774ae4e134ca3041b768ced`.
- Seis estudios, 118 páginas: E1 17, E2 20, E3 20, E4 20, E5 20, E6 21.
- E3 carece de recurso educativo registrado; E4 tiene portada provisional idéntica a E3; E6 comparte una portada para dos escenas.
- E2 → Aplicación → página 6 produce desbordamiento horizontal móvil por referencias largas. Corregir presentación sin suprimir la fuente original.
- V2 de Codex contendría la integración posterior de E4, pero **no está disponible aquí**; no atribuir a V1 esas correcciones.
- El prototipo y el proyecto principal son distintos. El repositorio `mi-biblia-web-demo` es una demostración técnica separada; no confundir con publicación definitiva.

## 7. Política de cambios
Conservar originales y registro de modificaciones. Corregir un problema reproducible por vez, sin rediseñar componentes ya aprobados. Nunca prometer una versión publicada antes de comprobar el sitio servido. El propietario solo debería intervenir para **aprobar el estudio, aprobar recursos y aprobar publicación**; no para transportar ZIP entre herramientas.
