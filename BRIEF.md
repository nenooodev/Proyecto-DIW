# Brief de proyecto: plataforma de rutas y lugares accesibles

## 1. Descripción del proyecto

El proyecto consiste en desarrollar una aplicación web inspirada en Google Maps, orientada a personas con movilidad reducida, que permita consultar rutas y puntos de interés teniendo en cuenta su accesibilidad real. La plataforma combinará la planificación de rutas, la información sobre barreras arquitectónicas y las reseñas aportadas por usuarios verificados que tengan experiencia directa con las dificultades de movilidad.

Las reseñas incluirán una clasificación del nivel de accesibilidad del lugar, que podrá ser **accesible, parcialmente accesible o no accesible**, y el método de desplazamiento utilizado por la persona que realiza la visita: **silla de ruedas o andador**. De esta forma, los usuarios podrán contextualizar las experiencias compartidas y comprender cómo puede variar la accesibilidad de un mismo lugar según las necesidades de movilidad de cada persona.

La aplicación se desarrollará utilizando **Angular** para el frontend, coordinando su implementación con las tecnologías definidas en el módulo de DWEC.

## 2. Problema que resuelve la aplicación

Las personas con movilidad reducida pueden encontrar dificultades para desplazarse de forma autónoma porque la información habitual de navegación no siempre permite conocer con suficiente detalle las barreras físicas que encontrarán durante el recorrido. Una ruta aparentemente válida puede incluir aceras estrechas, bordillos, obstáculos, zonas sin rampas o accesos incompatibles con sus necesidades. Del mismo modo, un establecimiento o punto de interés puede parecer accesible en términos generales y presentar, en realidad, dificultades que impidan su visita.

La investigación realizada para definir las user personas identifica dos situaciones concretas:

- **Usuario principal:** una persona de 18 años con parálisis cerebral infantil (PCI), que utiliza una silla de ruedas y dispositivos de asistencia basados en Tobii y TTS. Su ficha destaca las dificultades para desplazarse por calles con bordillos, obstáculos o aceras estrechas, así como las limitaciones del transporte público y la importancia de poder comunicarse durante el recorrido. Necesita planificar desplazamientos accesibles sin renunciar a su autonomía.
- **Usuario secundario:** una persona de 83 años que utiliza andador y presenta dificultades para manejar dispositivos móviles y ordenadores. Su ficha recoge la necesidad de desplazarse por rutas sencillas y evitar complicaciones tecnológicas, además de la posibilidad de necesitar asistencia en determinados trayectos.

Estas fichas muestran que la accesibilidad debe abordarse desde dos perspectivas complementarias: la accesibilidad física de las rutas y los lugares, y la accesibilidad de la propia aplicación.


## 3.  MVP

El MVP incluirá exclusivamente las funcionalidades necesarias para consultar rutas accesibles y compartir información útil sobre la accesibilidad de lugares.

### Funcionalidades incluidas

1. **Planificación de rutas:** permitir establecer un origen y un destino mediante una interfaz inspirada en Google Maps.
2. **Puntuación de accesibilidad:** mostrar una valoración de las rutas en función de sus características de accesibilidad.
3. **Filtrado automático de rutas:** excluir las rutas identificadas como no accesibles según los criterios disponibles.
4. **Consulta de puntos de interés:** mostrar información de lugares y establecimientos, incluyendo sus reseñas de accesibilidad.
5. **Verificación de usuarios:** establecer un mecanismo de verificación para que las reseñas que requieren esta condición puedan ser publicadas por usuarios verificados.
6. **Publicación de reseñas:** permitir que los usuarios verificados escriban reseñas sobre puntos de interés, describiendo las condiciones de accesibilidad que hayan experimentado.

Las reseñas incluirán dos datos que permitirán interpretar mejor cada experiencia:

- **Nivel de accesibilidad del lugar:** accesible, parcialmente accesible o no accesible.
- **Método de desplazamiento utilizado:** silla de ruedas o andador.


### Funcionalidades fuera del MVP

