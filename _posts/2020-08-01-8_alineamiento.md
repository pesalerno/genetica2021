---
layout: default
order: 8
title:  "Taller de alineamiento"
date: 2020-08-01
time:   "viernes 21 Ago"
categories: main
instructor: "Pati"
materials: ""
material-type: ""
lesson-type: autoguiada, evaluada
---

<a href="https://pesalerno.github.io/genetica-ago-2020/main/2020/06/08/7_geno-feno-2.html"><button>Actividad Anterior</button></a>		<a href="https://pesalerno.github.io/genetica-ago-2020/"><button>Inicio</button></a>    <a href="https://pesalerno.github.io/genetica-ago-2020/main/2020/06/09/9_proyectos-2.html"><button>Siguiente Actividad</button></a>

# Taller de alineamiento 




> -------------------
> 
> **VIERNES 9-10:30am** | Sesión Sincrónica para discutir el contenido de las dos actividades anteriores (*'Genotipo a Fenotipo'*) y para discutir cómo funcionará el taller de alineamiento. 
> 
> ------------------------ 
 
 
Los alineamientos de genes sirven para muchas cosas: nos ayudan a reconstruir historias evolutivas de grupos taxonómicos, nos permiten identificar "variantes" clínicos para identificar alelos responsables de ciertas patologías/cánceres, nos permiten describir poblaciones de animales en peligro de extinción y su capacidad adaptativa, entre muchas otras aplicaciones. 

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/rDNA.png?raw=true)<br>

En este taller, aprenderemos lo básico acerca de los marcadores genéticos y su historia, y de cómo los marcadores ribosomales - como el 16s - son usados para estudiar la mayor cantidad de vida en el planeta. Entenderemos lo díficil que es el concepto de "homología" con genética, despues de todo teniendo sólo cuatro bases, la probabilidad es altísima de que dos `A` sean iguales debido a homología o a convergencia, lo cual se hace particularmente difícil dada la estructura del `rRNA`. 


