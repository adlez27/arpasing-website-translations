# Tutorial de creación de bancos de voz

Este tutorial cubre tanto la grabación como la configuración de OTO.

Si bien puedes usar lo que quieras para grabar, te será mucho más fácil usar OREMO. Si actualmente no estás familiarizado/a con su uso, ve esto como una oportunidad para aprender. Si planeas procesar las muestras, deberás hacerlo después de grabar.
Descarga oficial: [OSDN]()  
Port para macOS: [UTAForum]()  
Version nativa traducida al inglés para Mac: [UTAForum]()  
(Recomiendo usar la versión port, porque la versión nativa para mac no tiene la caja de comentarios).

Para comenzar, descarga la última reclist por defecto de [la página de reclists](). Puedes escoger entre la versión con o sin el index. Si no usas OREMO, la versión sin index va a ser mucho más fácil de leer.

Si estás usando la lista con index:
- La carpeta contine un archivo de reclist, un archivo de comentario de OREMO y un archivo index.
- La reclist son números del 000 al 334.
- El archivo de comentario de OREMO te permite ver los fonemas o palabras reales que corresponden a cada número.
- El archivo index es para que Moresampler tenga una referencia a la hora de configurar el OTO.

Si estás usando la lista sin el index:
- La carpeta contiene un archvio de reclist y un archivo de comentario de OREMO.
- La reclist contiene fonemas arpabet.
- El archivo de comentario de OREMO te permite ver las palabras que corresponden con los fonemas.
- No se necesita un archivo index, ya que Moresampler puede leer los nombres de los archivos directamente.

Crea una carpeta para tu banco de voz y copia y pega OREMO-comment.txt (e index.csv en caso de haberlo) en tu nueva carpeta. En OREMO, abre la reclist. Establece como carpeta de destino tu nueva carpeta.

Puedes grabar con o sin guideBGM. Si quieres usar guideBGM, recomiendo usar una corta hecha para reclists CVVC, como las BGM CVVChinese o las BGM VCCV English.

Note to translator: These next two lines were written for english speakers.

El archivo de comentario te dirá cómo pronunciar aproximadamente usando palabras, y precisamente usando fonemas arpabet. [Este artículo corto]() te explicará cómo leer y pronunciar el arpabet. ¡Es bastante simple! Si ya estás familiarizado/a con otro sistema fonético como el sistema de PaintedCZ o X-SAMPA, consulta el cuadro en [esta página]().
Aparte de las líneas para vocales, cada línea tiene solo 1 tipo de vocal. Las tres sílabas rimarán.

Note to translator: Please write a new section here about how to properly pronounce English phonemes, for people who may be unfamiliar with them.

A pesar de que usamos (casi) las mismas letras, el inglés posee más fonemas que el español y tiene reglas de pronunciación muy distintas a las nuestras, por lo que es común para los hablantes de español ver una palabra escrita en inglés, hacerse una idea de cómo leerla pero en realidad tiene una pronunciación que jamás habríamos pensando (sobre todo las vocales, pero también suele suceder que existan consonantes con distintas pronunciaciones o incluso que sean mudas). En el cuadro de fonemas he tratado de mostrar cómo entender los sonidos del inglés desde el español, pero mientras más referencias se pueda tener, mejor. Otro punto a considerar es que normalmente al hablar tanto en español como en inglés se suelen simplificar u omitir pronunciaciones para hacer más rápida la comunicación, al momento de grabar un banco de voz se debe intentar pronunciar cada fonema indicado de manera clara para tener una buena configuración y que se puedan escuchar bien en el programa.
En resumen, lo que recomiendo es aprender bien el sonido de cada fonema para poder distinguirlos entre sí lo mejor posible y pronunciarlos de manera estable durante toda la grabación. También considero más fácil guiarse por los fonemas como si cada uno fuera una letra distinta que por las palabras del archivo de comentario, ya que como indiqué anteriormente, en inglés las letras no se leen siempre de la misma manera, si es que se pronuncian del todo.

Canta las 3 sílabas de forma consecutiva, como si estuvieras grabando VCV. Si en algún punto hay una "q" en los fonemas (o un apóstrofe en las palabras) significa una pequeña pausa/silencio (glottal stop/parada glotal).
Como referencia, puedes descargar bancos de voz existentes desde el [directorio de bancos de voz]().

**PARA TONOS MÚLTIPLES:** La carpeta principal del banco de voz debe contener un tono que no tenga ningún sufijo. Todos los otros tonos deben estar dispuestos en subcarpetas. Cuando grabes, no agregues sufijos a los nombres de los archivos, o Moresampler no podrá leer el index.csv al configurar el OTO.
**PARA MUESTRAS EXTRA:** Cualquier muestra extra que no sea estándar en ARPAsing debe estar en una subcarpeta, ya que deben tener un archivo oto.ini separado. Esto permite que el ARPAsing Assistant lea correctamente el oto.ini principal que posee solo entradas de OTO ARPAsing estándar.

