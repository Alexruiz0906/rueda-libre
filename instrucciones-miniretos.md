Contexto MINIRETO 2

El prototipo fue aprobado, pero el Play CDN no sirve para producción. El líder técnico pide montar el proyecto con la CLI y empezar la librería de componentes por los botones: uno principal, uno secundario y uno de contorno.

Objetivo

Configurar Tailwind con la CLI, verificar cómo se generan las clases y construir el componente botón con sus estados.

PASOS
Instrucciones
Dentro de nocturna/, instala Tailwind y su CLI con npm (necesitas Node.js), crea src/input.css con la importación de Tailwind y un archivo .gitignore que excluya la carpeta node_modules/.
Ejecuta la CLI desde nocturna/ en modo observación para generar src/output.css. Crea nocturna/index.html enlazando ese archivo y lleva allí la sección principal del prototipo.
Busca en output.css una clase que usas y otra que no usas (por ejemplo, bg-pink-500). Registra en la bitácora qué encontraste y por qué ocurre.
Construye las tres variantes de botón con estados hover y focus visibles. Si quitas el contorno de foco del navegador, reemplázalo por un anillo visible.
Prueba los botones con el teclado.
Haz commit y push incluyendo src/output.css (GitHub Pages no ejecuta la CLI), pero no node_modules.
REQ.
Requisitos técnicos
Node.js, npm, tailwindcss y @tailwindcss/cli; @import "tailwindcss" y la opción --watch.
.gitignore.
Variantes hover: y focus:; utilidades ring-*, rounded-*, shadow-*, espaciado y colores.
Contexto

Estas son las rutas de la campaña. Todas salen de la sede de Rueda Libre e incluyen bicicleta, casco, luces LED, chaleco reflectivo y guía:

Ruta

Distancia

Duración

Nivel

Precio

Luces del Centro

10 km

2 h

Fácil

$55.000

Miradores de la Ciudad

16 km

3 h

Medio

$75.000

Luna en Las Palmas

22 km

3,5 h

Difícil

$95.000

Objetivo

Construir una card completa con utilidades de bordes, sombras, espaciado, tipografía, colores y tamaños, reutilizando los botones del kit.

PASOS
Instrucciones
En nocturna/index.html, crea la sección "Rutas" y construye la card de la primera ruta.
Incluye una imagen con alto uniforme y ancho completo, una etiqueta de nivel, el nombre de la ruta, una lista con distancia, duración y punto de encuentro, el precio destacado y el botón principal del MiniReto 2.
Da a la etiqueta de nivel un color distinto por dificultad, sin depender solo del color: el texto también debe indicar el nivel.
Jerarquiza la lista de datos con tipografía: nombre del dato pequeño y en tono secundario, valor destacado.
Agrega un efecto al pasar el mouse sobre la card (por ejemplo, una sombra más fuerte o un borde de color) que no mueva el contenido.
Construye las cards de las otras dos rutas, una debajo de otra (la cuadrícula llega mañana). Haz commit y push.
REQ.
Requisitos técnicos
Utilidades de bordes (border, rounded-*), sombras (shadow-*), espaciado, tamaños (w-full, h-*, max-w-*), tipografía y colores.
Variante hover:; botones del MiniReto 2
Contexto

El equipo de diseño pide revisar todos los componentes en una sola página antes de armar la landing: "si el kit es consistente, la landing se arma sola". Faltan las alertas (información, éxito y advertencia) y los campos de formulario.

Objetivo

Completar el kit de componentes (botón, card, alerta e input) y reunirlo en una página de componentes publicada.

