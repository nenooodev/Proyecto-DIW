# Órbita 2: sistema visual de mi proyecto de diseño

## Enlaces

| Qué | Enlace |
|---|---|
| Archivo de Figma (versión "Entrega Órbita 2") |https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?version-id=2419483176312984971&node-id=745-547&p=f&t=hkdNudg5FAToqurw-0|
| Prototipo (enlace que empieza por `figma.com/proto/`) |https://www.figma.com/proto/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=1022-1767&p=f&t=hkdNudg5FAToqurw-0&scaling=min-zoom&content-scaling=fixed&page-id=975%3A1532&starting-point-node-id=1022%3A1767&show-proto-sidebar=1|
| Proyecto de Google Stitch (solo si lo has usado) |Desktop: https://stitch.withgoogle.com/projects/10305205798995987055
Móvil: https://stitch.withgoogle.com/projects/20239359341740460
|

## Dónde está cada cosa en Figma

| Entregable | Página y sección del archivo |
|---|---|
| Inventario de decisiones |Las decisiones generales del proyecto están explicadas en comentarios situados en la página de la guía de estilo|
| Wireframes rediseñados con sus notas |Las decisiones de rediseño de wireframes están en la página wireframes, sección mobile y desktop redesign junto con anotaciones enlazadas a cada cambio (ver con Shift+Y)|
| Componentes |Página components|
| Mockups del happy path |Página mockups|
| Pantalla principal en el segundo ancho |Página mockup sección mobile junto al frame de nombre Home Page|
| Pantallas en modo oscuro |Cambiar el modo a Dark en las pantallas de la pagina de mockups|
| Guía de estilo |Pagina guia estilo|

## Lista de comprobación de Figma

- [X] Variables en dos colecciones (primitivos y semánticos), con alias, modos claro y oscuro, ámbito, descripción y sintaxis de código.
- [X] Estilos de texto, efecto y retícula vinculados a las variables.
- [X] Componentes con Auto layout, variables, propiedades y variantes de estado.
- [X] Mockups construidos enteros con Auto layout y espacios sacados de variables.
- [X] Pantalla principal en un segundo ancho, con los mismos componentes.
- [X] Modo oscuro aplicado con el selector de modo.
- [X] Prototipo que recorre el happy path completo.
- [X] Prueba 1 superada: al cambiar `color/primary`, cambian todas las pantallas a la vez.
- [X] Prueba 2 superada: con todos los mockups en modo oscuro, nada desaparece contra el fondo.

## Resumen de decisiones

### Rediseño de los wireframes
Qué pantallas has cambiado, cuál es el cambio más importante y por qué (con tu persona o un principio de los apuntes).

No he cambiado ninguna pantalla entera, si no que he hecho pequeños cambios en componentes y distribución (basándome en algunos cambios que hizo Stitch que me gustaron). Algunos afectan solo algunas pantallas, otros son más globales, pero diría que el cambio más importante que he hecho es de tamaños, en mis wireframes originales era todo muy pequeño y ahora todo lo interactuable mide al menos 44 x 44px y en cuanto al texto, es de 14px como muy pequeño, todo basándome en la información de los apuntes

### Color
Color principal y secundario, y por qué los elegiste. Pareja de texto y fondo con el contraste más bajo de tu sistema y su valor, en cada modo.

Esto está más detallado en los comentarios de la guia de estilo, pero basicamente mi proyecto se compone de una paleta análoga de azules (#613DFF primario y #13759F secundario) porque creo que los azules son colores que como sociedad asociamos a la movilidad reducida, y me pareció buena idea crear la estética de la app con esa idea en mente, el primario es más saturado (para destacar) y el secundario es un azul más pensado para complementar con los neutros.

Mi contraste más bajo de texto es entre un fondo #EEEBFF y un texto #613DFF en claro (4.96:1) y en modo oscuro entre #13759F y #5A5959 (4.91:1) 

### Tipografía
Familias y pesos que usas, y por qué esas familias para tus personas.

Uso la Merriweather Sans y Er Mukta, de nuevo, lo detallo mejor en la guía de estilo, pero básicamente buscaba algo elegante y simple, evitando coger fuentes por ejemplo monoespaciadas ya que al estar una parte de mi app dirigida a personas mayores no estaba seguro de si un estilo de fuente así podria dificultarles la lectura, entonces fontjoy me sugirió estas familias y me cuadraron muy bien con esta idea.

### Espaciado y retícula
Base de la escala (4 u 8 píxeles), columnas, medianil y margen de la retícula del dispositivo de tu persona principal.
base 4, 12 columnas escritorio (16 de margen y 24 medianil) y 4 en movil (16 de margen y medianil), 
### Componentes
Lista de componentes con sus variantes de estado.

### Responsive y modo oscuro
Qué tuviste que ajustar al pasar la pantalla principal al segundo ancho, y qué corregiste en tus variables al pasar los mockups a modo oscuro.
Realmente me servía con el auto-layout que tenía ya aplicado hace tiempo, mi pantalla principal es bastante simple, con una searchbar, el mapa y un footer, de todas formas para que conste en el proyecto, he probado lo de añadir modos.
En los modos oscuros he dejado un poco más de lado los azules y he aplicado colores más neutro en general. Esto también lo explico mejor en la guia de estilo
## Uso de IA
Resumen en dos o tres frases de cómo has usado la IA en la órbita (o "no he usado ninguna herramienta de IA"). El detalle está en el [CHANGELOG.md](CHANGELOG.md).
He usado la IA sobre todo para gestionar el proyecto (desvincular componentes ya creados en los wireframes, recuperar capturas a color del mapa, revision de variables o redacción de guia de estilos, por ejemplo) nunca sobre el diseño directamente
## Lo que ha quedado pendiente
Lo que no has terminado o sabes que no funciona del todo, y por qué. Si está todo terminado, indícalo.
Lo fundamental para entregar está, todas las páginas son responsive con auto-layout, todo en variables, la guia de estilos con los 4 apartados y las pruebas al 200% y de contraste e incluso la prueba que he mencionado con los modos, mi intención era meter más inteactividad en los prototipos, pero están entregables
