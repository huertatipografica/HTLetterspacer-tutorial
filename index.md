# Como utilizar HT Letterspacer    

> Esta __herramienta__ fue creada para diseñar el espaciado de una fuente tipográfica, la desarrolló Andrés Torresi y es de distribución libre.    
> Aunque corre como un macro en el editor de fuentes [Glyphs](https://glyphsapp.com/), el __método__ de espaciado que propone puede ser adaptado a otros editores o lenguajes de programación.    
> El HT Letterspacer puede ser utilizado en fuentes simples con un solo master o en fuentes múltiple máster o superfamilias, se adapta a diferentes sistemas de escritura y puede ser aplicado durante la etapa de diseño o en fuentes ya terminadas. No está desarrollado para hacer kerning, sino para diseñar el espacio a la derecha e izquierda de los signos.    
> En el [Home page de HT Letterspacer](https://huertatipografica.github.io/HTLetterspacer/) y en el [repositorio GitHub](https://github.com/huertatipografica/HTLetterspacer) puedes encontrar más información sobre el desarrollo de esta herramienta.    
> Puedes descargarla gratuitamente del siguiente [link](https://huertatipografica.github.io/HTLetterspacer/).    

#### La magia no existe, son horas de trabajo    

Lo primero que deberías saber es que HT Letterspacer no es una *varita mágica*, no reemplaza al diseñador, el HT Letterspacer es una __herramienta__ y como tal debes aprender a utilizarla, debes aprender a configurar sus parámetros generales y debes aprender a modificar el archivo de configuración externa, en resumen, debes aprender a pensar el espaciado a través de esta nueva perspectiva y en este sentido estás frente a un cambio de paradigma, pues el espaciador propone un nuevo método.     

Al diseñar una letra, diseñas el negro y el blanco, el trazo y el espacio que lo rodea.    

Esta herramienta propone un método para pesar, diseñar y definir el espacio a la izquierda y a la derecha de un signo utilizando un grupo de parámetros generales que luego son ajustados en un archivo de configuración.    

El espaciado es una cuestión de diseño, los diseñadores de tipografía diseñamos el blanco que rodea a un signo, esas decisiones son afectadas por la forma y contraforma, el dibujo, las proporciones, el estilo, la función, el soporte y los demás items descriptos en su brief.    

Esta es una herramienta para diseñadores, no hay parámetros mágicos, hay un diseñador de tipografía con un brief que le marca el norte, el HT Letterspacer le permite realizar pruebas y experimentar diferentes posibilidades hasta lograr el espaciado que su tipografía requiere.    


#### Paso 1 → Descarga e instalación

Para comezar, descarga HT Letterspacer del [repositorio GitHub](https://github.com/huertatipografica/HTLetterspacer), y al ser un script de payton que corre en el editor de fuentes Glyphs, debes tener esta aplicación instalada.

![ventana de git hub](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/descargar-ht-de-git-hub.png?raw=true)

Para descargarlo puedes utilizar la applicación de GitHub Desktop, descargar el archivo .zip y descomprimir o descargarlo desde la terminal.

En el editor de fuentes Glyphs debes seguir los siguientes pasos:

1. Abrir las preferencias de Glyphs, menú _Glyphs > preferencias_ (`Cmd⌘-` `,`), en la ventana de preferencias, ir a la sección _Addons > Modules_ y hacer click en _Install Modules_.    

![install modules image](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/glyph-preferences-install-modules.gif?raw=true)

2. Ir al menú _Script > Abrir la carpeta de Scripts_ (Cmd⌘-Shift⇧-Y) y cerrar la aplicación Glyphs. Se abrirá en el escritorio la carpeta donde Glyphs guarda los _scripts_.

![Abrir la ventana de scripts](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-open-script-folder-sin-ht-letterspacer.png?raw=true)

En esta carpeta podrás encontrar los _scripts_ que ya tienes instalados, o si no has intalado ninguno, una carpeta vacía.

![scripts folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-folder.png?raw=true)

3. Colocar aquí la carpeta que descargaste en el paso 1.

![add img to scripts glyph's folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/add-ht-to-scripts-folder.gif?raw=true)

4. Volver a Glyphs e ir al menú _Script_ presionando la tecla `Opt ⌥`, de esta manera al desplegar el menú en lugar de _abrir ventana de scripts_ ahora podrás ver al final la opción _Reload Scripts_, esta acción actualizará dicha carpeta y podrás ver entre las opciones de _scripts_, _HTLetterspacer_.    
► Una forma práctica de acutalizar la carpeta de _script_ es precionar  `Cmd⌘ Opt⌥` `Schift⇧` `Y`    

![script palet con ht letterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer.png?raw=true)

5. __Opcional:__ cuando ya estés trabajando con el HT Letterspacer puedes utilizar un glifo de prueba llamado `_areas`, para esto deberías descargar `objectsGS.py` y `GSPen.py` del [repositorio de Glyphs-Scripts](https://github.com/schriftgestalt/Glyphs-Scripts) y ponerlos en la carpeta _Scripts_ (similar a lo que hiciste en los puntos 2, 3, 4 y 5). Estos _scripts_ siven para generar ese glifo `_areas`.    
    

> ### A continuación las 3 instancias de trabajos: 

> 1. Definir los parámetros generales para las minúsculas en el editor de tipografía → Paso 2 y 3.
> 2. Pasar esos parámetros generales a cada máster → Paso 4.
> 3. Adaptar esos parámetros a las otras categorías de signos en el archivo → Paso 5.    

 
#### Paso 2 → Utilización inicial del HT Letterspacer

Has empezado a diseñar nuestra fuente tipográfica, ya tienes un par de signos, por ejemplo una `n`, una `o` , una `v`, una `c` y ahora debes diseñar el blanco que los rodea, o sea, el espaciado. Aquí es donde comienzas a utilizar esta herramienta de espaciado.    

Pero antes debes resolver un pequeño asunto. La primera vez que accedas al menú _script > HTLetterspacer_ y se desplieguen las 2 opciones: HTLetterspacer UI y HTLeterspacer, antes que puedas elegir una de ellas se abrirá una ventana de diálogo indicando que falta un _archivo de configuración_ y preguntando si queremos crearlo, recomiendo responder __Yes!__   

![missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/missing-config-file-window.png?raw=true)

De esta manera se genera automáticamente un archivo `.py` en la misma carpeta donde has guardado el archivo `mifuente.glyph`. Si vas a esa carpeta encontrarás un nuevo archivo llamado `elnombredetufuente_autospace.py`, este era el _archivo de configuración faltante_, hablaremos de él más adelante.    

![Ventana missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/config-file-folder.png?raw=true)

#### Paso 3 → Primera aproximación al diseño de espaciado. Definición de los parámetros generales

> En esta sección hablaré de diseño de espaciado propiamente dicho y de cómo utilizar el HT Letterspacer para espaciar una fuente tipográfica.    
> Pero antes quisiera hacer una breve introducción para ponernos a todos en el mismo punto de partida y evitar malentendidos, ambigüedad o desencuentros semánticos. Quiero definir los siguientes puntos:    
> - ¿Qué es espaciado?    
> - ¿Qué factores podríamos considerar relevantes en la toma de partido del diseño del espaciado de una fuente?    
> - ¿Qué actores intervienen durante el proceso de espaciado?     
> - ¿Cómo estos actores están reflejados en los parámetros que HT Letterspacer propone?    

La novedad de esta herramienta es que nos desafía a pensar y a analizar el espaciado de una forma diferente, tal vez esto es lo que nos desorienta un poco en los primeros momentos. No es un botón mágico que arregla todo.

Espaciar es determinar cuánto espacio hay a la derecha y a la izquierda de un signo, cuánto aire lo rodea, es diseñar el blanco que nos deja leer el negro.    
Espaciar es equilibrar el espacio que hay dentro de la letra con el espacio que hay fuera de ella. 

![imagen espacio interno =~ espacio externo telder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/espacio-int-simliar-espacio-ext-telder.jpg?raw=true)
![imagen espacio interno =~ espacio externo alegreya](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/espacio-int-simliar-espacio-ext-alegreya.jpg?raw=true)

En este punto estamos todos más o menos de acuerdo, si hemos leímos sobre espaciado, la idea de igualar blancos internos-externos es recurrente. La imagen utilizada es similar: si para llenar el interior de una `n` necesito 1 litro de agua, también necesitaré 1 litro para llenar el espacio entre esa `n` y la letra que sigue. La gran pregunta es ¿es un litro, 0,8 o 1,2 litro?

Los métodos de espaciado propuestos por Walter Tracy, Thomas Phinney, Frank E. Blokland,  ponen el foco en las formas, agrupandolas, clasificándolas, analizandolas —rectas, curvas, diagonales, bastones, etcétera—.
HT Letterspacer propone observar el blanco, no se basa en la forma, la atención apunta al espacio y nos anima a mirarlo como una forma maleable, pues tenemos que determinar dónde empieza y termina ese blanco para dar lugar al negro.   

#### Criterios de diseño:    
Al empezar a pensar en rasgos generales cómo será el espaciado de una fuente, hay algunos datos que van a ir perfilando esa forma (blanca) estos ítem influyen en la toma de decisión. Por ejemplo, si tengo dos tipografías sans Serif para cuerpo de lectura, una en papel y otra en pantalla, la segunda tendrá un espaciado más generoso que la primera; o si tengo una tipografía para títulos y su variante de texto, la primera tendrá un espaciado más apretado.    
Hay factores que pueden ser un criterio de diseño:     
- diseño de los signos    
- proporciones    
- color    
- función    
- soporte    
- etc.    

#### Los actores que intervienen técnicamente son:
Cuando ya sabes que tipo de espaciado demanda tu tipografía y quieres utilizar el espaciador, hay un par de conceptos que necesitas conocer, de la misma manera que para dibujar un signo en un editor de tipografía sabes como funcionan las curvas de Bézier, los manejadores y los nodos. En el diseño de espaciado, los actores principales que intervienen son:    
- sidebearing (izquierdo y derecho)    
- contorno del glifo    
- bbox    
- ancho de caja    

> #### Mini glosario general:
> ► El __punto de origen__ es el punto cero en el eje x.    
> 
> ► El __ancho de la caja__ _(Advance width)_ es el ancho que avanza el signo, el límite izquierdo es el punto de origen (que coincide con el _sidebearing_ izquierdo) y el límite derecho es el _sidebearing derecho. El _ancho de caja_ está delimitado por lo laterales izquierdo y derecho, lo que ocurre entre estos laterales es ancho. Generalmente el ancho de caja es mayor a cero.    
> 
> ► Cuando hablo de __glifo,__ hago referencia al dibujo (a la forma, al negro) y al espacio que lo rodea.    
> 
> ► cuando hablo del __contorno__ hago referencia a la línea que dibuja la forma y contraforma, a la línea que dibuja el negro.    
> 
> ► los puntos extremos del contorno determinan el __Bouding Box (BBox)__. Dicho de otro modo, el __BBox__ es el rectángulo que circunscribe al contorno.    
> 
> ► __Sidebearing__ es el componente esencial del espaciado, es el espacio a la izquierda y a la derecha. Cada glifo tiene un sidebearing izquierdo llamado _Left Side Bearing (LSB)_ y un sidebearing derecho, _Right Side Bearing (RSB):_ __LSB__ es la distancia entre el punto de origen y el lado izquierdo del _BBox_. __RSB__ es la distancia entre el lado derecho del _BBox_ y el lateral derecho de la caja.    
> 
> ![imagen anatomía del signo](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/anatom%C3%ADa-del-glifo.jpg?raw=true)
> El espacio es lo que ocurre entre el límite de la caja y el contorno.


#### HT Letterspacer UI
El uso de esta herramienta tiene 3 momentos:    
- Definir los parámetros generales,    
- pasar los parámetros generales al o los máster y    
- configurar el archivo de ajuste.    

Para definir los parámetros recomiendo utilizar primero la ventana emergente `HT Letterspacer UI` (User Interface).    
Esta ventana es la que se abre una vez resuelto el asunto del archivo de configuración perdido (encontrado en el paso 2). Allí están los parámetros que debemos definir para diseñar el espaciado de nuestra tipografía.        

![Ventana emergente con explicación de los parámetros](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/parametros-explicacion.png?raw=true)
 

1. __LBS / RSB__ Con este parámetro indicas si el espacio debe ocurrir a la izquierda y a la derecha o solo de a un lado del signo.    

2. __Tabular.__ Este apartado está reservado para las figuras tabuladas y una fuente monoespaciada o de ancho fijo. Si tildas este parámetro, debes indicar cuál es el ancho de la caja.   

3. __Area__ `paramArea`. Este parámetro define el área a la izquierda y la derecha del BoudingBox, la superficie __rectangular__ entre el lado izquierdo (o derecho) del BoudingBox y el lateral izquierdo (o derecho) de caja, la línea base y la altura de x. El número que utilices para definir el valor de este parámetro está entre 0 y 1000, para una tipografía de texto podría ser entre 200 y 400.

![paramArea](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramArea.png?raw=true)



4. __Depth__ `paramDepth` (profunidad). Si todos los signos fueran rectos como el lado izquierdo de la `n` sans Serif geométrica el asunto del espaciado estaría resuelto y no estaríamos aquí discutiendo esto. ¿Qué ocurre con las contraformas abiertas, con las zonas blancas que están dentro del BBox y por lo tanto no son tomadas en cuenta en el parámetro área? ¿Cómo definimos las superficies blancas en una `c`, en una `v` o una `T`? ¿Hasta dónde es contraforma y donde empieza a ser espaciado?     
Hay una gran cantidad de blanco __dentro del BBox__ que incide en la ecualización del espacio. Para definir este parámetro es imprescindible un ojo bien entrenado, pues necesitamos determinar una _frontera visual,_ no hay ningún punto o línea que nos indique en qué momento el blanco interno de una `c` deja de ser espacio interior para ser espacio exterior, o en qué lugar, nuestro ojo deja de ver al espacio inferior de la `v` como contraforma para verlo como espaciado.
El número que utilizamos aquí es un porcentaje (una escala 0-100), e indica cuánto blanco debe medir hacia adentro del BBox, entre la línea de base y la altura de x. Para una tipografía de texto estándar puede ser entre 10 y 25.    

![paramDepth](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramDepth.png?raw=true)

5. __Overshoot__ `paramOver`. En los dos parámetros anteriores (_area_ y _depth_) el cálculo es dentro de la altura de x. Este parámetro expande el espacio medible hacia arriba y hacia abajo de la altura de x. Al considerar el espacio fuera de la altura de x, podemos establecer diferencias en el espaciado de una `i` sans, una `l` y una `j` , de una `a de anillo`, una `d` y una `q`. El uso de este parámetro aumenta la posibilidad de afinar el seteo del HT Letterspacer y optimizar el resultado final. El valor de este parámetro suele ser similar al valor de overshoot de la fuente.

![paramOver](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/paramOver.png?raw=true)

Entonces una vez que sabes que parámetro calcula qué blanco, puedes ir probando/experimentando rápidamente desde esta ventana diferentes valores hasta lograr el espaciado que quieres para tu tipografía.    

Personalmente comienzo con una secuencia de `n` para definir el __parámetro área,__ luego incorporo la `o` y empiezo a ver el valor del __parámetro depth__ agregando la `c`, la `v` y sigo afinando el ajuste, por último, veo que ocurre con `i`, `j` y `l` para definir el __parámetro overshoot.__ La secuencia se va transformando en palabras y frases que me permiten ajustar los detalles para revisar que el resultado me agrade.    

Como ya te habrás dado cuenta, esto no es simple, cuando crees haber encontrado el valor de `paramArea` agregas una `v` a la secuencia y todo se desacomoda, logras hallar el valor de `paramDepth` pero al agregar una `f` vuelve a desajustarse, modificas `paramArea` luego `paramOver` y reconsideras el valor de `paramDepth`. En este punto es importante saber qué modificas con cada parámetro, sino esto se vuelve realmente una lotería.

El testeo lo hago con las minúsculas. Las mayúsculas, figuras, símbolos, etc. tendrán un espaciado _parejo y armónico_ con estos valores, pero no óptimo, en el paso 5, podrás resolver esto.    

Otro punto importante de recordar es que si estás trabajando en una fuente que tiene un par de másters y cargas los valores para el máster light, luego vas al bold y cambias los valores para hacer pruebas allí, al volver al máster light, los valores que habías seteado serán los que cambiaste en el bold. Los valores en la ventana `HT Letterspacer UI` no quedan guardados, es una instancia de prueba. Recomiendo trabajar en un máster a la vez e ir pasando los parámetros al máster correspondiente.

![Pruebas de seteo](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/pruebas-de-parametros.gif?raw=true)    

##### Cómo pasar los valores a cada máster    

Una vez definidos los valores en la ventana emergente, debes cargarlos en el máster correspondiente, esto es bastante simple. En la ventana donde vienes trabajando haces click en `copy parameters` y vas a _Información de la fuente > Máster_ allí encontrarás una sección para los _Parámetros personalizados,_ en ese lugar debes pegarlos.   

![UI Window copiar parámetros](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/ui-window-copy-parameter.png?raw=true)

![copiar los parámetros en el mater info custom parameter](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/fonr-info-window-copy-parameters.png?raw=true)

También puedes anotar los valores, ir a la sección  _Parámetros personalizados_ y tipear en la columna _propiedades_ `paramArea` `paramDepth` `paramOver` y en la columna _valor_ el número corresponiente según los resultados de las pruebas realizadas.


> ##### Resumen    
> ► Es importante recordar que para aplicar el espaciador los glifos deben estar seleccionados.        
> ► Saber que parámetro corresponde a cada blanco te evitará trabajar a ciegas y jugar a la lotería.    
> ► La ventana NO GUARDA los valores.       
> ► Pasar los parámetros generales al máster.       
> ► Los parámetros generales se calculan contrastando minúsuclas, el resto de los signos tendrán un espaciado _parejo_ o _constante._ Podrás ajustar esto en el paso 5.    


#### Paso 4 → Aplicar el HT Letterspacer a toda la fuente

Ahora que ya están los parametros de espaciado aplicados en cada máster, puedes hacer correr el macro en toda la fuente, seleccionas todos los glifos y vas al menú _script > HTLetterspacer > HTLetterspacer_

![Script / HTLetterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer-a-toda-la-fuente.png?raw=true)

> Puede establecer un acceso a través del teclado para esta herramienta yendo a Preferencias del Sistema > Teclado, allí selecciona “Funciones rápidas de apps” a la izquierda, haz clic en el botón Añadir `+`, haz clic en el menú desplegable Aplicaciones y selecciona la app Glyphs. Si no está en la lista, selecciona Otra y, a continuación, busca las apps mediante el cuadro de diálogo Abrir. 
> En el campo “Título del menú”, escribe el comando del menú Script->HT_LetterSpacerUI. Haz clic en el campo “Función rápida de teclado”, pulsa la combinación de teclas que quieras usar como función rápida de teclado y, a continuación, haz clic en Añadir.   

Esto deberás repetirlo por cada máster e ir revisando los resultados. Si necesitas modificar alguno de los valores, puedes hacerlo desde la ventana _Información de la fuente > Máster_ o volver a trabajar con la ventana emergente, esto último es lo más ágil.


#### Paso 5 → Parámetros y archivo de configuración    

Como ya habrás advertido los parámetros generales logran un espaciado que se ajusta a las minúsculas pero las mayúsculas están _armónicamente_ apretadas.    
En el __paso 2__ leíste sobre un __archivo de configuración__, este archivo contiene las instrucciones para resolver este problema y ajustar los parámetros generales a las necesidades particulares de cada grupo de signos.    
Encontrarás este archivo en la misma carpeta donde está guardado el archivo de la fuente, se llama igual a ella más la extención `_autospace.py`. Al abrirlo con un editor de texto encontrás los siguiente:

~~~
# Reference
# Script, Category, Subcategory, value, referenceGlyph, filter

# Letters
*,Letter,Uppercase,1.25,H,*,
*,Letter,Smallcaps,1.1,h.sc,*,
*,Letter,Lowercase,1,x,*,
*,Letter,Lowercase,0.7,m.sups,.sups,

# Numbers
*,Number,Decimal Digit,1.2,one,*,
*,Number,Decimal Digit,1.2,zero.osf,.osf,
*,Number,Fraction,1.3,*,*,
*,Number,*,0.8,*,.dnom,
*,Number,*,0.8,*,.numr,
*,Number,*,0.8,*,.inferior,
*,Number,*,0.8,*,superior,

# Punctuation
*,Punctuation,Other,1.4,*,*,
*,Punctuation,Parenthesis,1.2,*,*,
*,Punctuation,Quote,1.2,*,*,
*,Punctuation,Dash,1,*,*,
*,Punctuation,*,1,*,slash,
*,Punctuation,*,1.2,*,*,

# Symbols
*,Symbol,Currency,1.6,*,*,
*,Symbol,*,1.5,*,*,
*,Mark,*,1,*,*,

# Devanagari
devanagari,Letter,Other,1,devaHeight,*,
devanagari,Letter,Ligature,1,devaHeight,*,
~~~

Si bien este archivo ya tiene una serie de valores estándar que funcionan más o menos bien, la idea es que puedas personalizarlo y ajustarlo a tus necesidades.    
De la misma manera que para ajustar los parámetros generales fueron definidos a los actores que intervienen (LBS, RBS, ancho de caja, etc.) aquí lo que debes aprender es a leer e interpretar este archivo para poder modificarlo a tu gusto.

En las primeras dos líneas se presenta comentado el esqueleto del documento (el `#` introduce un comentario sin valor de instrucción), esta secuencia se repite en los 5 grupos que el archivo tiene definidos por default. 
Los parámetros que declara son los siguientes:    

► `Script`: indica el sistema de escritura que afecta —latin, devanagari, cirílico, etc.— si usas `*` indicas que afecta a todos los scripts.     
► `Category`: indica qué categoría de signos —letters, numbers, punctuation, symbols— o `*` que incluye a todas las categorías.     
► `Subcategory`: describe las subcategorías, si la categoría es `letters` aquí podría ser `Uppercase`, `Lowercase`, `Ligature` `Small Caps` y `Superscript` o `*` que incluye a todas las subcategorías.     
► `value`: es el valor del coeficiente por el cual se multiplica el espacio definido en los parámetros generales. Si utilizas como valor `1` los valores indicados en `paramArea` `paramDepth` y `paramOver` serán aplicados sin modificación por lo tanto en la categoría `letters` subcategoría `lowercase` el valor que corresponde es `1`, para la subcategoría `uppercase` y `Small caps` como el espaciado debe ser más amplio será un valor mayor a `1` y para la `Superscript` será un valor menor a `1`.    
► `referenceGlyph`: este signo de referencia es el que determina la altura de x, el límite vertical de los parámetros generales, en las minúsculas sería una `x` en las mayúsculas sería una `H`. Es importante tenerlo en cuenta para las letras o números volados, pues estos signos se desarrollan casi en su totalidad fuera de la altura de x, entonces en la subcategoria `Superscript` el signo de referencia debería ser `x.susp`     
► `filter`: aquí puedes especificar un grupo de glifos según su nombre o extensión, por ejemplo `.ss01` o sencillamente `*` que designa a todos los nombres.     

![imagen con explicacion](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/archivo-de-cofiguracion.png?raw=true)

Es importante mencionar que no es posible excluir signos, no puedes establecer excepciones. 
Si hay signos que no quieres que sean afectados por el HT Letterspacer lo que debes hacer es no seleccionarlos en el archivo .glyphs cuando pasas el espaciador.

Otra opción es no pensarlo desde la excepción, sino incluirlo en esa situación a través de un filtro y transformarlo en una particularidad dentro de una categoría/subcategoría. Por ejemplo, deseo espaciar los números romanos, pero el espaciador toma las barras superior e inferior y no aplica el espaciado. Entonces:

~~~
#Numeros Romanos
Latin,Letter,Lowercase,1.5,RomanNumbersHight,.ss02,
~~~

Donde:    
► `Latin` > sistema de escritura.    
► `Letter` > categoría.    
► `Lowercase` > subcategoría.    
► `1.5` > valor.    
► `RomanNumbersHight` > Glifo de referencia, genero este glifo de referencia que redefine la altura de x.    
► `ss02` > Filtro, aquí es donde la _excepción_ es incluida como particularidad dentro de un grupo, los ss02.    

![imagen de reference glyph](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/reference-glyph.png?raw=true)

Otro ejemplo podría ser:
~~~
Latin,Letter,Uppercase,1.25,H,*,
Latin,Letter,Uppercase,1.4,H,E,
~~~

Observa la primera línea, donde el valor del parámetro `filter` es `*`, y en la segunda línea el valor `E`. Esto se lee: todas las mayúsculas usarán la letra H como referencia, y aplicará a todas las mayúsculas el coeficiente 1.25, pero en la segunda línea hay una nueva nueva regla que indica que para el filtro `E` el coeficiente será 1.4.

Creo que la clave para aprovechar al máximo las posibilidades de ajuste está en el sistema de categorías y subcategorías, filtros y referencias.

Una fuente es un sistema que contiene subsistemas, cada diseñador piensa sus categorías y subcategorías de manera que lo ayuden a ordenar el trabajo, a establecer una metodología, a definir criterios y fronteras.



#### Links relacionados
- [Letter Spacer macro by Huerta Tipográfica, Andrés Torresi](https://youtu.be/FrFGD3tzqig) 
- [Using Letter Spacer script with serif typeface, by Huerta Tipográfica](https://youtu.be/secaaoidYI0)
- [Typo Lab Talk 2018 - English](https://www.typotalks.com/videos/ht-letterspacer-everything-you-always-wanted-to-know-about-automatic-spacing-but-were-afraid-to-ask/)

#### Bibliografia
-El trazo. Teoría de la escritura. Gerrit Noordzij. Traducción Carlos García Aranda. 2009. Campgràfic Editors     
- [Espaçamento de fontes, Eduardo Novais](https://tipodafonte.wordpress.com/2016/12/13/espacamento/#more-2077)    
- [FreeType Glyph Conventions: 1 Basic Typographic ConceptsI](https://www.freetype.org/freetype2/docs/glyphs/glyphs-1.html)    
- [FreeType Glyph Conventions: II Glyph Outlines](https://www.freetype.org/freetype2/docs/glyphs/glyphs-2.html)    
- [FreeType Glyph Conventions: III Glyph Metrics](https://www.freetype.org/freetype2/docs/glyphs/glyphs-3.html)    
- Hacer y Componer, Francisco Gálvez Pizarro, Ediciones UC, Chile, 2018.    
- [How to Space a Font. FontLab Studio 5 tutorial with Thomas Phinney.](https://youtu.be/tbc_O7bNROs)    
- [Huerta Tipografica](https://huertatipografica.github.io/HTLetterspacer/)    
- [I love typography, Typography Terms (S), a glossary of typographic terms - October 9, 2007](https://ilovetypography.com/typography-terms/typography-terms-s/)    
- Los elementos del estilo tipográfico, versión 3.1, Robert Bringhurst, primera edición en español 2008.    
- [LS Cadencer Tools, Frank E. Blokland](https://www.revolvertype.com/tools/)    
- [On the Origin of Patterning in Movable Latin Type](https://www.lettermodel.org/)    
- [Stan Nelson: Making Type](https://typography.guru/video/stan-nelson-making-type-r27/)    


©HUERTA TIPOGRÁFICA | [MORE INFO](https://www.huertatipografica.com/en) | [GITHUB](https://github.com/huertatipografica/HTLetterspacer)

============