¡A configurar el OTO! Simplemente arrastra y suelta la carpeta en moresampler.exe para hacerlo.
Escribe 3 para elegir arpasing. Cuando se te pregunte si quieres renombrar duplicados, escribe y o yes. Cada vez que haya múltiples de cada dífono, como [s t], hacer esto agregará un sufijo numérico al final de las copias adicionales. Esto sirve para distinguir cada una, ya que pueden sonar diferente según el contexto de fonemas cercanos en la línea. También puedes decidir si quieres o no incluir un sufijo. No es posible usar caracteres como flechas o kanji, por lo que tendrás que usar sufijos como "S" o "A#3".

Si estás usando Mac o Linux, deberás usar wine para abrir Moresampler. Abre la terminal en la carpeta en la que esté moresampler.exe y escribe "wine moresampler.exe /ruta/al/bancodevoz". Si no puedes hacerlo, transfiere tus archivos a un ordenador Windows, o pide ayuda a un amigo con Windows para que lo genere.

Ahora que tu OTO base está generado, es momento de afinarlo. Cada entrada del OTO es un dífono, lo que quiere decir que solo hay dos fonemas o dos sonidos. En general, el primero es un conector a la nota previa, mientras que el segundo es el fonema principal de la nota presente. Para configurar el OTO, primero encuentra la sección correspondiente al primer fonema, después encuentra la sección para el segundo fonema.

## Primer Fonema

Esto cubre el offset azul y el overlap.

**[-]**  
La cantidad de overlap no importa realmente para este, porque estas notas siempre vienen al inicio de una frase, justo después de un descanso. Lo único importante es que cubra un área de silencio.

**[c]**  
*Oclusivas sordas (p t k)*  
Si este es el primer fonema en la línea, mueve el offset de manera que el overlap termine aproximadamente 15ms antes de la consonante.
Si hay otros fonemas antes que este, mueve el offset hasta donde terminó el anterior. Asegúrate de no poder escuchar el anterior. Pon el overlap aproximadamente 15ms antes de la consonante.

*Oclusivas sonoras y africadas (b d g ch jh)*  
Si este es el primer fonema en la línea, mueve el offset de manera que el overlap termine donde la consonante empieza.
Si hay otros fonemas antes que este, mueve el offset hasta donde terminó el anterior. Asegúrate de no poder escuchar el anterior. Pon el overlap donde la consonante empieza.

*Fricativas, nasales, y líquidas (f v th dh s z sh zh hh m n ng l r)*  
Mueve el offset hasta donde empieza la consonante. Para 'r' en particular, puede que quieras consultar la sección de glides como ayuda.

*Glides (y w)*  
Estas consonantes pueden ser difíciles de ver en una forma de onda normal. Haciendo clic en el botón [s], puedes cambiar a la vista de espectrograma, la cual te da otra forma de visualizar el audio. Las zonas claras son las frecuencias más fuertes. Estas consonantes aparecen como un cambio en las frecuencias con el tiempo.
Mueve el offset hasta donde comienza la consonante, después por el overlap donde sea consistente antes del cambio. La preutterance quedará después del cambio.

**[v]**  
Por defecto, el overlap de estas muestras debería ser bastante amplio. Si es absurdamente pequeño, sería bueno moverlo hasta alrededor de los 50ms.
Mueve el offset inicial para que el área entre este y el overlap esté a un nivel consistente.

Para diptongos, el overlap debería cubrir el área antes que la vocal cambie.

## Segundo Fonema

Para todos los casos, la preutterance debería ubicarse donde termina el primer fonema y comienza el segundo fonema. Esto también cubre el área rosada, el área blanca y el cutoff azul.

**[c]**  
*Terminaciones (p b t d k g ch jh)*  
Debería haber un pequeño trozo de silencio o casi silencio justo antes de la consonante. Mueve el rosado donde comienza el silencio y el cutoff hasta donde el silencio termina. Sí, no estamos incluyendo a la consonante misma. Esto es porque, en un UST, esta nota debería ser continuada por otra nota que SÍ tenga la consonante. Esto permite una transición fluida sin un sonido extraño de doble consonante.

*Fricativas (f v th dh s z sh zh hh)*  
Cubre la consonante entera con rosado hasta justo antes del final. LLeva el cutoff hasta el mismo lugar, dejando un pequeño espacio. Sin este espacio, los resamplers no serían capaces de renderizarlo. Sin embargo, no queremos que estas consonantes se estiren.

Si hay silencio después de la consonante, deja el área blanca como silencio.

*Nasales, líquidas y glides (m n ng l r y w)*  
Mueve el rosado hasta donde la consonante empieza a ser estable y consistente. Usa el cutoff para remover donde la consonante termina o se apaga. Estas consonantes pueden estirarse.

**[v]**  
Mueve el rosado hasta donde la vocal empieza a ser estable y consistente. Usa el cutoff para remover donde la vocal se apaga. El área blanca será la parte sostenida de la nota, lo que asegura que sonará bien.

Para dífonos vocal-vocal, pon la preutterance al final del cambio vocálico.

Para diptongos, pon el cutoff antes de que la vocal cambie.

**[-]**  
Cubre todo con rosado, de manera que todo lo que esté blanco sea silencio.

Y así sin más, tu banco de voz ya está listo. Por favor envía cualquier banco publicado al directorio. Diviértete, ¡buena suerte!
