# Como utilizar HT Letterspacer    

> Esta __herramienta fue creada para diseñar__ el espaciado de una fuente tipográfica, la desarrolló Andrés Torresi y es distribución libre.
> Corre como un macro en el editor de fuentes [Glyphs](https://glyphsapp.com/) pero el método de espaciado que propone puede ser adaptado a otros editores o lenguajes de programación.    
> El HT Letterspacer puede ser utilizado en fuentes simples o superfamilias, adaptable a diferentes sistemas de escritura y puede ser aplicado durante la etapa de diseño o en fuentes ya terminadas. No está desarrollado para hacer kerning, sino para diseñar el espacio a la derecha e izquierda de los signos.    
> En el [Home page de HT Letterspacer](https://huertatipografica.github.io/HTLetterspacer/) y en el [repositorio GitHub](https://github.com/huertatipografica/HTLetterspacer) puedes encontrar más información sobre el desarrollo de esta herramienta.    
> Puedes descargarla gratuitamente del siguiente [link](https://huertatipografica.github.io/HTLetterspacer/).    

### La magia no existe, son horas de trabajo    

Los primero que debes saber es que HT Letterspacer no es una *varita mágica*, no reemplaza al diseñador, el HT Letterspacer es una __herramienta__ y como tal debes aprender a utilizarla, debes aprender a configurar sus parámetros generales y debes aprender a modificar el archivo de configuración externa que adapta esos parámetros generales a las diferentes categorías de signos, en resumen, debes aprender a pensar el espaciado a través de esta nueva metodología y en este sentido estamos frente a un cambio de paradigma.    

### _NOTA Glosario
Hay muchos términos de nuestro oficio quisieramos establecer, pues al pasar de un idioma a otros algunos concepto se van mezclando y confundiendo.

- Fuente    
- Caracter    
- Glifo    
- Signo    
- Caja - ancho de caja    
- Outline
- Boudingbox - BBox - BB
- Left / Right side bearings (LSB / RSB), side bearings_    

### El concepto detrás de HT Letterspacer

Al diseñar una letra diseñamos el negro y el blanco, el trazo y el espacio que lo rodea.
Esta herramienta propone un método para pesar, diseñar y definir el espacio a la izquierda y a la derecha de un signo utilizando 3 parámetros. 
Primero debemos establecer los parámetros generales para las letras minúsculas y luego esos parámetros generales serán ajustados para las otras categorías de signos (mayúsuclas, figuras, puntuación) en un archivo de configuración externa (explicaremos esto más adelante).    

Por lo tanto esta herramienta tiene 2 estaciones de trabajo:    

- Definir los parámetros generales para las minúsculas en el editor de tipografía a través de la ventana emergente `HT Letterspacer UI`
- Adaptar esos parámetros a las otras categorías de signos en el archivo (externo) de configuración `elnombredenuestrafuente_autospace.py`.

Es una herramienta para diseñadores, no hay parámetros mágicos, cada diseñador puede hacer sus propios experimentos hasta lograr el color que pensó para su tipografía.    
El espaciado es una cuestión de diseño, los diseñadores de tipografía diseñamos el blanco que rodea a un signo, esas decisiones son afectadas por la forma y contraforma, el dibujo de los signos, las proporciones, el estilo, la función, los parámetros que define en el HT Letterspacer contemplan estos factores.

### Paso 1 → Descarga e instalación

1. Para comezar, descarga HT Letterspacer del [repositorio GitHub](https://github.com/huertatipografica/HTLetterspacer), y al ser un script de payton que corre en el editor de fuentes Glyphs, debes tener esta aplicación instalada.

![ventana de git hub](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/descargar-ht-de-git-hub.png?raw=true)

También puedes utilizar la applicación de GitHub Desktop o descargarlo desde la terminal.

En el editor de fuentes Glyphs debes seguir los siguientes pasos:

2. Abrir las preferencias de Glyphs, menú _Glyphs > preferencias_ (`Cmd⌘-` `,`), en la ventana de preferencias, ir a la sección _Addons > Modules_ y hacer click en _Install Modules_.    

![install modules image](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/glyph-preferences-install-modules.gif?raw=true)

3. Ir al menú _Script > Abrir la carpeta de Scripts_ (Cmd⌘-Shift⇧-Y) y cerrar la aplicación Glyphs. En el escritorio se abrirá en el escritorio la carpeta donde Glyphs guarda los _scripts_.

![Abrir la ventana de scripts](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-open-script-folder-sin-ht-letterspacer.png?raw=true)

En esta carpeta podrás podrás encontrar los _scripts_ que ya tienes instalados, o si no has intalado ninguno, una carpeta vacía.

![scripts folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-folder.png?raw=true)

4. Colocar aquí la carpeta que descargaste en el paso 1.

![add img to scripts glyph's folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/add-ht-to-scripts-folder.gif?raw=true)

5. Volver a Glyphs e ir al menú _Script_ presionando la tecla `Opt ⌥`, de esta manera al desplegar el menú en lugar de _abrir ventana de scripts_ ahora podrás ver al final la opción _Reload Scripts_ esta acción se actualizará dicha carpeta y podrás ver entre las opciones de _scripts_, _HTLetterspacer_.    
► Corte de tecla__ → otra forma veloz de acutalizar la carpeta de script: `Cmd⌘ Opt⌥` `Schift⇧` `Y`    

![script palet con ht letterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer.png?raw=true)

6. __Opcional:__ cuando ya estés trabajando con el HT Letterspacer puedes utilizar un glifo de prueba llamado `_area`, para esto deberías bajar `objectsGS.py` y `GSPen.py` del [repositorio de Glyphs-Scripts](https://github.com/schriftgestalt/Glyphs-Scripts) y ponerlos en la carpeta _Scripts_ (similar a lo que hiciste en los puntos 2, 3, 4 y 5). Estos _scripts_ siven para generar ese glifo `_areas`.


### Paso 2 → Utilización inicial del HT Letterspacer

Hemos empezado a diseñar nuestra fuente tipográfica, ya tenemos un par de signos, por ejemplo una `n`, una `o` , una `v`, una `c` y ahora debemos diseñar el blanco que los rodea, o sea, el espaciado. Aquí es donde empezamos a utilizar nuestra herramienta de espaciado.    

Antes debemos resolver un pequeño asunto. La primera vez que utilizamos el espaciador con una fuente tipográgica iremos al menú _script > HTLetterspacer_, allí se despliegan 2 opciones: HTLetterspacer UI y HTLeterspacer, el asunto es que antes de poder elegir una de esas opciones se abrirá una ventana de diálogo que nos indica que falta un _archivo de configuración_ y nos pregunta si queremos crearlo, a lo que debemos responder __Yes!__   

![missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/missing-config-file-window.png?raw=true)

De esta manera se genera automáticamente un archivo `.py` en la misma carpeta donde has guardado el archivo `.glyph`. Si vamos a esa carpeta encontraremos un nuevo archivo llamado `elnombredenuestrafuente_autospace.py`, este era el _archivo de configuración faltante_, hablaremos de él más adelante.    

![Ventana missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/config-file-folder.png?raw=true)

### Paso 3 → Primera aproximación al diseño de espaciado. Definición de los parámetros generales

> En esta sección hablaré de diseño de espaciado propiamente dicho y de como utilizar el HT Letterspacer para espaciar una fuente tipográfica.    
> Por tal motivo, antes quisiera hacer una breve introducción, para que podremos partir del mismo lugar y evitar malentendidos, ambigüedad o desencuentros semánticos:
> - ¿Qué es espaciado? – Definir algunos términos
> - ¿Qué actores intervienen durante el proceso de espaciado? 
> - ¿Qué factores podríamos considerar relevantes en la toma de partido del diseño del espaciado de una fuente?
> - ¿Cómo estos factores están reflejados en los parámetros que HT Letterspacer propone?

La novedad de esta herramienta es que nos desafía a pensar un método de análisis del espaciado diferente, tal vez esto es lo que nos desorienta un poco en los primeros momentos.

Espaciar es determinar cuánto espacio hay a la derecha y a la izquierda de un signo, cuanto aire lo rodea, es diseñar el blanco que nos deja leer al negro.    
Espaciar es equilibrar el espacio que hay dentro de la letra con el espacio que hay fuera de ella. 

![imagen espacio interno =~ espacio externo telder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/espacio-int-simliar-espacio-ext-telder.jpg?raw=true)
![imagen espacio interno =~ espacio externo alegreya](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/espacio-int-simliar-espacio-ext-alegreya.jpg?raw=true)

En este punto estamos todos más o menos de acuerdo, si hemos leímos sobre espaciado, el concepto de igualar blancos interno-externo es recurrente. La imagen es similar: si para llenar el interior de una `n` necesito 1 litro de agua/vino/cerveza, para llenar el epsacio entre esa `n` y la letra que sigue será también 1 litro. La gran pregunta es cómo hacer esto de alguna manera sistematizada para agilizar el proceso de producción.

Los métodos de espaciado propuestos por Walter Tracy, Thomas Phinney, Frank E. Blokland,  ponen el foco en las formas, agrupandolas, clasificándolas, analizandolas —rectas, curvas, diagonales, cuánto incide el serif, la aperturas, etcétera—.
HT Letterspacer propone un método que no se basa (al menos en la primera aproximación) en observar la forma, la atención apunta al espacio y nos anima a mirar ese blanco, lo que tenemos que determinar es dónde termina ese blanco y empieza el blanco del glifo siguiente.   

#### Los factores que determinan el _criterio_ de espaciado podrían ser:
- diseño
- proporciones
- color
- función
- soporte
- etc.

#### Los actores que intervienen técnicamente son:
- sidebearing izquierdo y derecho
- contorno del glifo
- bbox
- ancho de caja

> #### Glorsario:
> - El __punto de origen__ es el punto cero en el eje x.
> - El __ancho de la caja__ _(Advance width)_ es el ancho que avanza el signo, el límite izquierdo es el punto de origen ( que coincide el _sidebearing_ izquierdo) y el límite derecho es el _sidebearing derecho._ Generalmente el ancho de caja es mayor a cero y es mayor al ancho del _bouding box._    
> - Cuando hablo de __glifo,__ hago referencia al dibujo, la forma y al espacio que lo rodea.
> - cuando hablo del __contorno__ hago referencia a la línea que dibuja la forma y contraforma, a la línea que dibuja el negro. 
> - los puntos extremos del contorno del glifo determinan el __Bouding Box (o BBox)__. O el __BBox__ es el rectángulo que circunscribe al _contorno del glifo._
> - __Sidebearing__ es el componente esencial del espaciado, es el espacio, uno a la izquierda y otro a la derecha. Cada glifo tiene un sidebearing izquierdo llamado LSD _(left side bearing)_ y un sidebearing derecho, __RSB__ _(right side bearing):_ __LSB__ es la distancia entre el punto de origen y el lado izquierdo del _BBox_. __RSB__ es la distancia entre el lado derecho del _BBox_ y el ancho de la caja.
> ![imagen anatomía del signo](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/anatom%C3%ADa-del-glifo.jpg?raw=true)
> 
> counter es la contraforma
> el dibujo es la forma

 
# ¡Explicar como esos factores técnicos están representados en el ht letterspacer!

Los límites del espacio están delimitados por la caja y el contorno del glifo.




Esta etapa es de prueba y contraprueba desde la ventana emergente `HT Letterspacer UI` (User Interface).    

Pero antes, me gustaría hablar un momento sobre espaciado. Cuáles son los factores que 


Resuelto el asunto del archivo de configuración faltante se abrirá la ventana emergente del espaciador. Allí están los parametros que debemos ajustar para definir el espaciado de nuestra tipografía.        

![Ventana emergente con explicación de los parámetros](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/parametros-explicacion.png?raw=true)
 

1. __LBS / RSB.__ _Left / Right Side Bearings_, si ambos están tildados, indica que el espaciado se aplica a la derecho e izquierda del signo.     

2. __Tabular.__ Es item es para las figuras tabuladas, o una fuente monoespaciada o de ancho fijo. Si tildamos este parámetro, debemos indicar cuál es el ancho del signo.   

__REVISAR LAS IMAGENES, ESTAN MAL!__

3. __Area__ `paramArea`. Este parámetro define un área, una superficie rectangular determinada entre el lado derecho (o izquierdo) del signo, su correspondiente _Side Bearing_, la línea de base y la altura de x. Esta área se calcula en unidades UPM, para una tipografía para texto el valor estará entre 200 y 400.

![paramArea](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramArea.png?raw=true)

4. __Depth__ `paramDepth`. Cómo vimos, el área es un rectángulo, pero las letras nos rectangulares, si tenemos una `v`, una `c` o una `T` hay una gran cantidad de blanco que no es considerada por el parámetro área, los triángulos debajo de la `v` o la contraforma abierta de la`c`. ¿A partir de donde se empieza a medir el espaciado? Este parámetro es un porcentaje, cuánto entra el área a la del signo. Este parámetro se ve muy afectado por el diseño, el valor es un porcentaje de la alutra de x, para una tipografía de texto estándar puede ser entre 10 y 25.    

![paramDepth](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramDepth.png?raw=true)

5. __Overshoot__ (paramOver). Este parámetro expande el espacio medible hacia arriba o abajo de la altura de x. Con este parámetro podemos establecer diferencias en el espaciado de una `i` sans y una `l`, por ejemplo, entonces el signo con ascendente, la `l`, tendrá un espaciado más abierto que la `i`. El uso de este parámetro aumenta la posibilidad de afinar el seteo del espaciado y mejorar el resultado final. El valor corresponde a un porcentaje de la alutra de x. Este parámetro suele ser similar al valor de overshoot de la fuente.

![paramOver](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramOver.png?raw=true)

Entonces una vez que sabemos que parámetro calcula qué blanco, podremos ir probando/experimentando rapidamente desde esta ventana diferentes valores hasta lograr el espaciado que queremos.    
Personalmente comienzo con una secuencia de `n` para definir el parámetro área, luego incorporo la `o` y empiezo a ver el valor del parámetro depth, luego agrego la `c`, la `v` y sigo afinando el ajuste, por último, veo que ocurre con `i`, `j` y `l` para definir el overshoot. Por último voy componiendo palabras, frases y ajusto pequeñeces para revisar que el resultado me agrade.    

![Pruebas de seteo](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/pruebas-de-parametros.gif?raw=true)

Es importante recordar que para aplicar el espaciador los glifos deben estar seleccionados.    

#### Paso 4 → Pasar los valores a cada máster    

Retomando con el paso anterior, la ventana es para realizar experimentos, pruebas, no guarda los valores si vamos probando cosas diferentes de un master a otro. Por tal motivo, cuando logramos un espaciado que funciona, debemos cargar esos parámetros en cada máster, hacemos click en _copy parameter_ en la ventana emergente del HT Letterspacer.

![UI Window copiar parámetros](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/ui-window-copy-parameter.png?raw=true)

Vamos a _Información de la fuente > Máster_ y pegamos los valores en la ventana _Parámetros personalizados_.   
También podemos anotar los números y tipear en la ventana _Parámetros personalizados_ en la columna _propiedades_ `paramArea` `paramDepth` `paramOver` y en la columna _valor_ el número corresponiente según los resultados de las pruebas realizadas.

![copiar los parámetros en el mater info custom parameter](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/fonr-info-window-copy-parameters.png?raw=true)

#### Paso 5 → Aplicar el HT Letterspacer a toda la fuente

Ahora que ya están los parametros del espaciador aplicados en el máster, podemos hacer correr el macro en toda la fuente, sencillamente seleccionamos todos los glifos y vamos a _script > HTLetterspacer > HTLetterspacer_

![Script / HTLetterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer-a-toda-la-fuente.png?raw=true)

Esto deberás repetirlo por cada máster e ir revisando y testeando los resultados. Si necesitas modificar alguno de los valores, puedes hacerlo desde la ventana _Información de la fuente > Máster_ o volver a experimentar con la ventana emergente, esto último es lo más ágil.


#### Parámetros y archivo de configuración    

Estos parámetros que definimos los establecimos en función de las minúsuclas, son generales y aplican más o menos bien con la mayoría de los signos, pero si buscamos un resultado final de excelencia necesitamos ajustar aún más estas generalidades y personalizarlas a cada caso, a cada grupo de signos, ya que claramente el espaciado en las mayúsuclas, las versalitas, los números necesitan ser ajustadas, las mayúsculas y las versalitas deberían tener un espaciado más olgado y cada subcategoría de figuras tiene sus particularidades, la puntuación… aquí es donde el archivo de configuración que se generó automáticamente en el __paso 2__ entra en escena, donde los criterios de categorías y subcategorías harán el ajuste final.

Si abrimos con un editor de texto el archivo `nombredetufuente_autospace.py` que está en la misma carpeta que tu archivo `.glyph` encontraremos esto:

![archivo de configuración](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/archivo-py.png?raw=true)

Este archivo tiene una serie de ajustes básicos a los parámetros generales.    
Si observamos en el primer grupo leemos:    

> Letras y debajos 4 líneas indicando que algo ocurre con uppercase (mayúsculas), smallcaps (versalitas), lowercase (minúsuclas) y las lowercase .sups (letras voladas)


#### Links relacionados
- [Letter Spacer macro by Huerta Tipográfica, Andrés Torresi](https://youtu.be/FrFGD3tzqig) 
- [Using Letter Spacer script with serif typeface, by Huerta Tipográfica](https://youtu.be/secaaoidYI0)
- [Typo Lab Talk 2018 - English](https://www.typotalks.com/videos/ht-letterspacer-everything-you-always-wanted-to-know-about-automatic-spacing-but-were-afraid-to-ask/)

- [Domektica](https://www.domestika.org/es/blog/399-ht-letterspacer-revoluciona-el-sistema-de-espaciado-de-fuentes)

©HUERTA TIPOGRÁFICA | [MORE INFO](https://www.huertatipografica.com/en) | [GITHUB](https://github.com/huertatipografica/HTLetterspacer)


#### Bibliografia
- [Espaçamento de fontes, Eduardo Novais](https://tipodafonte.wordpress.com/2016/12/13/espacamento/#more-2077)
- [FreeType Glyph Conventions: 1 Basic Typographic ConceptsI](https://www.freetype.org/freetype2/docs/glyphs/glyphs-1.html)
- [FreeType Glyph Conventions: II Glyph Outlines](https://www.freetype.org/freetype2/docs/glyphs/glyphs-2.html)
- [FreeType Glyph Conventions: III Glyph Metrics](https://www.freetype.org/freetype2/docs/glyphs/glyphs-3.html)
- [How to Space a Font. FontLab Studio 5 tutorial with Thomas Phinney.](https://youtu.be/tbc_O7bNROs)
- [Huerta Tipografica](https://huertatipografica.github.io/HTLetterspacer/)
- [I love typography, Typography Terms (S), a glossary of typographic terms - October 9, 2007](https://ilovetypography.com/typography-terms/typography-terms-s/)
- [LS CADENCER TOOLS,  Frank E. Blokland](https://www.revolvertype.com/tools/)
- [On the Origin of Patterning in Movable Latin Type](https://www.lettermodel.org/)
- [Stan Nelson: Making Type](https://typography.guru/video/stan-nelson-making-type-r27/)




