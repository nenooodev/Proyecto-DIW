# Desvincular instancias en Figma Components

**Session ID:** ses_e6258c5ddffePIj2j3H8FoePJ0
**Created:** 11/2/2026, 8:05:44 PM
**Updated:** 11/2/2026, 8:17:29 PM

---

## User

https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=526-8&p=f&t=0jvIsarqq8CJqnBK-0 abre la pagina de components y desvinculame las instancias de todos los componentes en la seccion "Components", no toques la seccion Wireframe Components, cuando termines ordename los componentes de ambas secciones por secciones segun nivel de atomic design

---

## Assistant

I'll start by opening the Figma file and locating the page and sections you mentioned.

---

## Assistant

Antes de modificar el archivo, necesito confirmar dos detalles para no romper nada:

---

## Assistant

Perfecto. Primero verifico los límites reales de cada componente (algunos hijos sobresalen de su marco) para calcular la cuadrícula sin solapamientos.

---

## Assistant

Voy a probar el comportamiento del detach con una de las instancias para confirmar que los iconos internos permanecen vinculados.

---

## Assistant

Confirmado: los iconos permanecen vinculados. Ahora desvinculo el resto de instancias no-icono de la sección "Components".

---

## Assistant

Detach completado: 61 instancias desvinculadas, 63 iconos siguen vinculados. Ahora creo las subsecciones por nivel atómico y redistribuyo los componentes en ambas secciones.

---

## Assistant

Listo. Resumen de lo que hice en [Proyecto DIW → página Components](https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=526-8):

**1. Desvinculación de instancias (sección "Components")**
- Detach realizadas: **61 instancias** (las 6 principales + 55 anidadas que no eran iconos: Dropdown option, Input, Button, Star, Dropdown lists, etc.).
- **63 instancias de iconos siguen vinculadas** (Compass, GPS Pin, Settings, Star Icon, Back Arrow, caret, etc.), tal como pediste.
- La sección **Wireframe Components no se tocó**: sus 111 instancias siguen intactas.

**2. Organización por Atomic Design (en ambas secciones)**
Creé subsecciones anidadas dentro de cada sección, en este orden vertical:

| Nivel | Componentes | Cantidad |
|---|---|---|
| **Átomos** | Button, Circle Button, Dropdown option, Input, Star, Tag | 6 |
| **Moléculas** | Accessibility Select, Accessibility check, File Input, Info Card Header, Menu Option, Movement Method Select, Route Indicator, Route Info, SearchBar, StarBar | 10 |
| **Organismos** | Review, Review Form, Route Selection Panel, Session Modal | 4 |

- Componentes redistribuidos en cuadrícula con separación uniforme, alineados y **sin solapamientos** (lo verifiqué con las cajas reales de cada componente).
- Ambas secciones quedaron con el mismo tamaño (1040 × 3295).
- Moví "Wireframe Components" a x = -300 para que el nuevo ancho no se monte sobre la sección **Icons**, que dejé sin tocar.

Todo se puede revertir con Ctrl/Cmd+Z si algo no encaja. Si quieres, también puedo agrupar la sección **Icons** como Átomos.

---

## User

vale pero a los componentes desvinculados quitales Wireframe del nombre y vuelvelos a poner como componente, esta vez independiente

---

## Assistant

Entendido. Voy a renombrar los componentes de la sección "Components" quitando el prefijo "Wireframe" y convertir las 6 instancias desvinculadas (ahora frames) en componentes independientes.

---

## Assistant

Hecho en la sección **Components**:

**Renombrado (20 elementos)**
Eliminé el prefijo "Wireframe" de todos los componentes de la sección:
- **Átomos:** Button, Circle Button, Dropdown option, Input, Star, Tag
- **Moléculas:** Accesibility Select, Accesibility check, File Input, Info Card Header, Menu Option, Movement Method Select, Route Indicator, Route Info, SearchBar, StarBar
- **Organismos:** Review, Review Form, Route Selection Panel, Session Modal

**Conversión a componentes independientes (7)**
Los que habían quedado como frames tras el detach ahora son `COMPONENT` propios, sin vínculo a ningún master:
- Accesibility check
- Route Indicator
- Route Info
- StarBar
- Review
- Review Form
- Route Selection Panel

Los otros 13 ya eran `COMPONENT_SET` independientes (copias locales) y solo se renombraron.

**Estado final**
- Sección **Components**: 20 componentes, 0 con "Wireframe", 63 instancias de iconos que siguen vinculadas (como pediste).
- Sección **Wireframe Components**: intacta, conserva sus nombres "Wireframe…" y sus 111 instancias.
- Sin solapamientos ni elementos fuera de las subsecciones.

Nota: algunas capas internas de los componentes (por ejemplo dentro de Session Modal o Review Form) siguen llamándose "Wireframe Input", "Wireframe Button", etc. Si quieres, también les quito el prefijo.

---

## User

sisi, tu quitalo

---

## Assistant

Listo. Quité el prefijo **"Wireframe"** de las **55 capas internas** de la sección **Components**:

- Frames de Dropdown option, Input, Button, Star, Tag, Menu Option, File Input, Circle Button, StarBar, etc.
- No quedó ninguna capa con "Wireframe" en esa sección (verificado: 0 coincidencias).
- No se tocaron las variantes (`Propiedad 1=…`, `Status=…`) ni los nombres de los 20 componentes principales.
- La sección **Wireframe Components** sigue intacta con sus nombres originales.
