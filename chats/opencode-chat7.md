# Variables de Figma: descripción y sintaxis

**Session ID:** ses_e4cb615f4ffe3Eg9jXlTkTMqBl
**Created:** 11/7/2026, 12:55:28 AM
**Updated:** 11/8/2026, 12:42:25 AM

---

## User

Ayudame a poner descripcion y sinaxis de codigo a las variables de mi proyecto de figma, https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=975-1532&p=f&t=vNyVkrltKMzSLMav-0 te paso unas pautas: para los colores, hazlo solo con los tokens semanticos, indicando donde se usan siguiendo los normbres (por ejemplo, on-surface-bg es el color de fondo que se utiliza encima de una superficie, on-surface color directo de una superficie, on tag el color de una etiqueta..., el codigo debera seguir la nomenclatura --color-[nombre variable] sin corchetes, en las de spacing se explican solas simplemente pon a cuantos pixeles equivale cada una, teniendo en cuenta que la base es 4x(numero variable), en cuanto a sintaxis de codigo puedes mantener los nombres originales,  las de border radius un poco lo mismo, y en las de font size pon para que se utilizan dentro del proyecto heading 1 para el display del perfil, h2 para titular secciones, h3 para titulos de cards, body para textos normales, label para textos de botones y caption para anotaciones mas pequeñas quiero que la sintaxis de codigo sea --font-(nombre variable). Que todo este escrito en ingles

---

## Assistant

Ya tengo el inventario completo. Ahora voy a aplicar las descripciones y la sintaxis de código a cada variable.

---

## Assistant

Listo. He documentado **29 variables** en el archivo: descripción en inglés + *code syntax* (CSS, plataforma WEB). Verificado leyendo de vuelta los valores.

## Colores — solo tokens semánticos
Los primitivos (`Neutral/*`, `Primary/*`, `Secondary/*`) los he dejado sin tocar, tal como pediste.

| Variable | Code syntax | Descripción |
|---|---|---|
| color-primary | `--color-primary` | Primary brand color. Used for main actions, active states, and key highlighted elements. |
| color-secondary | `--color-secondary` | Secondary brand color. Used for supporting actions and accents that complement the primary color. |
| color-surface | `--color-surface` | Surface background color. Used for cards, panels, and container backgrounds. |
| color-on-surface-text | `--color-on-surface-text` | Text color on surfaces. Used for text placed on top of the surface color. |
| color-on-surface | `--color-on-surface` | Color applied directly on a surface. Used for icons, borders, and elements that sit on the surface. |
| color-on-primary | `--color-on-primary` | Content color on primary. Used for text and icons placed on top of the primary color. |
| color-on-secondary | `--color-on-secondary` | Content color on secondary. Used for text and icons placed on top of the secondary color. |
| color-on-surface-bg | `--color-on-surface-bg` | Background color used on top of a surface. Used for nested blocks or panels inside the main surface. |
| color-tag-bg | `--color-tag-bg` | Tag background color. Used as the background of tags and labels. |
| color-star-bg | `--color-star-bg` | Star background color. Used as the background of the rating stars. |

## Spacing (base 4px)
`space-1` → `--space-1` · "4px (4 × 1)" … `space-16` → `--space-16` · "64px (4 × 16)". Valores: 4, 8, 12, 16, 24, 32, 48, 64 px.

## Border radius
`radius-none` → `--radius-none` (0px), `radius-sm` → `--radius-sm` (4px), `radius-md` → `--radius-md` (8px), `radius-lg` → `--radius-lg` (16px), `radius-full` → `--radius-full` (9999px, fully rounded).

## Font sizes
| Variable | Code syntax | Uso |
|---|---|---|
| Heading 1 | `--font-heading-1` | 32px — profile display title |
| Heading 2 | `--font-heading-2` | 24px — section titles |
| Heading 3 | `--font-heading-3` | 20px — card titles |
| Body | `--font-body` | 16px — regular body text |
| Label | `--font-label` | 14px — button text |
| Caption | `--font-caption` | 14px — smaller annotations and helper text |

Todo está en inglés. Si quieres, puedo añadir también la sintaxis para Android/iOS o cambiar el formato de las descripciones (por ejemplo, incluir el token CSS dentro del texto).

---

## User

vale, ahora en la pagina de variables en la seccion colors borra la escala que esta de los wireframes y hazme 3, una de neutral, otra de primary y otra de secondary, especificando tambien una lista de colores realmente usados (son aquellos con referencia semantica) y por ultimo hazme la tabla de contrastes de esos colores usados, que por supuesto deberan estar rellenados en figma aplicando su referencia semantica

---

## Assistant

Voy a reconstruir la sección Colors. Primero elimino la escala de wireframes y luego monto las tres escalas, la lista de tokens semánticos y la tabla de contrastes (con muestras vinculadas a las variables y modos Light/Dark).

---

## Assistant

Hecho. He reconstruido la sección **Colors** de la página *Variables (Órbita 2)*.

## Qué he cambiado

1. **Eliminada** la escala antigua "Wireframe palette" (y sus 7 rectángulos).
2. **Tres escalas nuevas**, con cada swatch vinculado a su variable primitiva y su hex:
   - **Neutral**: 100, 200, 400, 500, 600, 700, 900, 950
   - **Primary**: 50 → 950 (11 pasos)
   - **Secondary**: 50 → 950 (11 pasos)
   - Nota: "Primitive scale – not applied directly in the UI".
3. **Lista de colores realmente usados** (10 tokens semánticos), con swatch vinculado, code syntax y valores Light/Dark:
   `color-primary`, `color-secondary`, `color-surface`, `color-on-surface`, `color-on-surface-bg`, `color-on-surface-text`, `color-on-primary`, `color-on-secondary`, `color-tag-bg`, `color-star-bg`.
4. **Tabla de contrastes WCAG 2.1** para los pares semánticos usados, con **7 filas** y previsualización "Aa" en **Light y Dark**:
   - Las muestras y previews están **rellenadas con las variables semánticas** (82 propiedades de color vinculadas).
   - Los 7 previews de Light y los 7 de Dark usan **modo explícito** de la colección, así que cada uno resuelve su modo real.
   - Ratio + nivel (`AAA`/`AA`/`Pass`/`Fail`) por modo, y columna de requisito (`Text 4.5:1` o `UI 3:1`).

## Resultado de contraste

| Par | Light | Dark |
|---|---|---|
| on-surface-text / surface | 18.77 AAA | 12.08 AAA |
| on-surface-text / on-surface | 21.00 AAA | 6.98 AA |
| on-surface-text / on-surface-bg | 19.45 AAA | 6.98 AA |
| on-surface-text / tag-bg | 17.96 AAA | 21.00 AAA |
| on-primary / primary | 5.80 AA | 21.00 AAA |
| on-secondary / secondary | 5.16 AA | 14.76 AAA |
| star-bg / surface | 1.44 **Fail** | 7.52 Pass |

La fila del icono de estrella falla en Light (1.44:1); lo he dejado reflejado tal cual porque es el valor real del token. Si quieres, puedo cambiar `color-star-bg` o excluir esa fila.

También cambié el fondo de la sección a blanco para que coincida con la sección *Font sizes* y sea legible (antes tenía un degradado oscuro). La sección ha pasado de 976×542 a **976×1811**.

¿Quieres que ajuste algo: el fondo, los pares de la tabla o el token de la estrella?

---

## User

los textos de esto ponlo en español, que es mas pa entrega, lo otro era para concordar con el proyecto

---

## Assistant

Voy a traducir todos los textos visibles de la sección al español, manteniendo los nombres de tokens y la sintaxis de código tal cual.

---

## Assistant

Listo. Todos los textos visibles de la sección están ahora en español, manteniendo como identificadores los nombres de tokens (`color-primary`, etc.) y la sintaxis CSS (`--color-primary`, etc.), que no deben traducirse.

Cambios aplicados:

- Título: **Colores**
- Subtítulo: "Sistema de color semántico: escalas primitivas, los tokens usados en la interfaz y comprobaciones de contraste WCAG para cada modo."
- Escalas: **Neutral / Primaria / Secundaria**, con "Escala primitiva: no se aplica directamente en la interfaz".
- **Colores usados** + "Todos los colores aplicados en la interfaz referencian uno de estos tokens semánticos. Los valores primitivos nunca se usan directamente."
- Valores: **Claro #… / Oscuro #…**
- **Contraste** + "Ratios de contraste WCAG 2.1 para los pares semánticos de primer plano y fondo usados en la interfaz."
- Cabeceras: **Primer plano / Fondo**, **Modo claro**, **Modo oscuro**, **Requisito**.
- Requisitos: "Texto: AA 4.5:1, AAA 7:1" e "Interfaz: 3:1"; estados **Pasa / Falla**.
- Usos traducidos: texto de cuerpo, superficie elevada, superficie anidada, etiqueta de tag, texto de botón, botón secundario, icono de estrella.
- Nota final traducida.
- La sección (capa) también se llama ahora **Colores**.

Las descripciones y code syntax de las variables siguen en inglés, como pediste para concordar con el proyecto.

---

## User

pequeña correcion, el tag-bg siempre se da ocn texto en color primary

---

## Assistant

Corregido. La fila de la etiqueta ahora usa **`color-primary` como primer plano sobre `color-tag-bg`**:

| Par | Modo claro | Modo oscuro |
|---|---|---|
| `color-primary` / `color-tag-bg` | **4.96:1 · AA** | **21.00:1 · AAA** |

Cambios aplicados en esa fila:
- Swatch de primer plano y texto "Aa" re-vinculados a `color-primary`.
- Nombre actualizado a `color-primary`.
- Ratios y niveles recalculados.
- Uso renombrado a **"Texto de etiqueta"**.

El resto de la tabla y de la sección queda igual.

---

## User

te falta incluir la combinacion de colores de color-secondary y color on surface, uso esa combinacion tanto teniendo el primero de bg como de fg, intercambiandolo con el on-surface (concretamente en una variante de boton y el hover de mis menu option

---

## Assistant

Añado las dos combinaciones (secondary como fondo y como texto, intercambiándose con on-surface) a la tabla de contrastes.



---

## Assistant

Añadidas las dos combinaciones a la tabla de contrastes:

| Primer plano | Fondo | Uso | Modo claro | Modo oscuro |
|---|---|---|---|---|
| `color-on-surface` | `color-secondary` | Variante de botón | **5.16:1 · AA** | **4.91:1 · AA** |
| `color-secondary` | `color-on-surface` | Hover de menú | **5.16:1 · AA** | **4.91:1 · AA** |

- Ambas filas tienen sus swatches y previews "Aa" vinculados a las variables semánticas, con modos Light/Dark explícitos.
- La tabla pasa a 9 filas de datos y la sección crece a 976×1922.
- Ajusté las etiquetas de uso a "Variante de botón" y "Hover de menú" para que no se cortaran en la columna de requisito.

---

## User

Es al reves on surface como bg es el boton y la otra es el hover

---

## Assistant

Corregido. Ahora las etiquetas coinciden con el uso real:

| Primer plano | Fondo | Uso | Modo claro | Modo oscuro |
|---|---|---|---|---|
| `color-on-surface` | `color-secondary` | **Hover de menú** | 5.16:1 · AA | 4.91:1 · AA |
| `color-secondary` | `color-on-surface` | **Variante de botón** | 5.16:1 · AA | 4.91:1 · AA |

Es decir, **on-surface como fondo es la variante de botón** (con secondary encima), y **secondary como fondo es el hover del menú** (con on-surface encima). El resto de la tabla queda igual.

---

## User

te flalta tmb la combinacion de color-on-surface-bg y color primary que la uso para las opciones de los menus dropdown

---

## Assistant

Confirmado en el componente: la opción de dropdown usa `color-on-surface-bg` como fondo y `color-primary` como texto. Añado esa fila.



---

## Assistant

Se ha perdido la fila "Hover de menú" al añadir la nueva. Reconstruyo la tabla completa con las 10 combinaciones en orden, para que quede consistente.



---

## Assistant

Añadida la combinación de las opciones de dropdown y, de paso, reconstruida la tabla completa para recuperar la fila "Hover de menú" que se había perdido.

La tabla final tiene **10 combinaciones**:

| Primer plano | Fondo | Uso | Claro | Oscuro |
|---|---|---|---|---|
| on-surface-text | surface | Texto de cuerpo | 18.77 AAA | 12.08 AAA |
| on-surface-text | on-surface | Superficie elevada | 21.00 AAA | 6.98 AA |
| on-surface-text | on-surface-bg | Superficie anidada | 19.45 AAA | 6.98 AA |
| primary | tag-bg | Texto de etiqueta | 4.96 AA | 21.00 AAA |
| on-primary | primary | Texto de botón | 5.80 AA | 21.00 AAA |
| on-secondary | secondary | Botón secundario | 5.16 AA | 14.76 AAA |
| on-surface | secondary | **Hover de menú** | 5.16 AA | 4.91 AA |
| secondary | on-surface | **Variante de botón** | 5.16 AA | 4.91 AA |
| **primary** | **on-surface-bg** | **Opciones de menú dropdown** | **5.37 AA** | **6.98 AA** |
| star-bg | surface | Icono de estrella | 1.44 Falla | 7.52 Pasa |

La nueva fila de dropdown está confirmada contra el componente real: fondo `color-on-surface-bg` y texto `color-primary`. La sección queda en 976×1992.

---

## User

el star-bg lo he cambiado a neutral-600

---

## Assistant

Actualizado. `color-star-bg` ahora es **Neutral/600** en modo claro y la tabla refleja el cambio:

| Par | Modo claro | Modo oscuro |
|---|---|---|
| `color-star-bg` / `color-surface` | **3.54:1 · Pasa** | **7.52:1 · Pasa** |

- El icono de estrella ya cumple el **3:1** de componentes de interfaz en ambos modos (antes fallaba en claro con 1.44:1).
- También actualicé el valor mostrado en "Colores usados": **Claro #7F807F / Oscuro #CCCCCC**.

Un detalle: en modo oscuro `color-star-bg` sigue apuntando a `Neutral/400` (#CCCCCC). Si querías `Neutral/600` también en oscuro, dímelo y lo ajusto.

---

## User

ahora ayudame a remodelar las seccion fonts, poniendo la escala, los pesos usados con un ejemplo de cada nivel y su uso, y las 2 familias. Para ver concretamente familia y pesos puedes ver los estilos de texto y para poner los usos puedes usar las descripciones de cada variable de la coleccion font sizes, todo en español eso si

---

## Assistant

He remodelado la sección **Font sizes** y la he renombrado a **Tipografía** (976×1279). Ahora tiene esta estructura:

## Familias
Dos tarjetas con espécimen y niveles asociados:
- **Merriweather Sans** — Titulares (`Heading 1`, `Heading 2`, `Heading 3`)
- **Ek Mukta** — Texto (`Body`, `Label`, `Caption`)

## Pesos
Tabla comparativa con **Regular 400** y **Bold 700**, con ejemplo en cada una de las dos familias.

## Escala tipográfica
Tabla con los 6 niveles, mostrando para cada uno: muestra renderizada, tamaño, pesos disponibles, familia, uso y token CSS.

| Nivel | Tamaño | Peso | Familia | Uso |
|---|---|---|---|---|
| Heading 1 | 32 px | Bold 700 | Merriweather Sans | Título de presentación del perfil |
| Heading 2 | 24 px | Bold 700 | Merriweather Sans | Titulares de sección |
| Heading 3 | 20 px | Regular 400 / Bold 700 | Merriweather Sans | Títulos de cards y subtítulos |
| Body | 16 px | Regular 400 / Bold 700 | Ek Mukta | Texto de cuerpo |
| Label | 14 px | Regular 400 / Bold 700 | Ek Mukta | Texto de botones |
| Caption | 14 px | Regular 400 / Bold 700 | Ek Mukta | Anotaciones y textos de ayuda |

Los usos salen de las descripciones de las variables de la colección **Font sizes**, traducidos al español, y cada fila incluye su sintaxis (`--font-heading-1`, `--font-body`, etc.).

Un aviso: en los estilos de texto, **"Heading 2 Bold" usa Inter Bold** en lugar de Merriweather Sans (parece un resto). En la sección lo he documentado como Merriweather Sans para mantener las dos familias; si quieres, te corrijo ese estilo para unificarlo.

---

## User

ya lo he corregido yo, un par de cosas a corregir, corrigelas tmb en las descripciones de variables, pon que la Heading 2 se utiliza para los nombres de sitios y rutas como ejemplo y tmb en la heading 3 pon de ejemplo las reviews

---

## Assistant

Hecho. Corregidas las dos cosas en los dos sitios:

## Descripciones de variables (en inglés)
| Variable | Descripción |
|---|---|
| `Heading 2` | `24px. Heading 2 — used for place and route names (for example, site or route titles).` |
| `Heading 3` | `20px. Heading 3 — used for card titles, for example reviews.` |

## Tabla de escala (en español)
| Nivel | Muestra | Uso |
|---|---|---|
| Heading 2 | **Ruta del Cares** | Nombres de sitios y rutas |
| Heading 3 | **Reseñas de usuarios** | Títulos de cards, por ejemplo reseñas |

La sección sigue en 976×1279 y he confirmado que el estilo `Heading 2 Bold` ya usa **Merriweather Sans Bold** tras tu corrección.

Queda una duda pendiente: en modo oscuro `color-star-bg` sigue apuntando a **Neutral/400 (#CCCCCC)**, no a Neutral/600. ¿Lo cambio también a Neutral/600 para que coincida con el modo claro?

---

## User

en la heading 3 clarifica que se utiliza para los nombres de usuario dentro de una review, y para indicar la categoria y el rating de un sitio o ruta en su pantalla de informacion, luego el body me gustaria que figurara como texto de lectura, me parece mas correcto

---

## Assistant

Actualizado en ambos sitios.

## Descripciones de variables (inglés)
| Variable | Descripción |
|---|---|
| `Heading 3` | `20px. Heading 3 — used for usernames inside a review, and for the category and rating of a site or route on its information screen.` |
| `Body` | `16px. Body — used for reading text.` |

## Tabla de escala (español)
| Nivel | Muestra | Uso |
|---|---|---|
| Heading 3 | Reseñas de usuarios | Nombres de usuario en reseñas, y categoría y rating de sitio o ruta |
| Body | Texto de lectura | Texto de lectura |

También cambié la **muestra** de Body a "Texto de lectura" para que no contradiga el uso. La sección vuelve a quedar en 976×1279 (la fila de Heading 3 ya cabe en dos líneas).

---

## User

creo que el body 700 no lo utilizo realmente ahora que lo pienso, me lo puedes mirar y si no eliminamos ese estilo? mira solo la pagina mockups

---

## Assistant

Antes de borrar nada, he mirado la página **Mockups**: el estilo **Body Bold sí aparece**, en 7 textos, todos el mismo caso:

| Dónde | Texto | Nodo |
|---|---|---|
| Home Page · SearchBar | "¿What's your next destiny?" | `I1018:32;959:1766` |
| Search Page · SearchBar | (vacío) | `I1018:76;959:1766` |
| Place Preview · SearchBar | "Bar Manolo" | `I1018:155;959:1766` |
| Place Info · SearchBar | "Bar Manolo" | `I1018:185;959:1766` |
| Route Info · SearchBar | "Bar Manolo" | `I1018:328;959:1766` |
| Start Route · SearchBar | "Bar Manolo" | `I1019:348;993:387;959:1766` |
| Desktop Route Preview · SearchBar | "Bar Manolo" | `I1022:2066;993:387;959:1766` |

No es que lo hayas aplicado a mano: viene del componente **SearchBar** (`959:1761`), cuyo texto "Value" tiene aplicado Body Bold. Por eso se repite en todas las instancias. Parece un resto, porque el valor de un buscador no debería ir en negrita.

¿Cómo lo hago?

1. **Cambiar el "Value" del SearchBar a Body (Regular) y borrar Body Bold** — deja el buscador como esperabas y elimina el estilo. *(recomendado)*
2. **Solo borrar Body Bold**, dejando esos 7 textos en negrita pero sin estilo vinculado.
3. **Dejarlo como está.**

Si eliges 1 o 2, también actualizo la tabla de escala: Body pasaría a mostrar solo **Regular 400**.

---

## User

he metido en la guia de estilos una recreacion de mis pantallas mas complicadas con la font al 200% pillalas y metelas en la guia de estilo de tipografias

---

## Assistant

He encontrado las dos recreaciones al 200% en la página **Guía estilos**: `Desktop - Place Preview Page` (1439×1177) y `Place Info Page` (412×1471). Las integro como bloque dentro de **Tipografía**.



---

## Assistant

Listo. Las dos recreaciones ya están dentro de la sección **Tipografía**, en un bloque nuevo debajo de la escala.

## Qué he añadido

**Bloque "Texto al 200%"** (1891 px de ancho), con título, descripción y las dos pantallas lado a lado a tamaño real, cada una con su etiqueta y medidas:

| Pantalla | Tamaño |
|---|---|
| Escritorio · Place Preview | 1439 × 1177 |
| Móvil · Place Info | 412 × 1471 |

- Cada pantalla va dentro de un marco con borde y esquinas redondeadas, para que se lea como una muestra y no como un frame suelto.
- Se han movido los frames originales (no son capturas), así que siguen siendo editables y cualquier cambio en ellos se refleja aquí.
- La sección pasa de 976×1279 a **1955×2908** para que quepan las dos pantallas sin reducirlas: así el texto se ve realmente al 200%.

Los frames estaban en `y ≈ 1563–2950` de la página; ahora viven dentro de la sección, por lo que ese hueco de la página queda libre.

Queda pendiente lo de **Body Bold**: solo se usa en el texto "Value" del componente SearchBar (7 instancias). Dime si cambio ese texto a Body Regular y elimino el estilo.

---

## User

hazme una seccion de componentes en la guia de estilo, listando sus variantes y ejemplos de uso correcto e incorrecto de todos los componentes

---

## Assistant

Voy a inventariar los componentes del sistema y montar la sección. Son 21 componentes (63 variantes) más 21 iconos.



---

## Assistant

Creada la sección **Componentes** en la página Guía estilos, justo debajo de **Colores** (976 × 3277).

## Estructura

Cabecera con el recuento (**21 componentes · 43 variantes · 21 iconos**) y una fila por componente con tres bloques:

1. **Nombre + variantes** tal como están definidas en Figma (sin prefijos `Propiedad 1=` / `Status=`).
2. **Uso correcto** (pill verde) — 2–3 reglas.
3. **Uso incorrecto** (pill roja) — 2–3 anti-ejemplos.

## Componentes documentados

| Grupo | Componentes |
|---|---|
| Acciones | Button, Circle Button, Menu Option |
| Formularios | Input, File Input, Dropdown option, SearchBar |
| Contenido | Tag, Star, StarBar, Review, Review Form, Info Card Header |
| Accesibilidad | Accesibility Select, Accesibility check, Movement Method Select |
| Rutas | Route Indicator, Route Info, Route Selection Panel |
| Estructura | Session Modal, Side Option Panel |
| Iconos | Los 21 iconos, con tamaños y reglas de uso |

Ejemplos de las reglas:

- **Button** — ✅ una acción principal por bloque ("Reservar ruta") · ❌ dos botones predeterminados compitiendo.
- **Dropdown option** — ✅ fondo `color-on-surface-bg` + texto `color-primary` · ❌ dejar el hover como estado por defecto.
- **Accesibility Select** — ✅ el nivel se comunica con icono, texto y color · ❌ indicarlo solo con color.
- **Star vs StarBar** — ✅ StarBar solo lectura y con valor numérico · ❌ usarla como entrada de datos.

Dos apuntes:

- Solo documento la librería **Components**; **Wireframe Components** queda fuera por ser material de exploración (lo indico en una nota al pie).
- Los nombres originales tienen la errata **"Accesibility"** (con doble s); los he mantenido literal para que coincidan con Figma. Si quieres, los renombro a "Accessibility" en todo el archivo y actualizo la sección.

---

## User

En star ponme que no se usa fuera de la star bar, si se debe usar fuera de ahi que se use el icono star, en el dropdown option ponle que solo se usa para "animar" los select, input pon que preferiblemente se acompañen o de un label o del icono que incluye el componente, las tags pon que solo se usan dentro de las reviews, los selects de accesibilidad que solo se usan dentro del review form, los accesibility check solo se usan en las pantallas que dan info sobre un sitio o ruta, y su objetivo es comunicar la accesibilidad de forma puramente visual, por lo cual el icono asociado debe ser descriptivo del problema de movilidad que representa y solo se debe usar con un tick (accesible), un simbolo de advertencia (parcialmente accesible) y cruz (no accesible), el file input debe tener siempre un mensaje asociado indicando el archivo esperado el route indicator debe ir indicando con su icono la proxima direccion que el usuario debera tomar, normalmente con flechas, el letrero dara informacion sobre la proxima salida y otros detalles, y el letrero pequeño indicara cuanto tiempo debera seguir en esa direccion o cuanto queda para tomar la misma, el route info debera siempre marcar el tiempo y distancia restantes junto a la hora de llegada, estos 2 ultimos componenntes solo se deberan utilizar en la pantalla de In Route, el session modal se debera triggerear siempre que el usuario clique una accion que requiera registro (suponiendo que no esta registrado) y dicha modal debera mostrarse siempre centrada en la pantalla donde se da el evento, aplicando siempre el principio de figura y fondo siendo la figura dicha modal, el Route selection panel el input de arriba siempre debe ser "origen" con el icono de GPS Arrow y el input de abajo debe ser destino con el icono de GPS Pin, el side Option Panel sustituye al footer de movil por lo que solo debe usarse en desktop sustituyendo a este

---

## Assistant

Actualizadas las reglas de los 12 componentes que indicaste. La sección pasa a **976 × 3582**.

| Componente | Uso correcto ahora dice |
|---|---|
| **Star** | Solo dentro de StarBar; fuera de ella, usar el icono **Star Icon** |
| **Dropdown option** | Solo para animar los selects (normal + hover); fondo `color-on-surface-bg` con texto `color-primary` |
| **Input** | Preferiblemente con label visible; si no, el icono que incluye el componente; placeholder solo como ejemplo |
| **Tag** | Solo dentro de las reviews (nivel de accesibilidad y método del autor) |
| **Accesibility Select** | Solo dentro del Review Form |
| **Accesibility check** | Solo en pantallas de información de sitio o ruta; comunicación puramente visual; icono descriptivo del problema de movilidad, solo con tick (accesible), advertencia (parcial) o cruz (no accesible) |
| **File Input** | Siempre con mensaje asociado indicando el archivo esperado |
| **Route Indicator** | Solo en In Route; el icono marca la próxima dirección (flechas), el letrero la próxima salida y detalles, el letrero pequeño el tiempo restante en esa dirección |
| **Route Info** | Solo en In Route; siempre tiempo y distancia restantes + hora de llegada |
| **Session Modal** | Se dispara al pulsar una acción que requiere registro; centrada en la pantalla del evento; la modal es la figura (figura y fondo) |
| **Route Selection Panel** | Input superior = «Origen» + GPS Arrow; inferior = «Destino» + GPS Pin |
| **Side Option Panel** | Sustituye al footer móvil, por lo que solo se usa en escritorio |

En cada fila he ajustado también los "usos incorrectos" para que sean el espejo de la regla nueva (p. ej. *"Invertir el orden origen / destino"*, *"Mostrar footer y panel a la vez"*, *"Usar otro símbolo que no sea tick, advertencia o cruz"*).

---

## User

vale, he añadido 2 estados a la review form, uno de error y otro de empty, hay tmb una variante nueva del button deactivated, mirate los colores nuevos y los estados y actualiza la seccion de colores y componentes

---

## Assistant

He localizado los tres tokens nuevos (`color-deactivated`, `color-error`, `color-on-deactivated`) y los dos estados. Actualizo primero las variables y la sección de Colores.



---

## Assistant

Actualizado todo. Resumen:

## Variables nuevas (documentadas)
| Token | Claro | Oscuro | Descripción añadida |
|---|---|---|---|
| `color-deactivated` | `#E3B8B8` (Error/400) | `#E3B8B8` | Fondo de controles no disponibles |
| `color-error` | `#FF0004` (Error/900) | `#FF0004` | Mensajes de validación y error |
| `color-on-deactivated` | `#000000` (Neutral/950) | `#000000` | Texto/iconos sobre deactivated |

Las tres tienen descripción en inglés y code syntax (`--color-deactivated`, `--color-error`, `--color-on-deactivated`).

## Colores
- **Colores usados**: añadidos los 3 tokens (columnas 7 / 6), con swatch y valores Claro/Oscuro.
- **Contraste**: 2 filas nuevas.

| Par | Uso | Claro | Oscuro |
|---|---|---|---|
| `color-on-deactivated` / `color-deactivated` | Texto de botón desactivado | **11.80 AAA** | **11.80 AAA** |
| `color-error` / `color-on-surface-bg` | Mensaje de error en formulario | **3.70 Falla** | **1.75 Falla** |

## Componentes
- **Button**: 7 variantes (+ `Deactivated`). Regla: *Deactivated solo cuando la acción no está disponible*; incorrecto usarlo como hover o como estado de carga.
- **Review Form**: 3 estados (`Empty Form`, `Error Form`, `Filled Form`). Reglas: Empty sin datos y Publicar desactivado · Error con mensaje bajo el campo · Filled con Publicar activo.
- Contador actualizado a **46 variantes** y sección movida a `y = 2080` para no solaparse con Colores.

## Dos avisos
1. **`color-error` no cumple AA** como texto: 3.70 en claro y 1.75 en oscuro sobre `color-on-surface-bg`. Necesitaría un rojo más oscuro (o fondo más claro) para llegar a 4.5:1. Lo he dejado marcado como "Falla" en la tabla.
2. El borde del contenedor de error (`Frame 24` del Error Form) está vinculado al primitivo **`Error/900`**, no al semántico `color-error`. Si quieres, lo rebindeo.

---

## User

cambiamelo si, y el color-error solo lo uso de borde

---

## Assistant

Hecho.

## Cambios

| Acción | Resultado |
|---|---|
| Borde del `Frame 24` (Error Form) | `Error/900` → **`color-error`** |
| Descripción de `color-error` | "Used only for borders and outlines that indicate validation errors." |
| Fila de contraste | Ahora es de interfaz, umbral 3:1 |

| Par | Uso | Claro | Oscuro |
|---|---|---|---|
| `color-error` / `color-on-surface-bg` | Borde de error en formulario | **3.70 Pasa** | **1.75 Falla** |

Además he comprobado que **no queda ningún uso del primitivo `Error/900`** en la sección Components.

## Un detalle que sigue descuadrado

El texto del mensaje **"You must enter a valid review"** dentro del Error Form sigue vinculado a `color-error` como *relleno de texto*. Si `color-error` es solo para bordes, ese texto debería usar otro token (por ejemplo `color-on-surface-text`, o un rojo oscuro aparte). Además, tal como está, ese texto incumple AA (3.70 en claro, 1.75 en oscuro).

¿Quiero cambiarlo a `color-on-surface-text` o prefieres que creemos un token aparte para texto de error?

---

## User

cambiamelo a on-surface-text

---

## Assistant

Cambiado.

## Resultado

| Elemento | Antes | Ahora |
|---|---|---|
| Texto "You must enter a valid review" | `color-error` | **`color-on-surface-text`** |
| Borde del `Frame 24` | `Error/900` | `color-error` |

- El mensaje ahora cumple de sobra: **19.45 AAA** en claro y **6.98 AA** en oscuro (ya cubierto por la fila "Texto sobre superficie anidada").
- He revisado el archivo completo: **ningún texto usa ya `color-error`**; solo queda como borde.
- En la tabla de contraste, la fila del error ahora muestra una **muestra de borde** en lugar de "Aa", para que la previsualización coincida con el uso real.

Sigue pendiente el único fallo real: el borde de error en **modo oscuro** da **1.75:1** y no llega al 3:1 de componentes de interfaz. Si quieres, lo subimos a un rojo más claro para modo oscuro.

---

## User

dale

---

## Assistant

Listo. El borde de error ya cumple **3:1** en los dos modos.

## Cambios

| Elemento | Valor |
|---|---|
| Nuevo primitivo `Error/600` | `#FF8F8F` |
| `color-error` · modo claro | `#FF0004` (Error/900) |
| `color-error` · modo oscuro | `#FF8F8F` (Error/600) |

| Par | Uso | Claro | Oscuro |
|---|---|---|---|
| `color-error` / `color-on-surface-bg` | Borde de error en formulario | **3.70 Pasa** | **3.18 Pasa** |

- Actualizada también la línea de **Colores usados**: `Claro #FF0004 / Oscuro #FF8F8F`.
- El modo claro mantiene el rojo vivo; en oscuro se usa un rojo más claro, que es lo habitual para que el borde destaque sobre el gris `#5A5959`.

El primitivo lo he llamado `Error/600` para no tocar los existentes; si prefieres otro nombre (o un tono ligeramente distinto), lo cambio en un momento.

---

## User

añademe una escala pequeña con los colores de error

---

## Assistant

Añadida la escala **Error** en la sección Colores, con las mismas piezas que las demás (muestra, paso y hex).

| Paso | Hex | Uso |
|---|---|---|
| 400 | `#E3B8B8` | `color-deactivated` |
| 600 | `#FF8F8F` | `color-error` en modo oscuro |
| 900 | `#FF0004` | `color-error` en modo claro |

- Los swatches están **vinculados a las variables primitivas** (no a valores sueltos), así que si cambias el primitivo se actualiza la muestra.
- La descripción de la escala: *"Escala primitiva: solo se usa a través de color-error"*.
- Colores pasa a **976 × 2442** y he vuelto a bajar **Componentes** a `y = 2250` para mantener el hueco de 73 px entre secciones.

---

## User

vale, tengo que meter tambien las decisiones que afectan al peso de la app en otra seccion, quiero que hables en concreto de: como no he metido mas pesos ya que me parecia innecesario en cuanto vi que con un bold para distinguir los headings y controlando el tamaño de los pesos de 400 podia hacer una buena jerarquia, de como todos los iconos son svgs recogidos de iconify con un estilo uniforme, y de como en el modo oscuro he priorizado unos colores mas neutro, principalmente por un tema de accesibilidad, pero que al final es una cosa que afecta tambien

---

## Assistant

Creada la sección **Peso de la aplicación** en la Guía estilos, debajo de **Tipografía** (x=527, y=2716, 976×639), con las tres decisiones:

## 01 · Dos pesos por familia
> Solo se usan Regular 400 y Bold 700. El bold queda reservado a los titulares y el resto de la jerarquía se construye controlando el tamaño del 400. Añadir más pesos era innecesario: multiplicaba los archivos de fuente sin mejorar la lectura.

Meta: **2 familias · 2 pesos · 4 archivos de fuente**

## 02 · Iconos SVG de Iconify
> Todos los iconos son SVG de Iconify, con un estilo uniforme: mismo tipo de trazo y mismas proporciones, en tres tamaños (16, 20 y 24 px). No hay imágenes rasterizadas, así que escalan sin pérdida y el conjunto pesa muy poco.

Meta: **21 iconos · SVG · 16 / 20 / 24 px**

## 03 · Modo oscuro neutro
> En modo oscuro se han priorizado colores más neutros. La razón principal es la accesibilidad (menos saturación y mejores contrastes), pero también afecta al peso: menos variantes cromáticas que mantener y menos combinaciones que revisar.

Meta: **3 escalas + error · 13 tokens semánticos**

Cada decisión va en una tarjeta numerada, con una nota al pie: *"Estas decisiones se aplican en toda la app y sirven de referencia para cualquier incorporación nueva."*

He mantenido el hueco de 73 px respecto a Tipografía. Si prefieres que las tarjetas vayan en tres columnas en lugar de apiladas, lo cambio.

---

## User

añademe tambien en tipografia una tabla relacionando la jerarquia de fuentes con una etiqueta html: quiero que sea heading-1 = h1, heading 2, h1 si es la pagina de info de un sitio o ruta o marcador de la siguiente accion dentro de un trayecto, h2 si se trata del marcador de tiempo/distancia restante/hora de llegada de ese trayecto, heading 3 seria un h1 en las modales, h2 en la info de un sitio o ruta ya que es un subtitulo y h3 si se tratase de un nombre de usuario que puso una review en un sitio o ruta, body y caption serian <p> mientras que label seria el texto de un <button> o <select>

---

## Assistant

Añadida la tabla **Etiquetas HTML** en Tipografía, justo después de **Escala** (antes de la nota y del bloque de Texto al 200%).

## Tabla

| Estilo | Etiqueta | Contexto |
|---|---|---|
| Heading 1 | `<h1>` | Título principal de la página |
| Heading 2 | `<h1>` | Info de sitio o ruta · marcador de la siguiente acción en un trayecto |
| Heading 2 | `<h2>` | Marcador de tiempo/distancia restantes y hora de llegada |
| Heading 3 | `<h1>` | Título de una modal |
| Heading 3 | `<h2>` | Subtítulo en la info de un sitio o ruta |
| Heading 3 | `<h3>` | Nombre de usuario en una review |
| Body | `<p>` | Texto de lectura |
| Caption | `<p>` | Anotaciones y textos de ayuda |
| Label | `<button>` / `<select>` | Texto de botones y selects |

Encabezado de la tabla con una entradilla: *"La jerarquía visual no siempre coincide con la del documento: un mismo estilo puede ser h1, h2 o h3 según el contexto."*

## Estado del layout

| Sección | Posición | Tamaño |
|---|---|---|
| Colores | y −265 | 976 × 2442 |
| Componentes | y 2250 | 976 × 3590 |
| Tipografía | y −265 | 1955 × 3494 |
| Peso de la aplicación | y 3302 | 976 × 639 |

Sin solapes: el contenido de Tipografía acaba en 1833 y el bloque del 200 % empieza en 1889. Hueco de 73 px entre secciones.

---

Quedan tres cosas abiertas de antes, dime si las cierro:

1. **`Body Bold`** solo lo usa el texto "Value" del SearchBar (7 usos). ¿Lo dejo, cambio ese texto a Body, o elimino el estilo?
2. **"Accesibility"** está escrito con doble *s* en los nombres de componentes. ¿Renombro a "Accessibility"?
3. **`color-star-bg`** en oscuro apunta a `Neutral/400` `#CCCCCC`. ¿Lo cambio a `Neutral/600`?
