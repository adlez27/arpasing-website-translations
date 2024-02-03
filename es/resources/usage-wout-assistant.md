# Tutorial para el uso de bancos de voz sin ARPAsing Assistant
Este tutorial explicará cómo usar un banco de voz ARPAsing en UTAU, sin ARPAsing Assistant.

Lo mejor es tener un banco de voz cuyo OTO ya haya sido configurado en su totalidad antes de hacer UST con él, porque el ajuste del tiempo de las notas dependerá de los valores de preutterance.

Si no estás usando el plugin, puedes evitar todos los problemas relacionados con ajustar el tiempo y fonemas incorrectos. Sin embargo, perderás los beneficios de tener estas conversiones bases.
Si tu ordenador es capaz de usar ARPAsing Assistant pero eliges no usarlo, puedes abrir el exe como programa independiente para buscar conversiones palabra-a-arpabet. Sin embargo, si no te es posible usarlo en su totalidad (por ejemplo, usuarios de Mac) puedes usar [este sitio web]() para encontrar conversiones. El diccionario puede no ser tan robusto como el que está integrado al plugin, pero después de familiarizarse con el sistema fonético deberías poder transcribir las palabras que falten por tu cuenta. Si no estás familiarizado/a con Arpabet, puedes guiarte con [este artículo]() o con el [cuadro de fonemas]().

Introduce la letra en inglés al UST como harías normalmente, como referencia.
Cambia cada nota al CV principal de la sílaba, separando cada fonema con un espacio. Por ejemplo, la palabra "cat" es "K AE T" en arpabet, así que cambia la letra para que diga `[k ae]`. Del mismo modo, "steps" es "S T EH P S", entonces pon `[t eh]`.
Las otras notas esenciales que necesitamos son las notas al final de la frase. Cada vez que haya un descanso después de una nota, necesitarás tener un fonema seguido de un silencio. Como regla, si el descanso es menor al largo de 1/4 de nota, cambia todo el descanso. Si el descanso es más largo, entonces solo debes cambiar el primer 1/4 de nota. Para "cat" esto sería la nota `[t -]`, y para "steps" sería `[s -]`.

Lo que queda es introducir las notas transicionales. Esta lista funciona con dífonos, así que cada nota tiene dos fonemas.
El silencio cuenta como una, y es necesario cada vez que se transicione entre la letra cantada y descansos. Ya cubrimos las notas que tienen descansos AL FINAL, así que veamos las notas con descansos al inicio. Si comienzas con una vocal, puedes solo añadir un guion. Por ejemplo "eye" `[ay]` se vuelve `[- ay]`. Si comienza con una consonante o grupo de consonantes, querrás trabajar hacia atrás desde la consonante más interna. Toma "strand" como ejemplo. Crea una nota justo antes de `[r ae]` que contenga `[t r]`. Crea una nota justo antes de `[t r]` que contenga `[s t]`. Crea una nota justo antes de `[s t]` que contenga `[- s]`. Esto te dará una transición completa desde el silencio, a través de las consonantes, hasta el núcleo de la sílaba.
Para transiciones entre sílabas, usa este mismo principio de transiciones completas de dífono a dífono.

"stranded on this island"
`[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]`

La duración de las notas transicionales depende de la preutterance de la nota que sigue. Sin embargo, puedes usar tu juicio personal para hacerlas más largas o cortas.
Si alguna nota en particular suena extraña o fuera de lugar, puedes cambiarla usando grabaciones alternas del mismo dífono añadiendo un sufijo numérico, como cambiar `[f ey]` a `[f ey1]` y así.

Desde este punto, puedes hacer el tuning como harías normalmente.
