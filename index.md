# Como utilizar HT Letterspacer    

> El HT Letterspacer es una __herramienta__ desarrollada por Andrés Torresi para __diseñar__ el espaciado de una fuente tipográfica. Se puede utilizar durante el proceso de diseño o en fuentes terminadas.   
>    
> La primera versión de esta herramienta funciona como una macro en el editor de fuentes [Glyphs](https://glyphsapp.com/) y utliza las categorías y subcategorías como criterio de organización pero este método puede ser adaptado a otros editores o lenguajes de programación.    
>    
> HT Letterspacer no hace kerning, solo sirve para definir el espacio a derecha-izquierda de los signos.    
>    
> Para informarte más sobre esta __herramienta__ puedes visitar:
>  [Home page de HT Letterspacer](https://huertatipografica.github.io/HTLetterspacer/)    
>     
> Es una herramienta libre y puedes descargarla de manera gratuita en este [repositorio](https://github.com/huertatipografica/HTLetterspacer) de GitHub. Allí encontrarás las instrucciones de instalación.    
            
### Esta herramienta no reemplaza al diseñador de tipografía    
Los primero que debes saber de HT Letterspacer es que no es una *varita mágica*, no reemplaza al diseñador, es una herramienta y como tal debes aprender a usarla, debes configurar sus parámetros de funcionamiento para que se ajuste a la tipografía que estás desarrollando.    
La configuración por default da resultados aceptables para un principiante pero si quieres obtener un resultado excelente deberás *settear* este *script* y adaptarlo a las particularidades y diseño de tu tipografía.
Descargar y seguir las instrucciones de instalación.    

### El concepto detrás de HT Letterspacer
Esta herramienta es un método para definir el blanco lateral (derecha-izquierda) de un glifo y establecer una forma de medirlo utilizando 3 parámetros. Estos parámetros se definen para las letras minúsculas y luego se modifican y adaptan para los diferentes signos –aquí es donde utiliza las categorías y subcategorías de glifos de Glyphs— en un archivo de configuración externo (`elnombredenuestrafuente_autospace.py`). Explicaremos esto más adelante.    

Esta herramienta tiene 2 instancias de trabajo:    

- Definición de los parámetros para las minúsculas en el editor de tipografía a través de la ventana emergente `HT Letterspacer UI`
- Adaptación de esos parámetros a las otras categorías de signos en el archivo de configuración `elnombredenuestrafuente_autospace.py`.

Esta herramienta funciona en fuentes simples o en superfamilias con varios masters, si deseas experimentar con diferentes criterios de espaciados puedes hacer pruebas de manera simple y ver rápidamente los resultados.    
También puedes utilizar esta herramienta con las figuras tabulares o fuentes monoespaciadas o de ancho fijo, usando la opción `tabular`.

Es una herramienta para diseñadores, no hay parámetros mágicos, cada diseñador puede hacer sus propios experimentos hasta encontrar su propio criterio para lograr el diseño de espaciado que desea. El espaciado de una fuente es una cuestión de diseño, los diseñadores de tipografía diseñamos el blanco que rodea a un signo, tomamos muchas desiciones basados en las proporciones y el dibujo de los signos, el HT Letterspacer es una herramienta para diseñar este espacio.

### Paso 1 → Descarga e instalación

Como ya dijimos, este script se ejecuta en el editor de tipografía Glyphs.

1. Abrir las preferencias de Glyphs (Cmd⌘-,), ir a la sección Addons/Modules y hacer click en _Install Modules_.    

![install modules image](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/glyph-preferences-install-modules.gif?raw=true)

2. Ir a _Script > Abrir la carpeta de Scripts_ (Cmd⌘-Shift⇧-Y) y cerrar la aplicación Glyphs.

![Abrir la ventana de scripts](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-open-script-folder-sin-ht-letterspacer.png?raw=true)

![scripts folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-folder.png?raw=true)

3. Descargar la última versión de HT Letterspacer del [repositorio](https://github.com/huertatipografica/HTLetterspacer) y colocar esa carpeta dentro de la carpeta Scripts que se abrió en el paso 2.

![add img to scripts glyph's folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/add-ht-to-scripts-folder.gif?raw=true)

4. Volver a Glyphs e ir a _Script_ con la tecla Opt⌥- presionada y al desplegarse esa ventana ahora encontrarás al final la opción _Reload Scripts_ o simplemente hacer Cmd⌘ Opt⌥-Schift⇧-Y, ya que con esta acción se actualizará dicha carpeta y podrás ver entre las opciones _HTLetterspacer_

![script palet con ht letterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer.png?raw=true)

5. __Opcional:__ para poder dibujar el glifo de prueba deberías bajar objectsGS.py and GSPen.py del [repositorio](https://github.com/schriftgestalt/Glyphs-Scripts) de [Glyphs-Scripts] y ponerlos en la carpeta `Scripts` (similar a lo que hiciste en los puntos 2, 3 y 4). Esto genera un glifo llamado `_areas`.


### Paso 2 → Utilización inicial del HT Letterspacer

Hemos empezado a diseñar nuestra fuente tipográfica, ya tenemos un par de signos, por ejemplo una `n`, una `o` , una `v`, una `c` y ahora debemos diseñar el blanco que los rodea, o sea, el espaciado. Aquí es donde empezamos a utilizar nuestra herramienta de espaciado.    

Antes debemos resolver un pequeño asunto. La primera vez que utilizamos el espaciador con una tipografía vamos a _script > HTLetterspacer_ y se despliegan las 2 opciones (HTLetterspacer UI y HTLeterspacer), pero antes que podamos selccionar una de esas opciones se abrirá una ventana de diálogo que nos indica que falta un archivo de configuración y nos pregunta si queremos crearlo, a lo que debemos responder **Yes**.   

![missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/missing-config-file-window.png?raw=true)

De esta manera se genera automáticamente un archivo `.py` en la misma carpeta donde has guardado el archivo `.glyph`. Si vamos a esa carpeta donde está guardada la tipografía encontraremos un nuevo archivo llamado `elnombredenuestrafuente_autospace.py`, este era el archivo de configuración faltante, hablaremos de él más adelante.    

![Ventana missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/config-file-folder.png?raw=true)

#### Paso 3 → Primera aproximación al diseño del espaciado. Definición de los parámetros generales

Esta etapa es de prueba y contraprueba desde la ventana emergente del HT Letterspacer UI (User Interface).    

Resuelto el asunto del archivo de configuración faltante se abrirá la ventana emergente del espaciador. Allí están los parametros que debemos ajustar para definir el espaciado de nuestra tipografía.        

![Ventana emergente con explicación de los parámetros](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/parametros-explicacion.png?raw=true)
 

1. __LBS / RSB.__ _Left / Right Side Bearings_, si ambos están tildados, indica que el espaciado se aplica a la derecho e izquierda del signo.     

2. __Tabular.__ Es item es para las figuras tabuladas, o una fuente monoespaciada o de ancho fijo. Si tildamos este parámetro, debemos indicar cuál es el ancho del signo.   

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
