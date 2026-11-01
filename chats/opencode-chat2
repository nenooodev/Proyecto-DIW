# Sustituir componentes old en wireframes

**Session ID:** ses_e677aa715ffeTZTaVjk9fZxXvJ
**Created:** 11/1/2026, 8:10:38 PM
**Updated:** 11/1/2026, 8:23:10 PM

---

## User

https://www.figma.com/design/ipV0P6FMdSz1lAe6mR5cnu/Proyecto-DIW?node-id=4-6&p=f&t=QWYXJaE3HxuUBBiq-0 tengo este proyecto donde estoy haciendo unos rediseños de wireframes, la cosa es que he rediseñado cambiando el componente principal y hora los rediseños no se aprecian, tienes los componentes antiguos en una seccion old, quiero que cambies sus equivalentes por esos en todas las paginas excepto las que pone Desktop Redesign y Mobile Redesign, que son los wireframes "nuevos"

---

## Assistant

I'll start by exploring the Figma file to understand the structure.



---

## Assistant

Now I understand the structure. Let me run a pilot swap on a few frames to validate the direction before applying it everywhere.



---

## Assistant

Direction confirmed: the old pages were showing the redesigned components. Let me apply the swap across all Mobile and Desktop frames.



---

## Assistant

Listo. He cambiado los componentes en las páginas antiguas para que vuelvan a mostrar el diseño anterior, dejando intactos los wireframes nuevos.

## Qué he hecho

En la página **💡 Wireframes**, en las secciones **Mobile** y **Desktop** (9 + 5 frames), he sustituido las instancias de los componentes rediseñados por sus equivalentes de la sección **old**:

| Componente rediseñado | Reemplazado por (sección `old`) | Instancias |
|---|---|---|
| Wireframe SearchBar | SearchBar | 7 |
| Wireframe Button | Button | 9 |
| Wireframe Input | Input | 4 |
| Wireframe Info Card Header | Info Card Header | 4 |
| Wireframe Session Modal | Session Modal | 2 |
| Wireframe Route Info | Route Info | 1 |

También he reenlazado las instancias de `Button` que apuntaban a un componente principal ya eliminado (las que había en Place Preview / Start Route) hacia el `Button` de `old`.

**No he tocado** `Mobile Redesign` ni `Desktop Redesign`: siguen con los componentes nuevos (botones tipo pill de 44 px, searchbar de 54 px, review form con estrellas y Publish, modal ancho, etc.). Verificado: 0 instancias nuevas quedan en Mobile/Desktop y las secciones Redesign conservan todas las suyas.

## Ajustes de tamaño necesarios

Al volver a los componentes antiguos, algunas instancias conservaban el tamaño del componente nuevo:
- **Session Modal** (Request Session, mobile y desktop): estaba a 373 px y se salía del frame; la he devuelto a su ancho original de 257 px y ha quedado centrada.
- El resto (searchbars de 400/420 px, inputs de 365 px) mantienen el ancho que tenía el diseñador; solo ha cambiado la altura, que ahora se adapta al componente antiguo.

## Dos cosas que conviene que revises

1. **Sliver de foto en Place Info / Route Info (mobile)**: ahora se ve una franja de ~40 px de la foto de cabecera por encima del bloque gris "Foto bar". No lo he provocado yo: el overlay `Frame 16` está fijado en y=217 y no sigue al contenido; al ser la cabecera antigua 10 px más baja, se ve un poco más. Si quieres, lo alineo.
2. **Instancias huérfanas**: en las páginas antiguas siguen quedando instancias de `Review Form`, `Review`, `Accesibility Select`, `Movement Method Select` (ids `888:*`) cuyo componente principal ya no existe en el archivo (fueron borrados). Se ven bien, pero no se pueden editar desde un componente maestro porque no hay copia de ellos en `old`. Puedo duplicarlos allí y reenlazarlos si te interesa.