Para mantener un alcance realista y priorizar las funcionalidades esenciales, quedan fuera de esta primera versión:

- Guardado de lugares y rutas favoritas.
- Historial de reseñas publicadas.
- Ampliación de las valoraciones de accesibilidad para contemplar otros tipos de discapacidad, más allá del enfoque inicial en movilidad reducida.

Estas funcionalidades podrán evaluarse para futuras versiones, una vez validada la utilidad de la propuesta principal.

## 4. Personas usuarias

### Persona principal: usuario de silla de ruedas

**Perfil:** persona de 18 años con parálisis cerebral infantil, usuaria de silla de ruedas y de tecnologías de apoyo a la comunicación.

**Necesidades principales:** encontrar rutas transitables, evitar barreras físicas, conocer las condiciones reales de calles y lugares y desplazarse con la mayor autonomía posible.

**Papel en el diseño:** representa el perfil prioritario para definir los criterios de accesibilidad de las rutas, los filtros, la presentación de la información y la compatibilidad de la interfaz con tecnologías de apoyo.

También permitirá comprobar que las reseñas aportan información útil sobre la accesibilidad de los lugares para personas que utilizan silla de ruedas.

**Ficha:** [Ficha de usuario principal](#fichas/usuario-principal).

### Persona secundaria: persona mayor usuaria de andador

**Perfil:** persona de 83 años que utiliza andador y que puede encontrar dificultades al manejar dispositivos móviles y ordenadores.

**Necesidades principales:** consultar rutas sencillas, evitar obstáculos y recorridos complicados, comprender rápidamente la información y utilizar una interfaz clara que no requiera conocimientos tecnológicos avanzados.

**Papel en el diseño:** permite comprobar que la aplicación sea comprensible y fácil de utilizar, con textos legibles, navegación predecible, controles claros y pocas barreras cognitivas.

Asimismo, permitirá evaluar si la clasificación de las reseñas ayuda a identificar las condiciones de accesibilidad experimentadas por otras personas que utilizan andador.

**Ficha:** [Ficha de usuario secundario](#fichas/usuario-secundario).


## 5. Criterios de éxito

El diseño se considerará satisfactorio cuando las personas representadas por las user personas puedan completar las tareas esenciales de manera comprensible, autónoma y accesible.


### Usuario principal

- Puede introducir un origen y un destino y consultar una ruta accesible sin ayuda externa.
- Puede identificar cuál de las rutas propuestas presenta mejores condiciones de accesibilidad y comprender por qué.
- Puede excluir las rutas que no cumplen sus necesidades de movilidad mediante los filtros disponibles.
- Puede consultar la ficha de un punto de interés y localizar rápidamente la información relevante sobre su accesibilidad.
- Puede identificar si un lugar está clasificado como accesible, parcialmente accesible o no accesible.
- Puede distinguir las reseñas realizadas por personas que utilizan silla de ruedas de aquellas realizadas por personas que utilizan andador.
- Puede publicar una reseña con el nivel de accesibilidad y el método de desplazamiento correspondientes, tras completar el proceso de verificación requerido.
- Puede completar las tareas principales utilizando las tecnologías de apoyo compatibles con su dispositivo, sin bloqueos en los controles esenciales.

### Usuario secundario

- Puede planificar un desplazamiento y localizar una ruta adecuada sin asistencia de otra persona.
- Puede identificar las rutas y los puntos de interés accesibles sin tener que interpretar información técnica compleja.
- Puede localizar las reseñas y comprender sus conclusiones mediante una interfaz clara y consistente.
- Puede distinguir el nivel de accesibilidad indicado en una reseña y reconocer si la experiencia corresponde a una persona que utiliza andador o silla de ruedas.
- Puede completar las tareas principales sin perderse en la navegación ni depender de instrucciones externas.
- Puede utilizar la aplicación con el texto ampliado y los controles accesibles sin que el contenido se corte o se produzcan desplazamientos horizontales innecesarios.

### Medición durante las pruebas

Para comprobar estos criterios se registrarán:

- El porcentaje de tareas completadas correctamente.
- El tiempo necesario para completar cada tarea.
- El número de errores y de solicitudes de ayuda.
- La capacidad de comprender las valoraciones y los criterios de accesibilidad.
- La capacidad de interpretar correctamente las tres categorías de accesibilidad y los dos métodos de desplazamiento.
- Los problemas detectados al utilizar tecnologías de apoyo, ampliar el texto o navegar mediante teclado.

Antes de realizar las pruebas, se establecerán objetivos cuantitativos para cada indicador. Los tiempos y porcentajes definitivos se fijarán como umbrales de evaluación, no como resultados ya obtenidos.

## 6. Restricciones del proyecto

### Restricciones tecnológicas

- El frontend deberá desarrollarse con **Angular**, respetando la estructura y las convenciones del framework.
- La implementación deberá coordinarse con los proyectos de DWEC y DWES, ajustándose a las tecnologías, los contratos de API y los servicios acordados para la comunicación con el backend.
- La información de rutas, puntos de interés, valoraciones y reseñas deberá proceder de fuentes disponibles y de datos que el sistema pueda gestionar.
- Las funcionalidades que dependan de servicios externos de mapas, geolocalización o cálculo de rutas estarán condicionadas por las API seleccionadas, sus límites de uso y sus condiciones de licencia.
- El sistema de verificación deberá limitar la publicación de las reseñas sujetas a este requisito a usuarios que hayan completado el procedimiento establecido.
- Los formularios de reseñas deberán permitir indicar el nivel de accesibilidad y el método de desplazamiento mediante opciones claras y comprensibles.

### Restricciones temporales

El desarrollo se realizará dentro del calendario académico del proyecto. Por ello, se priorizarán las funcionalidades esenciales del MVP y se evitará incorporar características secundarias que aumenten la complejidad sin contribuir directamente a validar la propuesta.

La planificación deberá contemplar el diseño de la interfaz, la implementación en Angular, la integración con el backend, las pruebas funcionales y las pruebas de accesibilidad y usabilidad.

### Restricciones relacionadas con las personas usuarias

- La aplicación deberá funcionar correctamente en los dispositivos móviles y ordenadores compatibles con la solución.
- La interfaz deberá ser compatible, en la medida que permitan el entorno técnico y las tecnologías seleccionadas, con lectores de pantalla, navegación mediante teclado y tecnologías de apoyo a la comunicación.
- Los textos deberán ser claros, los controles fáciles de identificar y la navegación consistente.
- La información importante no deberá depender exclusivamente del color, de iconos ambiguos ni de interacciones complejas.
- La experiencia deberá contemplar a personas con distintos niveles de competencia digital y permitir ampliar el texto sin perder contenido ni funcionalidad.
- La accesibilidad de las rutas no deberá presentarse como una garantía absoluta si la información disponible es incompleta, antigua o no ha sido verificada.

### Restricción ambiental y de conectividad

Al tratarse de una aplicación de planificación de desplazamientos, deberá poder utilizarse en situaciones en las que la conexión a Internet sea lenta, inestable o se interrumpa temporalmente. Esta situación puede producirse durante los trayectos o en zonas con poca cobertura, dificultando el acceso a la información necesaria para decidir cómo continuar un desplazamiento.

Para reducir este problema, se establece como objetivo inicial que la transferencia de datos de la carga inicial de la aplicación no supere **1 MB comprimido**, sin contar los recursos cartográficos externos, las teselas del mapa ni otros recursos de terceros, que se contabilizarán por separado.

El peso reducido de la aplicación contribuirá a disminuir el consumo de datos y a mejorar los tiempos de carga en conexiones lentas. Asimismo, se deberá evitar que una interrupción temporal de la conexión provoque errores innecesarios o deje la interfaz inutilizable. Cuando sea técnicamente viable, la aplicación conservará la información ya cargada y comunicará claramente cuándo no sea posible consultar datos actualizados o acceder a servicios externos.