>--------------------------
>
>**VIDEO:** En [este video](https://www.loom.com/share/38d12458cff845ca8fc47d7ab8302e1a) de ~20min les doy una introducción a los marcadores genéticos y sus usos.
>
>--------------------------
>
>**VIDEO:** En [este video](https://www.youtube.com/watch?v=wdS3j0TgbjM) de ~5min podrán entender todos los pasos y los detalles de la secuenciación Sanger, técnica que revolucionó el estudio de la genética desde hace ya más de cuatro décadas y que sigue siendo usada para generar la mayor cantidad de secuencias del mundo. 
>
>--------------------------



## Comenzando con bajar nuestras secuencias


Primero, escojan su grupo de estudio, el cual debe ser relativamente "pequeño", respecto al árbol de la vida: un género, una especie, como mucho una familia. De ese grupo taxonómico que escogieron, deben bajar un total de 10 secuencias del marcador `16S rRNA`, un fragmento ribosomal codificado por la mitocondria, y el cual es comúnmente secuenciado para una gran variedad de eucariotas. 


Segundo, vayan a la [página de NCBI](https://www.ncbi.nlm.nih.gov/nuccore/) donde pueden acceder a las secuencias genéticas disponibles públicamente. Allí, deben hacer una búsqueda, en el caso mío, yo busqué `16S Pseudacris`, el cual es un género de ranas arborícolas de Norteamérica. 

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/ncbi.png?raw=true)<br>

Cuando salen los resultados, ven que hay un montón!! ademas de eso, noten los nombres de los archivos... algunos contienen sólo la secuencia del gen, pero otros contienen un mónton de otros genes (12s por ejemplo).



Entonces, intenten escoger casi todos que únicamente contengan 16s, pero si tienen alguno que tenga más genes (tanto `downstream` como `upstream`), entonces lo pueden agregar. Básicamente, lo que ocurre es que a veces la gente amplifica y secuencia segmentos mitocondriales bastante grandes, por lo que verán que los nombres de las secuencias pueden contener genes adyacentes. 

>Para referencia, así se ve el genoma mitocondrial de los eucariotas (es decir, de ustedes): 
>
>![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/mtDNA-genome.png?raw=true)<br>
>


Regresando a la búsqueda que yo hice, de `Pseudacris`, una vez que ya sé cuales secuencias quiero bajar, las "escojo" haciendo "click" en la selección a TODAS las secuencias a la vez, y escojo `Send To>Complete Record>File>Fasta>Create File` tal como se observa en la foto de abajo:

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/pseudacris-download.png?raw=true)<br>


## Alineando y visualizando nuestras secuencias

Luego, ese archivo que bajen lo agregan (hacen "upload") directamente a la página del programa de alineamiento [Clustal Omega](https://www.ebi.ac.uk/Tools/msa/clustalo/), el cual va a generar un alineamiento de nuestras secuencias. Sólo hay que especificar que el "input" son decuencias de `DNA` y que el "output" es en el formato `NEXUS`.  

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/clustal-input.png?raw=true)<br>

De ahi, puede hacer "download" del archivo, donde podrán ver el alineamiento "cortado" (en ingles "interleaved") de nexus el cual usaremos para visualizar a más detalle. 


![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/clustal-output.png?raw=true)<br>

>**NOTA**: esta "descarga" sólo va a resultar en abrirles una página donde pueden copiar/pegar el documento en su computador. Ahora, esto NO LO DEBEN PEGAR en un editor de texto "normal" como `Word`, ya que le agregará demasiados elementos que van a "corromper" al archivo. Entonces, si no tienen un editor de texto "simple" en su computador, les recomiendo que se bajen el programa [jEdit](http://www.jedit.org/), el cual es un editor de texto para PC/Windows. Alli pueden abrir un archivo en blanco, copiar/pegar el texto de Clustal Omega, y guardar el archivo como: `alineamiento.nex` (*la terminación del nombre del archivo es muy importante para el paso siguiente!*).


Finalmente, en el programa [Mesquite](https://www.mesquiteproject.org/Installation.html), que pueden descargar para cualquier tipo de computador en el enlace anterior, podemos vizualizar nuestro alineamiento de modo mucho mas fácil, así como editarlo (por ejemplo para eliminar las bases en exceso que sólo están presentes en algunos individuos). Para abrir el archivo simplemente hagan "Open File" y así abren el archivo de `nexus` que guardaron. 



![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/mesquite-align.png?raw=true)<br>

## Editando y entendiendo nuestro alineamiento

Ahora, hablemos un poco más del alineamiento. Los alineamientos son básicamente inferencias de homología de secuencias de nucleótidos - es decir, la única forma de hacer uso del código genético para hacer cualquier tipo de inferencia histórica/ecológica/clínica es "alinear" los nucleótidos/secuencias entre organismos de tal modo que esos nucleótidos "compartan una historia evolutiva". 

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/homology.png?raw=true)<br>


En el alineamiento de arriba, estamos infiriendo que esas secuencias de nucleótidos comparten un ancestro común a nivel heredado e histórico, y que aún están siendo regidos por las mismas fuerzas evolutivas, es decir, que son **genes ortólogos**. 



> Acá es donde entran los conceptos de **genes ortólogos** (genes que comparten historia evolutiva porque tienen la misma funcion/uso entre una especie y otra) y **genes parálogos** (genes que comparten historia evolutiva debido a una duplicación, pero luego de la duplicación sus historias evolutivas se vuelven "independientes"). Ambas son homologías, pero los alineamientos deben ser hechos en grupos de genes ortólogos y no parálogos. 

> **PREGUNTA:** Por qué creen que es más difícil establecer homología en bases de nucleótidos de lo que puede ser en caracteres fenotípicos? 


Entonces, ahora debemos "limpiar" un poco el alineamiento. En primera instancia, ***debemos eliminar las bases que tienen demasiados datos faltantes***. En mi caso, se observa que el individuo `AY291110.1` empieza muchisimo antes en su secuencia que los otros tres, por lo que toda esa región del gen no tiene ningún tipo de información, y lo mejor - para eficiencia computacional y tambien para no sesgar el análisis - es eliminar TODAS las bases (o "caracteres") hasta la número `2054` que es donde empiezan el resto de las secuencias. 

![](https://github.com/pesalerno/genetica-ago-2020/blob/master/files/align-2.png?raw=true)<br>


Segundo, veamos las regiones de "gaps" o vacíos en el alineamiento, e investiguemos un poco acerca de ellos. Los gaps en los genes ribosomales siempre son regiones de "loops" en su conformación. Debemos intentar, dentro de lo posible, de arreglar un poco las regiones hipervariables de "loops" para que tengan sentido las inferencias de homologías. Para ello, y para un poco de detalles de las herramientas de edición de alineamiento de MEsquite, vean el video de abajo. 

>--------------------------
>
>**VIDEO:** En [este video](https://www.loom.com/share/86bcea7ed032428b99a1b6bfbd9eecff) de ~11min les doy una introducción a la edición de alineamientos de marcadores ribosomales usando Mesquite. 
>
>--------------------------



 
<a href="https://pesalerno.github.io/genetica-ago-2020/main/2020/06/08/7_geno-feno-2.html"><button>Actividad Anterior</button></a>		<a href="https://pesalerno.github.io/genetica-ago-2020/"><button>Inicio</button></a>    <a href="https://pesalerno.github.io/genetica-ago-2020/main/2020/06/09/9_proyectos-2.html"><button>Siguiente Actividad</button></a>






