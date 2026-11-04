# Mockups mobile con componentes de Figma

**Session ID:** ses_e58351085ffevxQjtATFuVASj5
**Created:** 11/4/2026, 7:20:57 PM
**Updated:** 11/4/2026, 8:22:44 PM

---

## User

entra a https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=526-8&p=f&t=F8nNojFk0wi2bGLp-0 metete en la pagina components y reconstruye los wireframes de la seccion mobile redesign con los componentes a color de la seccion components, haz la reconstruccion en la pagina mockups seccion mobile

---

## Assistant

Listo. Reconstruí las **9 pantallas mobile** de **Wireframes → Mobile Redesign** en **Mockups → Mobile**, manteniendo la misma retícula, tamaño (412×917) y contenido, pero usando las instancias de la sección **Components** (versión a color).

Pantallas creadas:
- Home Page
- Search Page
- Profile Page
- Place Preview Page
- Place Info Page
- Route Info Page
- In Route Page
- Start Route Page
- Request Session Page

Cambios principales:
- Sustituí los componentes wireframe por sus equivalentes a color: `SearchBar`, `Menu Option`, `Button`, `Circle Button`, `Info Card Header`, `Review Form`, `Review`, `Accesibility check`, `Route Indicator`, `Route Info`, `Session Modal`, `Tag`, etc.
- Apliqué la paleta del sistema: morado `#613DFF`, azul `#13759F`, superficies `#EDF8FD` / `#EEEBFF` / `#F2F2F3` y blanco.
- Corregí overrides de texto e iconos, alineación de las filas y detalles como el icono de Settings y la flecha de búsqueda.
- Conservé los mapas originales de los wireframes en Home, Place Preview, In Route y Start Route.

Puedes verlo aquí:  
https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=975-1533

Nota: el `Wireframe Route Selection Panel` suelto que estaba superpuesto sobre Start Route no lo dupliqué porque es un elemento de muestra, no una pantalla. Si lo quieres como overlay real sobre Start Route, lo añado.

---

## User

si, ponlo tmb

---

## Assistant

Añadido. El **Route Selection Panel** a color queda como overlay flotante sobre **Start Route Page**, dentro de **Mockups → Mobile**, con el buscador y los dos inputs ajustados al ancho de la pantalla.

https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=975-1533

---

## User

hazme lo mismo pero con los de desktop redesign en la pagina wireframes

---

## Assistant

He reconstruido las 5 pantallas de **Desktop Redesign** con los componentes a color y las he colocado en una nueva sección **Desktop** dentro de la página **Mockups**, junto a la de Mobile.

**Sección Desktop:** [abrir en Figma](https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=1022-1766)

Qué incluye:

| Pantalla | Contenido reconstruido |
|---|---|
| **Home** | Mapa de fondo + SearchBar Variant2 desplegable («Bar», Bar Antonio, Bar Manolo, Bar Juana La Loca) + Side Option Panel coloreado |
| **Profile** | Columna de perfil con botón atrás, avatar, «Manolo» y las 3 opciones (nombre, foto, cerrar sesión) + Side Option Panel |
| **Place Preview** | Foto a sangre + sidebar con buscador, cabecera (Bar Manolo / Restaurant / 4★), placeholder «Foto bar», 2 checks de accesibilidad, botones Route/Save, formulario de reseña y 2 reseñas + Side Option Panel |
| **Route Preview** | Mapa de ruta + sidebar con Route Selection Panel (origen/destino), cabecera «Bar Manolo / Ruta», checks, botones Place/Save, formulario y reseñas + **Side Option Panel como overlay** |
| **Request Session** | Fondo morado profundo + Session Modal «Choose Method» sobre blanco + **botón circular de cierre con aspa como overlay** |

Detalles:
- Se mantienen las posiciones y el tamaño 1440×1024 originales de cada frame dentro de la sección.
- Los dos elementos sueltos del wireframe (Side Option Panel de Route Preview y Circle Button de Request Session) se han recreado como overlays.
- Los mapas y la foto se reutilizan desde los rellenos de imagen originales.
- No queda ningún nodo «Wireframe» en la sección: todo son instancias de los componentes a color (`#613DFF`, `#13759F`, `#EDF8FD`, `#EEEBFF`, `#F2F2F3`).

