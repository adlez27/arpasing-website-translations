# Conversión de VCCV a ARPAsing

La reclist de inglés VCCV de PaintedCZ es popular en la comunidad internacional de UTAU, con una abundancia de bancos de voz y archivos UST disponibles en ese formato. Estos bancos de voz y archivos UST también pueden convertirse al estándar ARPAsing.

## Conversión de bancos de voz

La estructura organizacional de los bancos de voz VCCV divide las muestras en varias subcarpetas llamadas "CC-", "CV_CVC", etc. Las muestras de audio primero deben sacarse de las subcarpetas y ponerse en la carpeta principal del banco de voz. Descarga el archivo index [aquí]() y renómbralo a "index.csv", luego agrégalo a la carpeta.
Ahora puedes arrastrar y soltar la carpeta en Moresampler para la generación del OTO. Sin embargo, **no renombres/enumeres los duplicados**. Habrán cientos de duplicados, los cuales causaran que el ARPAsing Assistant no funcione correctamente. Descarga [esta herramienta]() para eliminar los duplicados del OTO generado. El máximo recomendado es entre 10-20.

## Conversión de archivos UST

Descarga [este plugin](), descomprímelo y colócalo en la carpeta de plugins donde UTAU esté instalado. Usar este plugin en un UST va a convertirlo desde los fonemas CZ a fonemas arpabet. Sin embargo, esto no lo volverá perfectamente compatible con un banco de voz arpasing de inmediato (por ejemplo, algunas notas pueden tener más de 2 fonemas). Por favor haz ajustes para acomodar el banco de voz.
Plugin original por ChieP  
Convertidor inspirado por Ivory @TheIvoryShield  
Modificaciones al plugin por KLAD
