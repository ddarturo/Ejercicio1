# Auditoría de `ejercicio1`

**Fecha:** 2026-09-17

## Resumen

La página presenta una estructura estática clara para una tarjeta personal. El HTML usa elementos semánticos principales, la hoja de estilos está enlazada correctamente y el comportamiento JavaScript corresponde al botón de mostrar u ocultar habilidades.

## Comprobaciones realizadas

- `index.html`, `styles.css` y `script.js` existen dentro de `ejercicio1`.
- `foto.jpg` existe y coincide con la ruta usada por la imagen del HTML.
- El documento incluye `lang="es"`, `charset` y `viewport`.
- La página usa `header`, `nav`, `main`, `section` y `footer`.
- La imagen tiene un texto alternativo descriptivo.
- El botón tiene `type="button"` y un texto comprensible.
- `script.js` usa los IDs presentes en el HTML: `anio`, `toggleHabilidades` y `listaHabilidades`.
- La carga de `script.js` usa `defer`.
- `node --check ejercicio1/script.js` no presenta errores de sintaxis.

## Hallazgos

### Hallazgos altos

No se detectan hallazgos altos.

### Hallazgos medios

- El botón alterna la visibilidad de la lista, pero no actualiza `aria-expanded` ni declara `aria-controls`. Esto dificulta que un lector de pantalla comunique el estado actual del control.
- No se observan reglas responsive específicas para la navegación. En pantallas estrechas los enlaces pueden necesitar una revisión visual para evitar saltos o falta de espacio.

### Hallazgos bajos

- El uso de `Arial` funciona, aunque una fuente con mejor legibilidad podría reforzar la presentación.
- El mensaje de `console.log` en `script.js` es útil durante el desarrollo, pero puede retirarse antes de una entrega final.

## Recomendaciones

1. Añadir `aria-controls="listaHabilidades"` y mantener `aria-expanded` sincronizado con el estado de la lista.
2. Revisar la navegación en anchos de 320px, 390px y 768px.
3. Eliminar el `console.log` cuando ya no se necesite depurar.
4. Validar el HTML, el contraste y el flujo de teclado con herramientas específicas de accesibilidad.

## Conclusión

`ejercicio1` está listo para publicarse como sitio estático en GitHub Pages. No hay errores bloqueantes detectados en la revisión actual; quedan mejoras de accesibilidad y responsive recomendadas para una versión posterior.