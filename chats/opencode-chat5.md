# Molecules y organisms como instancias

**Session ID:** ses_e5d03d882ffecIo8VnevMnBJv2
**Created:** 11/3/2026, 8:56:36 PM
**Updated:** 11/3/2026, 9:07:35 PM

---

## User

https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=959-1581&t=5SfovA6GVitbjRFa-0 haz que, en la seccion components de la pagina components, las molecules y organisms utilicen instancias de otros componentes, y no como frames

---

## Assistant

I'll start by reading the Figma guidelines and inspecting that section of the file.

---

## Assistant

Now I'll perform the conversions in the Molecules section.

---

## Assistant

He convertido los frames de **Molecules** y **Organisms** que replicaban componentes en instancias reales de esos componentes.

**Molecules**
- **Accesibility Select** (8 variantes): 16 opciones “Dropdown option” → instancias de *Dropdown option*.
- **Movement Method Select** (6 variantes): 9 opciones → instancias de *Dropdown option*.
- **StarBar**: los 5 frames “Star” → instancias de *Star* (variante Predeterminada).
- **SearchBar**: el frame “Circle Button” → instancia de *Circle Button*; los 3 “Menu Option” → instancias de *Menu Option* (Horizontal) con el icono cambiado a *Restaurant* y textos “Bar Antonio / Bar Manolo / Bar Juana La Loca”.
- **Route Info**: el frame “Circle Button” → instancia de *Circle Button* con el icono cambiado a *Cross*.

**Organisms**
- **Review**: los 2 frames “Tag” → instancias de *Tag*.
- **Review Form**: “Accesibility Select”, “Movement Method Select”, “Input” (área), “StarBar” y “Button” → instancias.
- **Route Selection Panel**: “SearchBar” → instancia de SearchBar (campo de búsqueda estirado a FILL) y los 2 “Input” → instancias de *Input*, conservando los iconos GPS Arrow / GPS Pin.
- **Session Modal**: “Back Arrow” → instancia de *Back Arrow*, los 5 “Input” → instancias de *Input*, “File Input” → instancia de *File Input* y los 2 “Button” → instancias de *Button*.

Detalles:
- Cada instancia conserva el tamaño original del frame y he sobrescrito los textos e iconos necesarios (Publish, Login, Sign Up, Email, Contraseña, Tu ubicación, Bar Manolo…), incluidos iconos ocultos vía la propiedad `hasIcon` cuando el frame original no los mostraba.
- He dejado como frames solo los contenedores de layout (Frame 7/8/9 de los selectores, Frame 15/23/24/25/30, Frame 16/17, Frame 29…), que no duplican ningún componente.
- Consecuencia visual esperada: los elementos adoptan el estilo real del componente (botones morados de la variante Predeterminada, opciones de dropdown como píldoras redondeadas, campo de búsqueda del SearchBar). Aviso de que los selectores “Open” de *Accesibility Select* ya venían con desbordamiento/recorte en los laterales del diseño original; no lo he modificado.
- Los componentes editados (SearchBar, StarBar, etc.) no se usan como instancia en otras páginas del archivo, así que no afecta a Mockups ni al resto.