PASOS
Instrucciones
Crea nocturna/componentes.html y muestra en ella los tres botones y una card del MiniReto 3.
Construye tres alertas (información, éxito y advertencia) con fondo suave, borde lateral de color, título destacado y texto. Indica a los lectores de pantalla que la de éxito es un aviso.
Construye dos campos de formulario (correo y celular), cada uno con etiqueta visible asociada, borde, relleno, texto de ejemplo, un texto de ayuda debajo y un estado de foco visible.
Define y aplica las "reglas del kit": los mismos radios de borde, la misma escala de espaciado y los mismos colores en todos los componentes. Regístralas en la bitácora.
Publica en GitHub Pages y revisa nocturna/componentes.html en línea.
REQ.
Requisitos técnicos
Utilidades de espaciado, tamaños, colores, tipografía, bordes y sombras.
Variantes hover: y focus:.
<label> con for, atributo role.
Contexto

Con el kit aprobado, diseño entregó la estructura de la landing: encabezado (logo, enlaces a las secciones y botón "Inscríbete"), sección principal, rutas (tres cards en fila), "¿Cómo funciona?" (cuatro pasos: elige tu ruta, inscríbete, recoge tu equipo y rueda), una franja de inscripción y el pie de página.

Objetivo

Construir el layout completo de la landing con las utilidades de layout de Tailwind y los componentes del kit.

PASOS
Instrucciones
Estructura la landing con etiquetas semánticas: encabezado, contenido principal con una sección por bloque (cada una con id para las anclas) y pie.
Envuelve el contenido de todas las secciones en el mismo contenedor centrado, con ancho máximo y relleno lateral.
Construye el encabezado con flex: logo a un lado, enlaces a las secciones y botón al otro, centrados verticalmente.
Distribuye las tres cards de rutas en una cuadrícula de tres columnas y los cuatro pasos de "¿Cómo funciona?" con grid o flex (justifica tu decisión en la bitácora).
Organiza el pie en tres bloques con flex.
Copia los componentes desde componentes.html sin crear variantes nuevas. Haz commit y push.
REQ.
Requisitos técnicos
Utilidades de layout: flex, grid, grid-cols-*, gap-*, container o max-w-* con mx-auto y px-*.
justify-*, items-*; anclas con #id; etiquetas semánticas.
Contexto

La campaña se promocionará en redes sociales, así que casi todo el tráfico llegará desde celulares. Hoy la landing solo funciona bien en escritorio.

Objetivo

Adaptar la landing a móvil, tablet y escritorio con el enfoque mobile-first de Tailwind.

PASOS
Instrucciones
Revisa la landing a 360 px y anota en la bitácora todo lo que se rompe.
Reescribe las clases de layout en clave mobile-first: sin prefijo para el celular y con sm:, md: y lg: para las pantallas más grandes. Rutas: una, dos y tres columnas. Pasos: una, dos y cuatro columnas. Encabezado: apilado en el celular y en fila desde md.
Ajusta tamaños de letra y espaciados por breakpoint (por ejemplo, un título más grande desde lg y más relleno en las secciones).
En el celular, oculta los enlaces a secciones del encabezado y deja visible el botón "Inscríbete".
Prueba en modo dispositivo a 360 px, 768 px, 1024 px y 1280 px, y registra el comportamiento en una tabla en la bitácora. Haz commit y push.
REQ.
Requisitos técnicos
Prefijos sm:, md: y lg:; grid-cols-*, flex-col/flex-row, hidden, tamaños de texto y espaciado.
DevTools (modo dispositivo).
Contexto

