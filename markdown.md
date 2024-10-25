## Encabezados

Para crear un encabezado, agregue signos de número ( \#) antes de una palabra o frase. La cantidad de signos de número que utilice debe corresponderse con el nivel del encabezado. Por ejemplo, para crear un encabezado de nivel tres ( \<h3\>), use tres signos de número (p. ej., \#\#\# My Header).

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| \# Heading level 1 | \<h1\>Heading level 1\</h1\> | Título nivel 1 |
| \#\# Heading level 2 | \<h2\>Heading level 2\</h2\> | Título nivel 2 |
| \#\#\# Heading level 3 | \<h3\>Heading level 3\</h3\> | Título nivel 3 |
| \#\#\#\# Heading level 4 | \<h4\>Heading level 4\</h4\> | Título nivel 4 |
| \#\#\#\#\# Heading level 5 | \<h5\>Heading level 5\</h5\> | Título nivel 5 |
| \#\#\#\#\#\# Heading level 6 | \<h6\>Heading level 6\</h6\> | Título nivel 6 |

### Sintaxis alternativa

Alternativamente, en la línea debajo del texto, agregue cualquier cantidad de \==caracteres para el nivel de encabezado 1 o \--caracteres para el nivel de encabezado 2\.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| Heading level 1 \=============== | \<h1\>Heading level 1\</h1\> | Título nivel 1 |
| Heading level 2 \--------------- | \<h2\>Heading level 2\</h2\> | Título nivel 2 |

### Prácticas recomendadas para encabezados

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar un espacio faltante entre los signos de número ( \#) y el nombre del encabezado. Para lograr compatibilidad, siempre coloque un espacio entre los signos de número y el nombre del encabezado.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| \# Here's a Heading  | \#Here's a Heading |

También debe colocar líneas en blanco antes y después de un encabezado para mayor compatibilidad.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| Try to put a blank line before... \# Heading ...and after a heading. | Without blank lines, this might not look right. \# Heading Don't do this\! |

## Párrafos

Para crear párrafos, utilice una línea en blanco para separar una o más líneas de texto.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| I really like using Markdown. I think I'll use it to format all of my documents from now on. | \<p\>I really like using Markdown.\</p\> \<p\>I think I'll use it to format all of my documents from now on.\</p\> | Me gusta mucho usar Markdown. Creo que lo usaré para formatear todos mis documentos de ahora en adelante. |

### Mejores prácticas para los párrafos

A menos que el [párrafo esté en una lista](https://www.markdownguide.org/basic-syntax/#paragraphs) , no sangre los párrafos con espacios o tabulaciones.

 Nota: Si necesita sangrar párrafos en la salida, consulte la sección sobre cómo [sangrar (tabulación)](https://www.markdownguide.org/hacks/#indent-tab) .

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| Don't put tabs or spaces in front of your paragraphs. Keep lines left-aligned like this.  |     This can result in unexpected formatting problems.   Don't add tabs or spaces in front of paragraphs. |

## Saltos de línea

Para crear un salto de línea o una nueva línea ( \<br\>), finalice una línea con dos o más espacios y luego presione Enter.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| This is the first line.   And this is the second line. | \<p\>This is the first line.\<br\> And this is the second line.\</p\> | Esta es la primera línea.Y esta es la segunda línea. |

### Mejores prácticas para saltos de línea

Puede utilizar dos o más espacios (comúnmente denominados "espacios en blanco finales") para los saltos de línea en casi todas las aplicaciones Markdown, pero es un tema controvertido. Es difícil ver los espacios en blanco finales en un editor y muchas personas colocan dos espacios después de cada oración de forma accidental o intencional. Por este motivo, es posible que desee utilizar algo distinto de los espacios en blanco finales para los saltos de línea. Si su aplicación Markdown [admite HTML](https://www.markdownguide.org/basic-syntax/#html) , puede utilizar la \<br\>etiqueta HTML.

Para mayor compatibilidad, utilice espacios en blanco finales o la \<br\>etiqueta HTML al final de la línea.

Hay otras dos opciones que no recomiendo usar. CommonMark y algunos otros lenguajes de marcado livianos te permiten escribir una barra invertida ( \\) al final de la línea, pero no todas las aplicaciones Markdown lo admiten, por lo que no es una gran opción desde una perspectiva de compatibilidad. Y al menos un par de lenguajes de marcado livianos no requieren nada al final de la línea: solo escribe return y crearán un salto de línea.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| First line with two spaces after.   And the next line. First line with the HTML tag after.\<br\> And the next line.  | First line with a backslash after.\\ And the next line. First line with nothing after. And the next line.  |

## Énfasis

Puedes agregar énfasis poniendo el texto en negrita o cursiva.

### Atrevido

Para poner en negrita un texto, agregue dos asteriscos o guiones bajos antes y después de una palabra o frase. Para poner en negrita la mitad de una palabra para enfatizarla, agregue dos asteriscos sin espacios alrededor de las letras.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| I just love \*\*bold text\*\*. | I just love \<strong\>bold text\</strong\>. | Me encanta el texto en negrita . |
| I just love \_\_bold text\_\_. | I just love \<strong\>bold text\</strong\>. | Me encanta el texto en negrita . |
| Love\*\*is\*\*bold | Love\<strong\>is\</strong\>bold | El amor es atrevido |

#### Mejores prácticas audaces

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar los guiones bajos en el medio de una palabra. Para lograr compatibilidad, use asteriscos para poner en negrita el medio de una palabra y enfatizarla.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| Love\*\*is\*\*bold | Love\_\_is\_\_bold |

### Itálico

Para poner un texto en cursiva, agregue un asterisco o un guión bajo antes y después de una palabra o frase. Para poner en cursiva la mitad de una palabra para enfatizarla, agregue un asterisco sin espacios alrededor de las letras.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| Italicized text is the \*cat's meow\*. | Italicized text is the \<em\>cat's meow\</em\>. | El texto en cursiva es el *maullido del gato* . |
| Italicized text is the \_cat's meow\_. | Italicized text is the \<em\>cat's meow\</em\>. | El texto en cursiva es el *maullido del gato* . |
| A\*cat\*meow | A\<em\>cat\</em\>meow | Un maullido *de gato* |

#### Prácticas recomendadas para cursiva

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar los guiones bajos en el medio de una palabra. Para lograr compatibilidad, use asteriscos para poner en cursiva el medio de una palabra y darle énfasis.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| A\*cat\*meow | A\_cat\_meow |

### Negrita y cursiva

Para enfatizar el texto con negrita y cursiva al mismo tiempo, agregue tres asteriscos o guiones bajos antes y después de una palabra o frase. Para poner en negrita y cursiva la mitad de una palabra para enfatizarla, agregue tres asteriscos sin espacios alrededor de las letras.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| This text is \*\*\*really important\*\*\*. | This text is \<em\>\<strong\>really important\</strong\>\</em\>. | Este texto es *realmente importante* . |
| This text is \_\_\_really important\_\_\_. | This text is \<em\>\<strong\>really important\</strong\>\</em\>. | Este texto es *realmente importante* . |
| This text is \_\_\*really important\*\_\_. | This text is \<em\>\<strong\>really important\</strong\>\</em\>. | Este texto es *realmente importante* . |
| This text is \*\*\_really important\_\*\*. | This text is \<em\>\<strong\>really important\</strong\>\</em\>. | Este texto es *realmente importante* . |
| This is really\*\*\*very\*\*\*important text. | This is really\<em\>\<strong\>very\</strong\>\</em\>important text. | Este es realmente un texto *muy* importante. |

 Nota: El orden de las etiquetas emy strongpuede invertirse dependiendo del procesador Markdown que estés usando.

#### Prácticas recomendadas para usar negrita y cursiva

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar los guiones bajos en el medio de una palabra. Para lograr compatibilidad, use asteriscos para poner en negrita y cursiva el medio de una palabra para enfatizarla.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| This is really\*\*\*very\*\*\*important text. | This is really\_\_\_very\_\_\_important text. |

## Citas en bloque

Para crear una cita en bloque, agregue una \>antes de un párrafo.

\> Dorothy followed her through many of the beautiful rooms in her castle.

La salida renderizada se ve así:

Dorothy la siguió por muchas de las hermosas habitaciones de su castillo.

### Citas en bloque con varios párrafos

Las citas en bloque pueden contener varios párrafos. Agregue una \>en las líneas en blanco entre los párrafos.

\> Dorothy followed her through many of the beautiful rooms in her castle.  
\>  
\> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

La salida renderizada se ve así:

Dorothy la siguió por muchas de las hermosas habitaciones de su castillo.

La bruja le ordenó que limpiara las ollas y las teteras, barriera el suelo y mantuviera el fuego alimentado con leña.

### Citas en bloque anidadas

Las citas en bloque se pueden anidar. Agregue un signo \>\>antes del párrafo que desea anidar.

\> Dorothy followed her through many of the beautiful rooms in her castle.  
\>  
\>\> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

La salida renderizada se ve así:

Dorothy la siguió por muchas de las hermosas habitaciones de su castillo.

La bruja le ordenó que limpiara las ollas y las teteras, barriera el suelo y mantuviera el fuego alimentado con leña.

### Citas en bloque con otros elementos

Las citas en bloque pueden contener otros elementos con formato Markdown. No se pueden utilizar todos los elementos: tendrás que experimentar para ver cuáles funcionan.

\> \#\#\#\# The quarterly results look great\!  
\>  
\> \- Revenue was off the chart.  
\> \- Profits were higher than ever.  
\>  
\>  \*Everything\* is going according to \*\*plan\*\*.

La salida renderizada se ve así:

#### ¡Los resultados trimestrales lucen geniales\!

* Los ingresos estaban por las nubes.  
* Las ganancias fueron mayores que nunca.

*Todo* va según lo previsto .

### Mejores prácticas para usar citas en bloque

Para mayor compatibilidad, coloque líneas en blanco antes y después de las citas en bloque.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| Try to put a blank line before... \> This is a blockquote ...and after a blockquote. | Without blank lines, this might not look right. \> This is a blockquote Don't do this\! |

## Liza

Puede organizar elementos en listas ordenadas y desordenadas.

### Listas ordenadas

Para crear una lista ordenada, agregue elementos de línea con números seguidos de puntos. Los números no tienen que estar en orden numérico, pero la lista debe comenzar con el número uno.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| 1\. First item 2\. Second item 3\. Third item 4\. Fourth item | \<ol\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ol\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| 1\. First item 1\. Second item 1\. Third item 1\. Fourth item | \<ol\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ol\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| 1\. First item 8\. Second item 3\. Third item 5\. Fourth item | \<ol\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ol\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| 1\. First item 2\. Second item 3\. Third item     1\. Indented item     2\. Indented item 4\. Fourth item | \<ol\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item     \<ol\>       \<li\>Indented item\</li\>       \<li\>Indented item\</li\>     \</ol\>   \</li\>   \<li\>Fourth item\</li\> \</ol\> | Primer artículo Segundo punto Tercer punto Elemento sangrado Elemento sangrado Cuarto punto |

#### Prácticas recomendadas para listas ordenadas

CommonMark y algunos otros lenguajes de marcado livianos permiten usar un paréntesis ( )) como delimitador (por ejemplo, 1\) First item), pero no todas las aplicaciones Markdown lo admiten, por lo que no es una gran opción desde una perspectiva de compatibilidad. Para lograr compatibilidad, use solo puntos.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| 1\. First item 2\. Second item | 1\) First item 2\) Second item |

### Listas desordenadas

Para crear una lista desordenada, agregue guiones ( \-), asteriscos ( \*) o signos más ( \+) delante de los elementos de línea. Aplique sangría a uno o más elementos para crear una lista anidada.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| \- First item \- Second item \- Third item \- Fourth item | \<ul\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ul\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| \* First item \* Second item \* Third item \* Fourth item | \<ul\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ul\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| \+ First item \+ Second item \+ Third item \+ Fourth item | \<ul\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item\</li\>   \<li\>Fourth item\</li\> \</ul\> | Primer artículo Segundo punto Tercer punto Cuarto punto |
| \- First item \- Second item \- Third item     \- Indented item     \- Indented item \- Fourth item | \<ul\>   \<li\>First item\</li\>   \<li\>Second item\</li\>   \<li\>Third item     \<ul\>       \<li\>Indented item\</li\>       \<li\>Indented item\</li\>     \</ul\>   \</li\>   \<li\>Fourth item\</li\> \</ul\> | Primer artículo Segundo punto Tercer punto Elemento sangrado Elemento sangrado Cuarto punto |

#### Cómo iniciar elementos de una lista desordenada con números

Si necesita comenzar un elemento de lista desordenada con un número seguido de un punto, puede usar una barra invertida ( \\) para [escapar](https://www.markdownguide.org/basic-syntax/#escaping-characters) del punto.

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| \- 1968\\. A great year\! \- I think 1969 was second best. | \<ul\>   \<li\>1968. A great year\!\</li\>   \<li\>I think 1969 was second best.\</li\> \</ul\> | 1968\. ¡Un gran año\! Creo que 1969 fue el segundo mejor año. |

#### Prácticas recomendadas para listas desordenadas

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar los distintos delimitadores en la misma lista. Por cuestiones de compatibilidad, no mezcle ni combine delimitadores en la misma lista: elija uno y manténgalo.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| \- First item \- Second item \- Third item \- Fourth item | \+ First item \* Second item \- Third item \+ Fourth item |

### Agregar elementos en listas

Para agregar otro elemento a una lista preservando la continuidad de la lista, sangre el elemento cuatro espacios o una tabulación, como se muestra en los siguientes ejemplos.

 Consejo: Si las cosas no aparecen como esperas, verifica que hayas sangrado los elementos de la lista con cuatro espacios o una tabulación.

#### Párrafos

\* This is the first list item.  
\* Here's the second list item.

    I need to add another paragraph below the second list item.

\* And here's the third list item.

La salida renderizada se ve así:

* Este es el primer elemento de la lista.  
* Aquí está el segundo elemento de la lista.  
  Necesito agregar otro párrafo debajo del segundo elemento de la lista.  
* Y aquí está el tercer elemento de la lista.

#### Citas en bloque

\* This is the first list item.  
\* Here's the second list item.

    \> A blockquote would look great below the second list item.

\* And here's the third list item.

La salida renderizada se ve así:

* Este es el primer elemento de la lista.  
* Aquí está el segundo elemento de la lista.  
  Una cita en bloque luciría genial debajo del segundo elemento de la lista.  
* Y aquí está el tercer elemento de la lista.

#### Bloques de código

[Los bloques de código](https://www.markdownguide.org/basic-syntax/#code-blocks) suelen tener una sangría de cuatro espacios o una tabulación. Cuando están en una lista, se les aplica una sangría de ocho espacios o dos tabulaciones.

1\. Open the file.  
2\. Find the following code block on line 21:

        \<html\>  
          \<head\>  
            \<title\>Test\</title\>  
          \</head\>

3\. Update the title to match the name of your website.

La salida renderizada se ve así:

1. Abra el archivo.

Encuentre el siguiente bloque de código en la línea 21:  
 \<html\>  
   \<head\>  
     \<title\>Test\</title\>  
   \</head\>

2.   
3. Actualice el título para que coincida con el nombre de su sitio web.

#### Imágenes

1\. Open the file containing the Linux mascot.  
2\. Marvel at its beauty.
!\[mono\](./mono.jpg)
https://github.com/alexisbolivar5/practica-0
3\. Close the file.

La salida renderizada se ve así:

1. Abra el archivo que contiene la mascota de Linux.  
2. Maravíllate con su belleza.
 ![mono][image1]  
4. Cerrar el archivo.

#### Liza

Puede anidar una lista desordenada en una lista ordenada, o viceversa.

1\. First item  
2\. Second item  
3\. Third item  
    \- Indented item  
    \- Indented item  
4\. Fourth item

La salida renderizada se ve así:

1. Primer artículo  
2. Segundo punto  
3. Tercer punto  
   * Elemento sangrado  
   * Elemento sangrado  
4. Cuarto punto

## Código

Para indicar una palabra o frase como código, enciérrela entre comillas simples ( \`).

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| At the command prompt, type \`nano\`. | At the command prompt, type \<code\>nano\</code\>. | En el símbolo del sistema, escriba nano. |

### Cómo escapar de las comillas invertidas

Si la palabra o frase que desea indicar como código incluye una o más comillas invertidas, puede escaparla encerrando la palabra o frase entre comillas invertidas dobles ( \`\`).

| Reducción | HTML | Salida renderizada |
| ----- | ----- | ----- |
| \`\`Use \`code\` in your Markdown file.\`\` | \<code\>Use \`code\` in your Markdown file.\</code\> | Use \`code\` in your Markdown file. |

### Bloques de código

Para crear bloques de código, sangre cada línea del bloque con al menos cuatro espacios o una tabulación.

   \<html\>  
      \<head\>  
      \</head\>  
    \</html\>

La salida renderizada se ve así:

\<html\>  
  \<head\>  
  \</head\>  
\</html\>

 Nota: Para crear bloques de código sin sangrar líneas, utilice [bloques de código cercados](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks) .

## Reglas horizontales

Para crear una regla horizontal, utilice tres o más asteriscos ( \*\*\*), guiones ( \---) o guiones bajos ( \_\_\_) en una línea por separado.

\*\*\*

\---

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

La salida renderizada de los tres parece idéntica:

---

### Mejores prácticas para la regla horizontal

Para mayor compatibilidad, coloque líneas en blanco antes y después de las reglas horizontales.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| Try to put a blank line before... \--- ...and after a horizontal rule. | Without blank lines, this would be a heading. \--- Don't do this\! |

## Campo de golf

Para crear un enlace, encierre el texto del enlace entre corchetes (por ejemplo, \[Duck Duck Go\]) y luego siga inmediatamente con la URL entre paréntesis (por ejemplo, (https://duckduckgo.com)).

My favorite search engine is \[Duck Duck Go\](https://duckduckgo.com).

La salida renderizada se ve así:

Mi motor de búsqueda favorito es [Duck Duck Go](https://duckduckgo.com/) .

 Nota: Para crear un vínculo a un elemento de la misma página, consulte [la sección sobre cómo crear vínculos a identificadores de encabezado](https://www.markdownguide.org/extended-syntax/#linking-to-heading-ids) . Para crear un vínculo que se abra en una nueva pestaña o ventana, consulte la sección sobre [destinos de vínculos](https://www.markdownguide.org/hacks/#link-targets) .

### Añadiendo títulos

Opcionalmente, puedes agregar un título a un enlace. Este aparecerá como una información sobre herramientas cuando el usuario pase el cursor sobre el enlace. Para agregar un título, escríbalo entre comillas después de la URL.

My favorite search engine is \[Duck Duck Go\](https://duckduckgo.com "The best search engine for privacy").

La salida renderizada se ve así:

Mi motor de búsqueda favorito es [Duck Duck Go](https://duckduckgo.com/) .

### URL y direcciones de correo electrónico

Para convertir rápidamente una URL o dirección de correo electrónico en un enlace, enciérrelo entre corchetes angulares.

\<https://www.markdownguide.org\>  
\<fake@example.com\>

La salida renderizada se ve así:

[https://www.markdownguide.org](https://www.markdownguide.org/)  
fake@example.com

### Formato de enlaces

Para [enfatizar](https://www.markdownguide.org/basic-syntax/#emphasis) los enlaces, agregue asteriscos antes y después de los corchetes y paréntesis. Para indicar que los enlaces son [código](https://www.markdownguide.org/basic-syntax/#code) , agregue comillas invertidas en los corchetes.

I love supporting the \*\*\[EFF\](https://eff.org)\*\*.  
This is the \*\[Markdown Guide\](https://www.markdownguide.org)\*.  
See the section on \[\`code\`\](\#code).

La salida renderizada se ve así:

Me encanta apoyar a la [EFF](https://eff.org/) .  
Esta es la [*Guía de Markdown*](https://www.markdownguide.org/) .  
Consulta la sección sobre [code](https://www.markdownguide.org/basic-syntax/#code).

### Enlaces de estilo de referencia

Los enlaces de estilo de referencia son un tipo especial de enlace que facilita la visualización y lectura de las URL en Markdown. Los enlaces de estilo de referencia se construyen en dos partes: la parte que se mantiene en línea con el texto y la parte que se almacena en otro lugar del archivo para que el texto sea fácil de leer.

#### Cómo formatear la primera parte del enlace

La primera parte de un vínculo de estilo de referencia se formatea con dos conjuntos de corchetes. El primer conjunto de corchetes rodea el texto que debe aparecer vinculado. El segundo conjunto de corchetes muestra una etiqueta que se utiliza para señalar el vínculo que está almacenando en otra parte del documento.

Aunque no es obligatorio, puedes incluir un espacio entre el primer y el segundo par de corchetes. La etiqueta del segundo par de corchetes no distingue entre mayúsculas y minúsculas y puede incluir letras, números, espacios o signos de puntuación.

Esto significa que los siguientes formatos de ejemplo son aproximadamente equivalentes para la primera parte del enlace:

* \[hobbit-hole\]\[1\]  
* \[hobbit-hole\] \[1\]

#### Formateo de la segunda parte del enlace

La segunda parte de un enlace de estilo de referencia está formateada con los siguientes atributos:

1. La etiqueta, entre paréntesis, seguida inmediatamente de dos puntos y al menos un espacio (por ejemplo, \[label\]: ).  
2. La URL del enlace, que opcionalmente puedes incluir entre corchetes angulares.  
3. El título opcional para el enlace, que puede incluir entre comillas dobles, comillas simples o paréntesis.

Esto significa que los siguientes formatos de ejemplo son aproximadamente equivalentes para la segunda parte del enlace:

* \[1\]: https://en.wikipedia.org/wiki/Hobbit\#Lifestyle  
* \[1\]: https://en.wikipedia.org/wiki/Hobbit\#Lifestyle "Hobbit lifestyles"  
* \[1\]: https://en.wikipedia.org/wiki/Hobbit\#Lifestyle 'Hobbit lifestyles'  
* \[1\]: https://en.wikipedia.org/wiki/Hobbit\#Lifestyle (Hobbit lifestyles)  
* \[1\]: \<https://en.wikipedia.org/wiki/Hobbit\#Lifestyle\> "Hobbit lifestyles"  
* \[1\]: \<https://en.wikipedia.org/wiki/Hobbit\#Lifestyle\> 'Hobbit lifestyles'  
* \[1\]: \<https://en.wikipedia.org/wiki/Hobbit\#Lifestyle\> (Hobbit lifestyles)

Puedes colocar esta segunda parte del enlace en cualquier parte de tu documento Markdown. Algunas personas las colocan inmediatamente después del párrafo en el que aparecen, mientras que otras las colocan al final del documento (como notas finales o notas a pie de página).

#### Un ejemplo de cómo juntar las piezas

Digamos que agrega una URL como un [enlace URL estándar](https://www.markdownguide.org/basic-syntax/#links) a un párrafo y se ve así en Markdown:

In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends  
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to  
eat: it was a \[hobbit-hole\](https://en.wikipedia.org/wiki/Hobbit\#Lifestyle "Hobbit lifestyles"), and that means comfort.

Aunque puede indicar información adicional interesante, la URL que se muestra en realidad no agrega mucho al texto sin formato existente, más allá de dificultar la lectura. Para solucionar esto, puede formatear la URL de esta manera:

In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends  
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to  
eat: it was a \[hobbit-hole\]\[1\], and that means comfort.

\[1\]: \<https://en.wikipedia.org/wiki/Hobbit\#Lifestyle\> "Hobbit lifestyles"

En ambos casos anteriores, el resultado generado sería idéntico:

En un agujero en el suelo vivía un hobbit. No era un agujero sucio, húmedo y desagradable, lleno de restos de gusanos y con un olor fétido, ni tampoco un agujero seco, vacío y arenoso en el que no había nada en lo que sentarse ni comer: era un [agujero de hobbit](https://en.wikipedia.org/wiki/Hobbit#Lifestyle) , y eso significa comodidad.

y el HTML para el enlace sería:

\<a href="https://en.wikipedia.org/wiki/Hobbit\#Lifestyle" title="Hobbit lifestyles"\>hobbit-hole\</a\>

### Mejores prácticas para enlaces

Las aplicaciones Markdown no se ponen de acuerdo sobre cómo manejar los espacios en medio de una URL. Para lograr compatibilidad, intenta codificar cualquier espacio en la URL con %20. Como alternativa, si tu aplicación Markdown [admite HTML](https://www.markdownguide.org/basic-syntax/#html) , puedes usar la aetiqueta HTML.

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| \[link\](https://www.example.com/my%20great%20page) \<a href="https://www.example.com/my great page"\>link\</a\>  | \[link\](https://www.example.com/my great page)  |

Los paréntesis en medio de una URL también pueden ser problemáticos. Para lograr compatibilidad, intente codificar en la URL el paréntesis de apertura ( () con %28y el paréntesis de cierre ( )) con %29. Como alternativa, si su aplicación Markdown [admite HTML](https://www.markdownguide.org/basic-syntax/#html) , puede usar la aetiqueta HTML .

| ✅ Haz esto | ❌ No hagas esto |
| ----- | ----- |
| \[a novel\](https://en.wikipedia.org/wiki/The\_Milagro\_Beanfield\_War\_%28novel%29) \<a href="https://en.wikipedia.org/wiki/The\_Milagro\_Beanfield\_War\_(novel)"\>a novel\</a\>  | \[a novel\](https://en.wikipedia.org/wiki/The\_Milagro\_Beanfield\_War\_(novel)) |

## Imágenes

Para agregar una imagen, agregue un signo de exclamación ( \!), seguido de un texto alternativo entre corchetes y la ruta o URL del recurso de imagen entre paréntesis. Opcionalmente, puede agregar un título entre comillas después de la ruta o URL.


!\[[peta\!\](./peta.jpeg](https://github.com/alexisbolivar5/practica-0/blob/main/san-juan-mountains.avif) "peta")

La salida renderizada se ve así:

![peta\!][image2]

 Nota: Para cambiar el tamaño de una imagen, consulte la sección sobre [tamaño de imagen](https://www.markdownguide.org/hacks/#image-size) . Para agregar un título, consulte la sección sobre [títulos de imágenes](https://www.markdownguide.org/hacks/#image-captions) .

### Vinculación de imágenes

Para agregar un enlace a una imagen, encierre el Markdown de la imagen entre corchetes y luego agregue el enlace entre paréntesis.

!\[azucar\](./azucar.jpg )\](https://github.com/alexisbolivar5/practica-0/blob/main/azucar.jpg)

La salida renderizada se ve así:

![azucar][image3]

## Personajes que escapan

Para mostrar un carácter literal que de otro modo se usaría para dar formato al texto en un documento Markdown, agregue una barra invertida ( \\) delante del carácter.

\\\* Without the backslash, this would be a bullet in an unordered list.

La salida renderizada se ve así:

\*Sin la barra invertida, esto sería una viñeta en una lista desordenada.

### Personajes de los que puedes escapar

Puede utilizar una barra invertida para escapar los siguientes caracteres.

| Personaje | Nombre |
| ----- | ----- |
| \\ | barra invertida |
| \` | acento grave (ver también [cómo escapar acentos graves en el código](https://www.markdownguide.org/basic-syntax/#escaping-backticks) ) |
| \* | asterisco |
| \_ | subrayar |
| { } | llaves |
| \[ \] | soportes |
| \< \> | corchetes angulares |
| ( ) | paréntesis |
| \# | signo de libra |
| \+ | signo más |
| \- | signo menos (guión) |
| . | punto |
| \! | signo de admiración |
| | | tubería (ver también [tubería de escape en las tablas](https://www.markdownguide.org/extended-syntax/#escaping-pipe-characters-in-tables) ) |

## HTML

Muchas aplicaciones Markdown permiten utilizar etiquetas HTML en texto con formato Markdown. Esto resulta útil si prefieres determinadas etiquetas HTML a la sintaxis Markdown. Por ejemplo, a algunas personas les resulta más fácil utilizar etiquetas HTML para imágenes. El uso de HTML también resulta útil cuando necesitas cambiar los atributos de un elemento, como especificar el [color del texto](https://www.markdownguide.org/hacks/#color) o cambiar el ancho de una imagen.

Para utilizar HTML, coloque las etiquetas en el texto de su archivo con formato Markdown.

This \*\*word\*\* is bold. This \<em\>word\</em\> is italic.

La salida renderizada se ve así:

Esta palabra está en negrita. Esta *palabra* está en cursiva.
