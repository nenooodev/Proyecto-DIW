# Fotos del mapa en Figma

**Session ID:** ses_e44a24204ffesCfEyv1ehnzx8q
**Created:** 11/8/2026, 2:34:05 PM
**Updated:** 11/8/2026, 3:51:24 PM

---

## User

https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=975-1532&p=f&t=qG6Pnw4inpBTj36D-0 restaura las fotos del mapa a color en los mockups, para ello debes: ir a la seccion mobile y desktop (original, no redesign) restaurar la saturacion de todas las fotos del mapa de GMaps a su valor original, y reemplazarlas en las pantallas equivalentes de los mockups, sin, por supuesto, modificar nada en los wireframes

---

## Assistant

I'll start by exploring the Figma file to understand its structure.

---

## Assistant

I've confirmed the map photos are color images with a desaturation filter applied (and one baked grayscale). Now I'll restore them in the Mockups page only.

---

## Assistant

Listo. Restauré los mapas de GMaps a color en la página **Mockups**, respetando la estructura y sin tocar la página **Wireframes**.

**Qué encontré:** los mapas eran imágenes a color con un filtro de saturación `-1` aplicado en el relleno (uno de ellos, el del Home, estaba ya aplanado en gris).

**Cambios aplicados (solo en Mockups):**

Sección **Mobile**
- `Home Page` y `Home Page Responsive`: sustituí el mapa en gris por el original a color del wireframe original de Home (misma vista de Cádiz).
- `Place Preview Page`: saturación restaurada a 0 (color).
- `Start Route Page`: saturación restaurada a 0 (color).
- `In Route Page`: se mantiene el mapa oscuro, ya estaba a saturación original (0) y es el estilo previsto en el diseño original.

Sección **Desktop**
- `Desktop - Home Page`: saturación restaurada.
- `Desktop - Profile Page`: saturación restaurada.
- `Desktop - Place Preview Page` → `Foto local`: saturación restaurada.
- `Desktop - Route Preview Page` → `Mapa ruta`: saturación restaurada.

**Verificación:** todos los rellenos de imagen de mapas en Mockups quedan con `saturation: 0`, y comprobé que los valores de saturación de la página Wireframes (Mobile, Mobile Redesign, Desktop y Desktop Redesign) siguen exactamente como estaban.

---

## User

revisame en la pagina de wireframes que cada elemento de las secciones de redesign tenga su spacing vinculado a una variable, tanto el mobile como el desktop, si alguno no lo tiene cambialo a la variable mas cercana

---

## Assistant

He revisado y corregido el spacing en las dos secciones de redesign de la página **Wireframes**, sin tocar las secciones originales.

**Alcance**
- `Wireframes > Mobile Redesign` (`812:1301`)
- `Wireframes > Desktop Redesign` (`812:985`)

**Resultado de la auditoría**
- **Mobile Redesign:** 459/459 campos de spacing no nulos quedan vinculados a variables.
- **Desktop Redesign:** 509/515 campos vinculados.
- Total: **623 vinculaciones** aplicadas (gap + padding en todos los auto-layout, incluidos los elementos dentro de instancias).
- Sin errores.

**Criterio usado**
Se han mapeado al token más cercano de la colección **Spacing** (`space-1`=4, `space-2`=8, `space-3`=12, `space-4`=16, `space-6`=24, `space-8`=32, `space-12`=48, `space-16`=64). En los empates (10, 14, 20) se ha elegido el token menor para no forzar crecimiento de layouts:
- 10 → `space-2` (8)
- 14 → `space-3` (12)
- 20 → `space-4` (16)
- 9.6 → 8 · 12.3 → 12 · 11 → 12 · 2/3/5 → 4
- 8, 12, 16, 24, 32 ya coincidían con su token.

**Excepciones (6 campos, 3 nodos)**
No los he vinculado porque no son spacing de diseño, sino valores de centrado/separación estructural; ajustarlos a 64 rompería la composición:
- `Desktop - Request Session Page` (`812:1056`): `gap 150` y `padding izq./der. 351` (centrado del modal).
- `Wireframe Side Option Panel` en Profile y Place Preview: `itemSpacing 512` (spacer que empuja contenido).

Si quieres, puedo crear variables específicas para esos valores (p. ej. `layout-center-351`, `spacer-512`) y vincularlos también.

Las secciones **Mobile** y **Desktop** originales quedan intactas, y no se ha modificado ningún componente principal: los cambios de las instancias son overrides por instancia.
