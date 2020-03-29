## Como utilizar HT Letterspacer    

> El HT Letterspacer es una __herramienta__ desarrollada por Andrés Torresi para __diseñar__ el espaciado de una fuente tipográfica. Se puede utilizar durante el proceso de diseño o en fuentes terminadas.   
>    
> La primera versión de esta herramienta funciona como un macro en la editor de fuentes [Glyph](https://glyphsapp.com/) y utliza las categorias y subcategoriás como criterio de organización pero este método puede ser adaptado a otros editores o lenguajes de programación.    
>    
> HT Letterspacer no hace kerning, solo sirve para definir el espacio a derecha-izquierda de lo sisgnos.    
>    
> Para informarte más sobre esta __herramienta__ pudes visitar 
>  [Home page de HT Letterspacer](https://huertatipografica.github.io/HTLetterspacer/)    
>     
> Es una herramienta libre y puedes descargar de manera gratuita [en este repositorio de GitHub](https://github.com/huertatipografica/HTLetterspacer) allí encontrarás instrucción es de instalación.    
    
&nbsp;
        
#### Esta herramienta no reemplaza al diseñador de tipografía    
Los primero que debes saber de HT Letterspacer es que no es una *bartita mágica*, no reemplaza al diseñador, es una herramienta y como tal debes aprender a usarla, debes configurar sus parámetros de funcionamiento para que se ajuste a la tipografía que estás desarrollando.    
La configuración por default da resultados aceptables para un principiante pero si quieres obtener un resultado excelente deberás *settear* este *script* y adaptarlo a las particularidades y diseño de tu tipografía.
Descargar y seguir las instrucciones de instalación.    

#### El concepto detrás de HT Letterspacer
Esta herramienta es un método para definir el blanco lateral (derecha-izquierda) de un glifo y establece una forma de medirlo y utilizando 3 parámetros. Estos parámetros se definen para las letras minúsculas y luego se modifican y adaptan para las diferentes signos –aquí es donde utiliza las categorías y subcategorías de glifos de Glyphs— en un archivo de configuración externa (`elnombredenuestrafuente_autospace.py`) . (Explicaremos esto más adelante).    

Esta herramienta tiene 2 instancias de trabajo:    

- Definición de los parámetos para las minúsculas en el editor de tipografía a través de la ventana emergente `HT Letterspacer UI`
- Adaptación de esos parámetros a las otras categorías de signos en el archivo de configuración `elnombredenuestrafuente_autospace.py`.

Esta herramienta funciona en fuentes simples o en superfamilias con varios masters, si deseas experimentar con diferentes criterios de espaciados puedes hacer pruebas de manera simple y ver rápidamente los resultados.    
Tambieen puedes utilizar esta herramienta con las figuras tabulares o fuentes monoespaciadas o de ancho fijo, usando la opción `tabular`.

Es una herramienta para diseñadores, no hay parámetros mágicos, cada diseñador puede hacer sus propios experimentos hasta encontrar su propio criterio para lograr el diseño de espaciado que desea. El espaciado de una fuente es una cuestión de diseño, los diseñadores de tipgorafía diseñamos el blanco que rodea a un signo, tomamos muchas desiciones basadas en las proporciones y el dibujo de los signos, el HT Letterspacer es una herramienta para diseñar este espacio.

#### Paso 1 → Descarga e instalación

Como ya digimos, este script corre en el editor de tipografía Glyph

1. Abrir las preferencias de Glyph (Cmd⌘-,), ir a la sección Addons/Modules hacer click en _Install Modules_.    

![install modules image](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/glyph-preferences-install-modules.gif?raw=true)

2. Ir a _Script > Abrir la carpeta de Scripts_ (Cmd⌘-Schift⇧-Y) y cerrar la aplicación Glyphs.

![Abrir la ventana de scripts](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-open-script-folder-sin-ht-letterspacer.png?raw=true)

![scripts folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-folder.png?raw=true)

3. Descargar las última versión de HT Letterspacer del respositorio [GitHub](https://github.com/huertatipografica/HTLetterspacer) y coloca esa carpeta dentro de la carepta Scripts que se abrió en el paso 2.

![add img to scripts glyph's folder](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/add-ht-to-scripts-folder.gif?raw=true)

4. Volver a Glyphs e ir a Script con la tecla Opt⌥- presionada y al desplegarse esa ventana ahora encontrarás al final _Reolad Scripts_ o simplemente hacer Cmd⌘ Opt⌥-Schift⇧-Y, con esta acción se actualizará dicha carpeta y podrás ver entre las opciones _HTLetterspacer_

![script palet con ht letterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/script-con-ht-letterspacer.png?raw=true)


#### Paso 2 → Utilización inicial del HT Letterspacer, archivo .py

Hemos empezado a diseñar nuestra fuente tipográfica, ya tenemos un par de signos, por ejemplo una `n`, una `o` y una `v`, ahora debemos diseñar el blanco que los rodea, o sea el espaciado.    
De la manera tradicional compondría una línea de nnnnnnn, mido el espacio interior de la `n`, lo divido por dos y ese espacio a cada lado, luego iría ajustando, una vez encontrado el espaciado que me gusta, iría agregando las otras letras a la secuancia, ajustando el espacio y buscando el ritmo que quiero que mi tipografía tenga.    

Con esta herramienta la dinámica es diferente.   
Una vez que tenemos una par signos diseñados vamos a _script > HTLetterspacer_ y se despliega otra subventana con 2 opciones:    
- HTLetterspacer UI    
- HTLeterspacer    
    
![Ventana HTLetterspacer UI y HTLetterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/01-script-htls-htls_UI.png?raw=true)

La primera vez que utilizamos el espaciador con una tipografía se abre una ventana de diálogo que nos dice que falta un archivo de configuración y pregunta si queremos crearlo, nuestra respuesta será SI.   

![Archivo .py](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/02-create-py-file.png?raw=true)

De esta manera se genera automáticamente un archivos `.py` en la misma carpeta a donde has guarado el archivo `.glyph`. Por lo tanto, en a la carpeta donde tenemos guardada nuestra fuente encontraremos un nuevo archivo llamado `elnombredenuestrafuente_autospace.py`, este era el archivo faltante, hablaremos de él más adelante.    

![Ventana missing config file](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/03-py-file.png?raw=true)

#### Paso 3 → Prueba y contraprueba desde la ventana emergente    

Resueltos el asunto del archivo perdido se abrirá la ventana emergente del espaciador.    
En ella encontrarás los parametros que debemos ir ajustando para definir el espaciado de nuestra tipografía. (Hablaremos sobre estos parámetros más adelante).       

![Ventana emergente](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/05-htls-window.png?raw=true)
 
Desde esta ventana podremos ir probando rapidamente diferenets valores hasta lograr el espaciado que queremos.    
Es recomendable primero espaciar una secuencia de nnn, a continuación podés agregar ooo y así sucesivamente el resto de las letras, luego repetir todo con las mayúsculas y las demás categorías y subcategorías de signos.    

![Pruebas de seteo](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/05-seteo-HTLS-UI.gif?raw=true)

#### Paso 4 → Pasar los valores a cada máster    

Cuando logramos un espaciado que funciona en nuestra tipografía, hacemos click en _copy parameter_ en la ventana emergente del HT Letterspacer, vamos a _Información de la fuente > Máster_ y pegamos los valores en la ventana _Parámetros personalizados_.   

![Copy custom parameter de la ventana emergente](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/06-htls-window-probar-copy-custom-parameter.png?raw=true)

![Ventana font info-master-custom parameter](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/07-font-info-customparameter.png?raw=true)

También podemos anotar los números y tipear en la ventana _Parámetros personalizados_ en la columna _propiedades_ `paramArea` `paramDepth` `paramOver` y en la columna _valor_ el número corresponiente según los resultados de las pruebas realizadas.

![custom parameter](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/07-custom-parameter.png?raw=true)

#### Paso 5 → Aplicar el HT Letterspacer a toda la fuente.

Ahora que ya están los parametros del espaciador aplicados en el máster, podemos hacer correr el macro en toda la fuente, sensillamente seleccionamos todos los glifos y vamos a _script > HTLetterspacer > HTLetterspacer_

![Script / HTLetterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/08-script-htls.png?raw=true)

Este paso puede llevar unos segundos/minutos, dependiendo de cuantos glifos tenga tu tipografía.    
Tendrás que repetir el proceso por cada máster e ir revisando ytesteando los resultados. Si  necesitas modificar alguno de los valores, puedes hacerlo desde la ventana _Información de la fuente > Máster_ o volver a experimentar con la ventana emergente, esto es más ágil.

### Parámetros y archivo de configuración    

`paramArea` `paramDepth` `paramOver` 

#### Links relacionados:    
- [Letter Spacer macro by Huerta Tipográfica, Andrés Torresi](https://youtu.be/FrFGD3tzqig) 
- [Using Letter Spacer script with serif typeface, by Huerta Tipográfica](https://youtu.be/secaaoidYI0)
- [Typo Lab Talk 2018 - English](https://www.typotalks.com/videos/ht letterspacer-everything-you-always-wanted-to-know-about-automatic-spacing-but-were-afraid-to-ask/)

- [Domektica](https://www.domestika.org/es/blog/399-ht letterspacer-revoluciona-el-sistema-de-espaciado-de-fuentes)

©HUERTA TIPOGRÁFICA | [MORE INFO](https://www.huertatipografica.com/en) | [GITHUB](https://github.com/huertatipografica/HTLetterspacer)
