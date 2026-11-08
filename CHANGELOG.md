# Uso de IA

## Brief

https://chatgpt.com/share/6ad3b740-2748-83ed-bc1f-491dd8167a26 

En esta conversación se puede ver como le pedi a chatgpt ayuda con la redacción del brief, lo he revisado manualmente y el resultado final es bastante similar al que se ve en el ultimo prompt, simplemente me he limitado a quitar textos redundantes una vez obtuve dicha versión

## Ayuda con las entrevistas

Entrevista 1: https://share.gemini.google/S5rS4ivUQbWw

Le pedi a Gemini que me ayudase a transcribir y respetar el formato pedido para la entrevista 1, ya que entremezclaba audios de Whatsapp mios como entrevistador con respuestas en texto del entrevistado, en la conversación pase un .md con los huecos para los audios seguidos de la respuesta correspondiente del entrevistado, para que Gemini solo tuviera que rellenar esos huecos con la transcripción, también le pedi que no me transcribiera literalmente, ya que al ser una conversación larga y en audios hay muchas muletillas pausas e informalidades por mi parte, por lo que tambien le pedí que recortara ese tipo de cosas manteniendo la esencia de la conversación

Entrevista 2: 

https://share.gemini.google/brPRcrlkzXIb

Para esta entrevista simplemente me limité a pedir una transcripción sin pausas ya que al estar todo en audio era más sencillo, yo simplemente corregí alguna palabra que no estaba bien transcrita y quitar el encabezado

# Órbita 2

## Asesoría en la paleta de colores

https://chatgpt.com/share/6adfa5a8-d140-83ed-b195-645cdc6cdeda

Una vez tenia una paleta de colores escogida , me surgieron dudas de como combinar bien los azules que habia elegido (ya que los azules son los colores que a mi parecer se asocian más a la movilidad reducida) con el amarillo a modo de complementario, asi que, aunque veia que la paleta tenia un sentido, decidi preguntar a chatgpt por si me hacia visualizarlo mejor. 

## Ayuda restaurando componentes pre-rediseño

[Transcripción](chats/opencode-chat.md)

[Transcripción 2](chats/opencode-chat2.md)

Hubo componentes que rediseñé tocando el componente principal, por lo que se cambiaron todas las instancias y el rediseño no se apreciaba. Para no perder el tiempo copiando y pegando del historial de versiones, le pedi a opencode que me ayudara via MCP, en ninguna de estas conversaciones cambié nada ya que la idea era simplemente restaurar algo ya hecho

## Stitch como referente en los rediseños

[Móvil](https://stitch.withgoogle.com/projects/20239359341740460)

[Escritorio](https://stitch.withgoogle.com/projects/10305205798995987055)

La mayoría de cambios que he hecho en los rediseños son inspirados por los wireframes que me ha dado Stitch, no he aplicado nada directamente, ya que dichos diseños me parecían sobrecargados, pero es cierto que me ha servido de referencia para saber qué cambiar en ciertos componentes de mi UI, como la sidebar, la barra de búsqueda etc... 

## Ayuda desvinculando componentes usados en los wireframes para hacer cambios independientes en los mockups

[Transcripción](chats/opencode-chat3.md)
Como tenía muchos componentes ya hechos desde la Órbita 1, dupliqué la hoja y le pedí a opencode que me desvinculara las instancias duplicadas de sus padres, para así poder editar esos componentes en los mockups sin afectar a los wireframes, ya de paso le pedí que me agrupase tanto los componentes del wireframe como los del mockup por atomic design, para no hacerlo yo manualmente.

## Ayuda construyendo mockups a partir de estructura wireframes + componentes ya estilizados

[Transcripcion](chats/opencode-chat4.md)

Le pedi a opencode que me construyera los mockups con la misma estructura que el rediseño de los wireframes, utilizando los componentes coloreados en lugar de los blanco y negro, para ahorrar tiempo en calcar las pantallas. Tuve que corregir algunos detalles de color y el prototipado, pero en general estaba bastante bien, ya que simplemente era reconstruir algo ya hecho

## Ayuda con instancias anidadas

[Transcripcion](chats/opencode-chat5.md)

Después de la conversación anterior, tuve algunos problemas porque la IA me habia recreado las instancias anidadas como frames, de forma que no veia reflejados los cambios si hacía cambios en el padre, simplemente le pedi que lo corrigiera

## Ayuda con guia de estilos

[Transcripcion](chats/opencode-chat6.md)

Esto es una conversación muy larga que abarca varios dias y bastantes iteraciones por mi parte en la que empiezo pidiendole que me ayude con las descripciones y sintaxis de código de las variables y terminamos componiendo toda la guía de estilos, siempre con la idea de yo ser el que toma las decisiones y la IA el brazo que escribe y lo pone presentable, he retocado sobre todo en la parte de casos de uso de componentes.

## Ayuda con restos

[Transcripcion](chats/opencode-chat7.md)

Aquí le pedí un pequeño checkeo de restos del proyecto porque controlar que todo use variables se me ha hecho bastante trabajoso (especialmente con el spacing) y no quería que se me pasase nada (aun así algo se dejó por el camino)

## Retoques finales

[Transcripcion](chats/opencode-chat8.md)

Aquí le pedí que restaurase las capturas de google maps a su saturación original (para quitar el blanco y negro) para los mockups y que mirase otra vez restos de variables pero esta vez en los wireframes.
