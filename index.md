### Como utilizar HT-Letterspacer    

#### Paso1 → [Descargar HT-Letterspacer](https://github.com/huertatipografica/HTLetterspacer)

Descargar y seguir las instrucciones de instalación

#### Paso 2 → Utilización inicial del HT-Letterspacer, archivo .py

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

Ahora que ya están los parametros del espaciador aplicados en el master, podemos hacer correr el macro en toda la fuente, sensillamente seleccionamos todos los signos y vamos a _script > HTLetterspacer > HTLetterspacer_

![Script / HTLetterspacer](https://github.com/CaroGiovagnoli/HTLetterspacer-tutorial/blob/master/img/08-script-htls.png?raw=true)



#### Links relacionados:    
- [Letter Spacer macro by Huerta Tipográfica, Andrés Torresi](https://youtu.be/FrFGD3tzqig)    
- [Domektica](https://www.domestika.org/es/blog/399-ht-letterspacer-revoluciona-el-sistema-de-espaciado-de-fuentes)