Si quieres, puedo ajustar densidad/espaciados de las sidebars o subir el contenido para que la segunda reseña no quede cortada por el borde inferior.

---

## User

me podrias hacer el prototipo? siguiendo el de los wireframes

---

## Assistant

¡Listo! El prototipo de la sección **Desktop** en **Mockups** ya está conectado siguiendo el comportamiento de los wireframes.

**Enlace para probarlo:**
https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=1022-1767&m=dev

(el flujo se llama **Desktop** y arranca en la Home)

---

### Interacciones creadas

**Home**
- Barra de búsqueda → Place Preview
- Los 3 resultados del desplegable → Place Preview (con hover `Horizontal hover`)
- Opciones del panel lateral: Explore / Profile → Home / Profile (con su hover)
- Opciones del menú lateral → hover de variante

**Place Preview**
- Botón atrás (círculo) → BACK, con hover
- **Route** → Route Preview (con hover)
- **Save** → hover
- Selector de accesibilidad y de método de desplazamiento → se abren (`Status=Open`)
- Campo de reseña y **Publish** → abren **Request Session** como **overlay**
- Panel lateral: Explore → Home, Profile → Profile

**Route Preview**
- Botón atrás → BACK, con hover
- **Place** → Place Preview (con hover)
- **Save** → hover
- Selectores → abiertos
- Campo de reseña y **Publish** → **Request Session** en overlay
- Panel lateral: Explore / Profile

**Profile**
- Botón atrás → BACK
- Filas del menú → hover
- «Cerrar sesión» → BACK
- Explore → Home

**Request Session (overlay)**
- Botón circular con la cruz → **CLOSE** (cierra el overlay)
- Botones del modal → hover

---

Notas: el **Side Option Panel** y la **Session Modal** reaparecen como overlay tal como en los wireframes, y los overlays se abren centrados sobre el frame actual. Lo que no pude replicar exactamente son los *cambios de variante* del login/signup del modal y el hover del panel lateral, porque esas variantes pertenecen al set de wireframes y no al set de componentes de color; ahí dejé solo el hover disponible.

¿Quieres que extienda el mismo prototipo a la sección **Mobile**?

---

## User

esta regular, pero pon el de movil y yo ya corrijo

---

## Assistant

Hecho. La sección **Mobile** de Mockups ya tiene su propio flujo de prototipo, independiente del de Desktop.

**Probar:** https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=1018-31

En el panel de Prototipo ahora hay dos flujos: **Desktop** y **Mobile** (este arranca en Home Page).

### Interacciones añadidas

**Home** → SearchBar va a Search Page; la opción *Account* va a Profile (mantiene los hovers del desplegable).

**Search** → atrás hace BACK; los 3 resultados (Bar Antonio / Bar Manolo / Bar Juana La Loca) van a Place Preview.

**Profile** → atrás hace BACK; *Cerrar sesión* hace BACK; las 3 filas mantienen hover.

**Place Preview** → SearchBar va a Search; atrás BACK; *Route* → Start Route; *Info* → Place Info; *Save* con hover.

**Place Info** → atrás BACK; los selects de accesibilidad y método se abren; *Review Form*, el campo de texto y *Publish* abren **Request Session** como overlay.

**Route Info** → atrás BACK; mismos selects, input y *Publish* → Request Session en overlay.

**In Route** → botón con la cruz hace BACK (salir de la ruta).

**Start Route** → *Go* → In Route; *Info* → Route Info; la flecha de atrás del panel hace BACK.

**Request Session** → cruz → CLOSE; Login y Sign Up solo con hover (el cambio de variante del modal no lo permite el set de componentes de color).

Los hovers que ya existían se conservaron y el flujo de Desktop sigue intacto. Si algo queda raro, dímelo y lo ajusto, o corrígelo directo en el archivo.
