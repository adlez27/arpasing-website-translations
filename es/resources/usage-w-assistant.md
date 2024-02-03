# Tutorial para el uso de bancos de voz con ARPAsing Assistant

Este tutorial explicará cómo usar un banco de voz ARPAsing en UTAU, usando ARPAsing Assistant.
Lo mejor es tener un banco de voz cuyo OTO ya haya sido configurado en su totalidad antes de hacer UST con él, porque el ajuste del tiempo de las notas dependerá de los valores de preutterance.

Si todavía no tienes el plugin ARPAsing Assistant, puedes descargarlo [aquí](). Descomprime el toolkit y mueve la carpeta "arpasing-assistant" a la carpeta "plugins" donde UTAU está instalado.
Pon palabras normales en inglés en el UST, selecciona las notas y arranca el plugin ARPAsing Assistant para convertirlas. Como alternativa, puedes ingresar los fonemas arpabet en la nota, separados por espacios. Si colocas `/u` al final de una palabra, la nota se dividirá en partes equidistantes para cada dífono, en lugar de que cada dífono tenga diferentes duraciones.
Las notas que selecciones para la conversión DEBEN tener otra nota después de ellas. La mejor forma de asegurar esto es poner un descanso al final del UST.

Para hacer palabras multisilábicas a través del **ingreso de palabras**, deberás eliminar todas las notas excepto la primera sílaba y extender la primera nota para cubrir la duración de todas las notas combinadas. Pon la palabra completa en la nota, y conviértela de forma normal. Desde aquí deberás poner las notas de vuelta al tono correcto y corregir el tiempo.
Sin embargo, hacer palabras multisilábicas a través del **ingreso de fonemas** es mucho más fácil, ya que puedes simplemente partir los fonemas a través de varias notas existentes antes de la conversión.

**PARA TONOS MÚLTIPLES Y MUESTRAS EXTRA:** Si un banco de voz está correctamente configurado, debería funcionar sin problemas, pero hay situaciones comunes que causan incompatibilidad con ARPAsing Assistant. La carpeta principal del banco de voz debe contener un tono sin sufijos, y todos los otros tonos deben estar en subcarpetas. Cualquier muestra extra no estándar también debe estar en subcarpetas. ARPAsing Assistant solo lee el archivo oto.ini principal del banco de voz, y ese archivo debe contener solo entradas de OTO ARPAsing estándar.

Cuando conviertas palabras en notas difónicas, ARPAsing Assistant seleccionará la mejor copia de un dífono en particular basado en el contexto. Por ejemplo, si ingresas la palabra "stand", eligirá una nota `[t ae]` desde una muestra "stae" en vez de una muestra "tae". El contexto de grabaciones usando palabras crea una prounciación natural. Este es el propósito de los sufijos numéricos, para distinguir entre ellas. No elimines los números.

Si bien se recomienda usar un UST completamente sin tuning, puedes ajustar el nivel de volumen de notas y flags antes de la conversión, y estos se mantendrán.
Los pitchbends y vibratos se estropean y alinean con notas erróneas, por lo que se recomienda removerlos por completo antes.

Escucha el UST como quede para tener una idea de cómo suena y qué secciones debes arreglar. Lo más probable es que algunas notas quedarán fuera de tiempo, y habrán pronunciaciones que no te dejen satisfecho.
Encuentra las palabras o sílabas donde la pronunciación no es la que deseas. Si no estás familiarizado/a con Arpabet, puedes guiarte con [este artículo]() o el [cuadro de fonemas]() al editar.

Arreglemos los tiempos. El problema más evidente es con palabras multisilábicas. Ya que debieron ser combinadas en notas únicas antes de la conversión, los tiempos no quedan como se había previsto. Mantén ctrl y arrastra los finales de las notas para cambiar las duraciones sin empujar las demás notas. Alínealas para que los CV principales de cada sílaba comiencen en la posición prevista. Ajusta los tonos mientras lo haces, seleccionando todas las notas de una sílaba y moviéndolas arriba/abajo.
Busca frases que comiencen con consonantes (serían las primeras sílabas después de lo que era un descanso). La nota `[- C]` suele ser muy corta, así que mantén ctrl y arrastra el lado izquierdo para hacerla más larga. Ajusta la duración para que empiece donde el envelope de la nota siguiente comienza.

A partir de ahí puedes ir a nota por nota arreglando el tiempo de todas las notas pequeñas, cambiándolas a la duración del envelope de la preutterance de la nota siguiente.
Por esto es que quieres que el OTO de tu banco de voz esté completamente configurado. Probablemente querrás establecer tu Quantize a 64th notes.
A medida que vayas puedes también modificar pronunciaciones. Por ejemplo, "don't want" quedará como `[d ow][ow n][n t][t w][w aa]`, etc. pero estas son demasiadas notas para un espacio corto, donde en la práctica esta frase suele sonar como "don want" al cantar. Por lo tanto, remueve `[n t]` y cambia `[t w]` a `[n w]`.

Desde este punto, puedes hacer el tuning como harías normalmente.