La landing usa colores genéricos de Tailwind. El cliente quiere sus colores y sus tipografías (los mismos del sitio principal) y un color nuevo para la campaña, Amarillo Farol (#FFD166). Además, quiere que "Rueda Nocturna" se vea espectacular para quienes usan el modo oscuro.

Objetivo

Personalizar el tema de Tailwind con los colores y las fuentes de la marca, e implementar el modo oscuro.

PASOS
Instrucciones
En src/input.css, define con @theme los seis colores de la marca (los cinco del sitio más Amarillo Farol) con nombres propios, y las familias Montserrat y Open Sans. Carga las fuentes desde Google Fonts.
Reemplaza en la landing y en componentes.html todos los colores genéricos de Tailwind por los de la marca.
Agrega la variante dark: a fondos, textos, cards, bordes y campos, usando la estrategia por defecto (preferencia del sistema).
Valida con el verificador de contraste las combinaciones que usas en modo oscuro; presta atención a Verde Ruta sobre Azul Noche. Corrige las que no cumplan.
Prueba el modo oscuro emulándolo en DevTools (panel Rendering, opción prefers-color-scheme: dark) o cambiando el tema de tu sistema. Haz commit y push.
REQ.
Requisitos técnicos
@theme con variables --color-* y --font-*; utilidades generadas a partir del tema.
Variante dark:; Google Fonts.
Contraste WCAG; DevTools (emulación del modo oscuro).
Contexto

Al revisar el código, un compañero comentó: "Hay botones con quince clases repetidas en todo el HTML". Y el cliente preguntó: "¿En qué framework debería quedar la próxima versión de todo mi sitio?". Tú ya construiste con los dos, así que tienes los datos para responder.

Objetivo

Mejorar la legibilidad del HTML de la landing y justificar por escrito, con datos de tus dos versiones, el framework recomendado.

PASOS
Instrucciones
Identifica las listas de clases que más se repiten en la landing (por ejemplo, botones, etiquetas y campos) y cuenta cuántas veces aparece cada una.
Para los botones, que son un solo elemento que se repite mucho, crea clases con @apply dentro de la capa de componentes (máximo tres clases propias). Para las piezas más grandes, como las cards, mantén el marcado del kit y reutilízalo de forma consistente.
Ordena las clases de cada elemento por categoría (layout, espaciado, tipografía, color y estados).
Genera el CSS minificado de la landing agregando la opción --minify a la CLI y mide su tamaño. Compáralo con el CSS y el JavaScript de Bootstrap que carga el sitio v2.0 (DevTools, Network).
Escribe en la bitácora la comparativa Bootstrap vs Tailwind con cuatro criterios (curva de aprendizaje, personalización, tamaño final y casos de uso) apoyados en tu experiencia y tus mediciones, y una recomendación justificada para Rueda Libre. Haz commit y push.
REQ.
Requisitos técnicos
@layer components y @apply (con moderación); reutilización de componentes.
Opción --minify de la CLI; DevTools (Network, tamaño de los recursos).
Criterios de comparación: curva de aprendizaje, personalización, tamaño final y casos de uso.

---
MINIRETO 9 AL 12 Contexto

El cliente necesita recibir inscripciones hoy mismo. Datos requeridos: nombre completo, correo, celular, ruta (una de las tres), día de salida (jueves, viernes o sábado), número de acompañantes (de 0 a 3), nivel de experiencia (principiante, intermedio o avanzado), si tiene bicicleta propia (sí o no) y aceptación de las condiciones.

Objetivo

Construir en tiempo limitado un formulario semántico, accesible y validado con los componentes del kit.

PASOS
Instrucciones
Inicia un cronómetro de 40 minutos.
Crea la sección de inscripción en la landing, con su encabezado y un formulario agrupado en conjuntos de campos con título.
Elige el control adecuado para cada dato y asocia cada uno con su etiqueta.
Aplica las reglas: todo es obligatorio, el nombre tiene mínimo 3 caracteres, el celular tiene 10 dígitos y empieza por 3, y los acompañantes van de 0 a 3.
Da estilo con los campos del kit: dos columnas para los campos cortos desde md y soporte para modo oscuro.
Prueba el formulario vacío, con datos inválidos y completo, y recórrelo solo con el teclado. Registra el tiempo real en la bitácora. Haz commit y push.
REQ.
Requisitos técnicos
Repaso de semántica y formularios: <form>, <fieldset>, <legend>, <label>, tipos de <input>, <select>, opciones y casilla.
Validación nativa: required, minlength, pattern con title, min y max.
Utilidades de Tailwind: grid, md:, dark:, focus:.
Contexto

El cliente quiere que quien visite el sitio principal descubra la campaña, y que desde la landing se pueda volver al sitio y reservar una bicicleta. Hoy son dos productos que no se conocen entre sí.

Objetivo

Integrar la landing en Tailwind con el sitio en Bootstrap mediante una navegación y una identidad visual coherentes.

PASOS
Instrucciones
Inicia un cronómetro de 40 minutos.
En el sitio v2.0 (Bootstrap), agrega "Rueda Nocturna" a la navbar de las tres páginas y una cuarta diapositiva en el carrusel que lleve a la landing.
En la landing (Tailwind), haz que el logo lleve al inicio del sitio y agrega un botón "Reserva tu bici" hacia la página de reservas.
Usa rutas relativas correctas entre la raíz del repositorio y la carpeta nocturna/.
Revisa que la marca sea la misma en ambos productos: mismos códigos de color en las variables de Bootstrap y en tu @theme, mismas fuentes y los mismos datos de contacto en el pie.
Verifica todos los enlaces en local y en GitHub Pages. Registra el tiempo real. Haz commit y push.
REQ.
Requisitos técnicos
Repaso de Bootstrap: navbar, carrusel y variables --bs-*.
Repaso de Tailwind: @theme y utilidades.
Contexto

A dos días del lanzamiento, el cliente pide una sección "Planes Rueda Nocturna". Quiere destacar el plan Pareja como "Más elegido":

Plan

Precio

Incluye

Individual

$55.000 por persona

Bicicleta y casco · Luces LED y chaleco · Guía certificado · Hidratación

Pareja

$99.000 las dos personas

Todo lo del plan Individual · Foto del recorrido · Snack para dos · Prioridad en la ruta

Grupo (4 a 8)

$45.000 por persona

Todo lo del plan Individual · Guía exclusivo · Horario a elección · Fotos del grupo

Objetivo

Resolver un requerimiento nuevo aplicando box model, Flexbox y Grid con Tailwind en tiempo limitado.

PASOS
Instrucciones
Inicia un cronómetro de 45 minutos.
Crea la sección de planes con una cuadrícula de una columna en el celular y tres desde lg, con cards de la misma altura.
Organiza cada card en columna para que su botón quede siempre al final, y alinea la lista de beneficios con flex y separación uniforme.
Destaca el plan Pareja con un borde más grueso de color, un fondo diferente y una etiqueta "Más elegido" al comienzo de la card, sin mover las demás cards.
Mantén el box model coherente con el kit (relleno, bordes y separación) y comprueba en DevTools que las tres cards tienen el mismo ancho y el mismo relleno.
Asegura el modo oscuro y el contraste. Registra el tiempo real en la bitácora. Haz commit y push.
REQ.
Requisitos técnicos
Repaso de box model: relleno, borde y separación (p-*, border-*, gap-*).
Repaso de Grid y Flexbox: grid, grid-cols-*, lg:, flex, flex-col, justify-between, gap-*.
Variante dark:; DevTools (Computed).
ontexto

Es el día del lanzamiento. El director de Nodo Digital presentará el trabajo al cliente y te pide dejar todo listo y ensayar una demo corta. Lo que no esté documentado o no funcione en línea, para el cliente no existe.

Objetivo

Consolidar y entregar el ecosistema Rueda Libre (sitio v2.0 y landing Rueda Nocturna) validado, documentado, publicado y listo para demostrar.

PASOS
Instrucciones
Ejecuta la lista de verificación final en ambos productos: estructura semántica, accesibilidad (texto alternativo, encabezados, contraste y teclado), formularios validados, responsive a 360, 768 y 1280 px, modo claro y oscuro en la landing, cero errores 404, sin estilos en línea y output.css minificado subido.
Valida con el validador del W3C la landing y la página de reservas del sitio, y corrige los errores que reporte.
Convierte tu bitácora en un README.md que incluya: descripción del proyecto, enlaces publicados, páginas, tecnologías, recomendación de framework (MiniReto 8), capturas (escritorio, celular y modo oscuro), aprendizajes y autor.
Publica la versión final con un commit de lanzamiento y verifica todo en GitHub Pages.
Prepara una demo de tres minutos: contexto del cliente, recorrido en vivo (sitio → landing → inscripción, vista en celular y modo oscuro) y dos decisiones técnicas que tomaste. Ensáyala con cronómetro frente a un compañero y anota la retroalimentación que recibas.
REQ.
Requisitos técnicos
Validador del W3C; lista de verificación de entrega.
README.md con títulos, listas, enlaces e imágenes.

## Conventional commit sugerido (para hacerlo al finalizar)

```bash
git add nocturna/ bitacora.txt .vscode/settings.json readme.md
git status   # verifica que NO aparezca nocturna/node_modules
git commit -F - <<'MSG'
feat(nocturna): landing Rueda Nocturna con Tailwind CLI y kit de componentes

- configura Tailwind v4 con @tailwindcss/cli (scripts dev --watch y build --minify)
- agrega kit de componentes: 3 botones, card de ruta, alertas e inputs (componentes.html)
- construye la landing con header, rutas, ¿cómo funciona?, inscripción y footer
- aplica diseño mobile-first con breakpoints sm/md/lg
- define tema de marca con @theme (6 colores, Montserrat y Open Sans) y modo oscuro
- extrae botones a @layer components con @apply (btn-primario/secundario/contorno)
- incluye src/output.css minificado para GitHub Pages; ignora node_modules
- documenta en la bitácora hallazgos, contraste WCAG y comparativa Bootstrap vs Tailwind
MSG
git push origin Rueda-LibreV2.0
```

Versión corta en una línea:

```
feat(nocturna): landing Rueda Nocturna con Tailwind CLI, kit de componentes, mobile-first y modo oscuro
```


---

## Conventional commits sugeridos · MiniRetos 9 a 12

> Si ya hiciste el commit de los MiniRetos 2 a 8 (bloque de arriba), usa estos. Si vas a subir todo junto, salta al **commit único** del final.

```bash
# MiniReto 9 · formulario de inscripción
git add nocturna/index.html nocturna/src/output.css
git commit -m "feat(nocturna): formulario de inscripción con fieldsets y validación nativa"

# MiniReto 10 · integración sitio ↔ landing
git add index.html paginas/ css/styles.css
git commit -m "feat(sitio): enlaza Rueda Nocturna en navbar, carrusel y unifica marca"

# MiniReto 11 · planes
git commit -am "feat(nocturna): sección de planes con plan Pareja destacado"

# MiniReto 12 · lanzamiento
git add README.md img/capturas/ bitacora.txt
git commit -m "docs: README de lanzamiento, capturas y validación W3C"
git push origin Rueda-LibreV2.0
```

### Commit único (todo de una vez)

```bash
git add README.md bitacora.txt index.html paginas/ css/styles.css img/capturas/ nocturna/ .vscode/settings.json
git status   # verifica que NO aparezca nocturna/node_modules
git commit -F - <<'MSG'
feat: lanzamiento Rueda Nocturna integrada con el sitio Rueda Libre v2.0

- agrega formulario de inscripción con fieldsets y validación nativa (MiniReto 9)
- enlaza la landing desde la navbar y una 4.ª diapositiva del carrusel; logo y
  "Reserva tu bici" vuelven al sitio; unifica colores, fuentes y contacto (MiniReto 10)
- agrega sección de planes con grid, cards de igual altura y plan Pareja destacado (MiniReto 11)
- corrige errores del validador W3C (0 errores en 5 páginas) y agrega h1 faltantes
- agrega README.md con enlaces, tecnologías, recomendación de framework y capturas (MiniReto 12)
MSG
git push origin Rueda-LibreV2.0
```

> GitHub Pages publica desde la rama que tengas configurada (normalmente `main`). Si es así, haz merge de `Rueda-LibreV2.0` en `main` para ver los cambios en línea, y revisa ahí los enlaces.
