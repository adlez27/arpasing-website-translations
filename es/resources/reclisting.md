# Tutorial para la escritura de reclists

ARPAsing no es una reclist única y estática, sino un método de UTAU en inglés. Es similar a cómo VCV no es una única reclist, sino un método de UTAU en japonés. El único criterio para que una reclist sea una reclist ARPAsing es la compatibilidad con el OTO automático de Moresampler y con el plugin ARPAsing Assistant.

Puedes escribir tu reclist en inglés o líneas adicionales de la forma que quieras, mientras los fonemas que incluyas se correspondan directamente al Arpabet. En cuanto esté escrita, necesitarás crear un archivo index.csv para que Moresampler sepa cómo configurar el OTO.
Si estás escribiendo líneas adicionales, puedes simplemente agregarlas al index.csv existente para esa reclist. Si estás haciendo una lista desde cero, deberás crear un nuevo archivo index. Puedes usar cualquier editor de texto para crear uno, pero también puedes usar el editor de csv que quieras.

La primera columna contiene todos los nombres de los archivos, los cuales son por lo general exactamente los mismos del archivo de reclist que usarías en OREMO. Debes incluir la extensión de archivo. Si estás usando un editor de texto, separa esta columna de la siguiente con una coma. La segunda columna tiene la versión en arpabet de los fonemas para esa línea. Cada fonema debe ser separado por un guion bajo.
Como alternativa, puedes escribir tu reclist directamente en Arpabet desde el inicio, y separar cada fonema con un guion bajo. Esto elimina completamente la necesidad de escribir un index.csv.

Todos los fonemas arpabet son aceptados por el OTO automático de Moresampler, excepto estos:
`[em] [en] [eng] [el] [nx] [dx]`

Si has hecho líneas adicionales, debes generar el OTO para todo el banco de voz, para que los duplicados sean correctamente enumerados.

Para hacer la grabación más fácil, también puedes hacer un archivo de comentario de OREMO. El archivo se llama "OREMO-comment.txt" y va en la carpeta destino del banco de voz. La primera columna contiene todos los nombres de los archivos correspondientes a la reclist. La extensión de archivo no es necesaria, solo debe concordar con el archivo de reclist. Separa las columnas con tabulador. En la columna siguiente va el comentario, donde escribes notas, como la forma en que la muestra debe pronunciarse.
