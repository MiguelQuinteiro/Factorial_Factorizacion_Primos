# Factorial_Factorizacion_Primos
Estudio de los Factoriales la Factorización y los Números Primos

Factoriales!, Factorización y Números Primos

No estoy seguro de que se hayan estudiado de esa manera, lo primero es comenzar con una lista de numeros factoriales

0!, 1!, 2!,.....n! empezando de arriba hacia abajo. junto al resultado buscar la factorización ejemplo:

 0! =       1 = 2^0  * 3^0  * 5^0 * 7^0 * 11^0
 1! =       1 = 2^0  * 3^0  * 5^0 * 7^0 * 11^0
 2! =       2 = 2^1  * 3^0  * 5^0 * 7^0 * 11^0
 3! =       6 = 2^1  * 3^1  * 5^0 * 7^0 * 11^0
 4! =      24 = 2^3  * 3^1  * 5^0 * 7^0 * 11^0
 5! =     120 = 2^3  * 3^1  * 5^1 * 7^0 * 11^0
 6! =     720 = 2^4  * 3^2  * 5^1 * 7^0 * 11^0
 7! =    5040 = 2^4  * 3^2  * 5^1 * 7^1 * 11^0
 8! =   40320 = 2^7  * 3^2  * 5^1 * 7^1 * 11^0
 9! =  362880 = 2^7  * 3^4  * 5^1 * 7^1 * 11^0
10! = 3628800 = 2^8  * 3^4  * 5^2 * 7^1 * 11^0
11! = 3628800 = 2^8  * 3^4  * 5^2 * 7^1 * 11^1

Me dí cuenta que los exponentes de los números de las tablas cambian de una forma en particular, los de la columna 2 cambian cada dos filas, los de la columna tres cambian cada 3 filas y los de la 5 cambian cada cinco filas, de manera que cuando se calcula la factorización de un numero primo factorial, obligatoriamente es la primera vez que se tiene que utilizar a ese número primo en la factorización, así que me olvide de los factoriales y me concentré solamente en el cambio de los exponentes de los números primos y cree esta tabla. (ver Imagen)

Cambié entonces en la tabla a los exponentes y sus bases por 0 y 1 solamente de manera que bajo el dos (2) pongo 0,0,1,1,0,0,1,1,0,0 y bajo el tres (3) 0,0,0,1,1,1,0,0,0,1,1,1.

Los números primos vienen obligatoriamente cuando se intenta seguir la lista y en la fila la cadena de los 1 y 0 es igual a la anterior, entonces para diferenciarlas hay que poner un 1 al final y estamos encontrando un nuevo número primo. De manera que se pueden obtener todos los nuemros primes, sin dividir, sin buscar nada más que continuar las columnas según los números que ya se tengan.

Obviamente ya me cree un programita que hace eso exactamente... (ver otra imangen)

No se si llamarlo una Criba, porque en realidad no tengo que ir más lejos de donde me encuentro en la línea de los números enteros a tachar ningun valor, simplemente la lista de los números primos va emergiendo sola a partir de todos los números primos anteriores que ya se tengan.

Y por supuesto ya no es necesario calcular el factorial de ningún numero grande, lo que sería más dificil incluso que hallar al siguiente número primo, ya que los factoriales crecen demasiado rápido. Lo único que interesa es si la fila anterior y la fila actual son iguales o no, y si son iguales para diferenciarlas en la fila actual se tiene que agregar un 1 al final y por lo tanto estas en la fila de un nuevo número Primo.... ¡Que tal! ¿Que te parece?  ¿Lo habias visto antes?

Reduje el problema del cálculo del factorial a solo interesarme si los exponentes van a cambiar o no de una fila a la siguiente y ni siquiera es es un cambio de base a binaria, piensa en cada columna como algo separado, en la columna del 2 las potencias se repiten cada dos veces, y luego aumentan de exponente, el cual se vuelve a repetir dos veces nada más y así todo el rato... como lo que me interesan son los nuemros primos y no los factoriales lo único que debo registrar es si tengo que utilizar el mismo exponente anterior o lo debo cambiar y para eso me es suficiente con pensar en forma binaria, 1,1 si sigue igual y luego cambio a 0,0 para los siguientes dos casos, algo similar pasa en la columna del tres pero esta vez cada tres veces 0,0,0 y luego 1,1,1 y así con todas las columnas.

La cosa es, ni siquiera hay que factorizar, los factores primos se van ENCONTRANDO a medida que continuas con la lista hacia abajo, cuando quieres crear una nueva fila y todos los numeros estan REPETIDOS en la anterior, es OBLIGATORIO agregar un nuevo FACTOR PRIMO en una nueva columna y ese factor primo coincide con el número de la Fila en la que te encuentras.

Para factorizar que procedimientos seguimos ??? Tomamos al número y lo dividimos entre el número primo mas pequeño que se pueda? para ver si es una division entera o no ? y así susecivamente... Yo no tengo que hacer esa division.

En Resumen... Lo primero calcular las factorizaciones de los primeros factoriales para que se vea lo que digo sobre como cambian los exponentes de los factores primos .. los del 2 crecen de dos en dos repeticiones y los del 11 crecen de once en once repeticiones...  ESA ES LA PRIMERA PARTE...

Luego la segunda parte es cambiar por 0 y 1 esos casos y olvidarnos por completo de los Factoriales, porque en realidad no nos interesan los exponentes, porque no queremos encontrar el factorial de ningún número en particular (cosa que es dificil y costoso computacionalmente), lo único que interesa es si el EXPONENTE se va a repetir o no en la siguiente FILA, luego a medida que voy creando las filas siguiendo el patrón de cada columna en particular voy viendo si lo que encuentro son filas distintas o iguales, SI SON IGUALES BINGO, encontre un nuevo nuemero primo y una nueva Columna para la tabla. En los títulos de las columnas del primer dibujo te van quedando todos los numeros Primos que se van encontrando secuencialmente.... Sin Dividir, Sin Factorizar y sin calcular el Factorial de ningún número.

Los ceros y los unos son una manera de decir que el exponente al que se encuentra el número de la columna es el mismo o cambio a otro distinto en 0! y en 1! el 2 en la segunda columna esta elevado a la Cero las primeras dos filas tienen 2^0 y 2^0, luego en las filas del 2! y del 3! el 2 esta elevado a la uno alli ese número primo está con 2^1 y 2^1, luego en las filas del 4! y del 5! el dos esta elevado a la tres 2^3 y 2^3, luego en las filas del 7! y del 8! el 2 esta elevado a la cuatro 2^4 y 2^4, y siempre será así, el factor 2 ira cambiando de exponente cada DOS FILAS. Como no me importa el valor que tome el exponente sino que lo que me importa es cada cuantas filas cambia el exponente, los puedo cambiar para completar las filas con 0 y 0 para las primeras dos filas, luego con 1 y 1 para las filas 3 y 4 y luego nuevamente para 0 y 0 para las filas 5 y 6, espero con esto se entieda para que utilizo a los ceros y a los 1 ahora ????.

Con el tres vas a tener lo mismo pero 3^0, 3^0, 3^0 luego ,3^1, 3^1, 3^1 en las siguientes tres filas, luego 3^2, 3^2, 3^2 y luego en las siguientes filas 3^4, 3^4 ,3^4.... De forma que van a cambiar los exponentes cada tres filas, eso lo podemos simplificar diciendo que utilizo primero tres 0, luego tres 1, luego otra vez tres 0, luego otra vez tres 1 y así sucecivamente hasta el infinito en esa Columna del número 3.

Me interesaria entender la teoria porque creo que da para mucho más, habría que darle algo de formalidad para poder analizarla y allí es donde yo me quedo corto.

Por ejemplo yo estoy revisando toda la FILA antes de decidir si el numero que viene es PRIMO o no, y resulta que eso es una perdida de tiempo, porque si los factores Primos anteriores a la raiz cuadra del numero no cambiam CREO que ya no pueden cambiar los que estan después de ese valor, bueno yo tengo varios días con esto y me parece una idea original, al menos no la he visto por alli, estoy buscando si alguien se a proximado a los números primos de esta forma y no lo he encontrado, tal vez si, pero hay que buscar con más detalle.

Luego Buscando en Internet encontré un teorema que relaciona factoriales con primos es El teorema de Wilson , lo conoces?

Teorema de Wilson https://es.m.wikipedia.org/wiki/Teorema_de_Wilson  

En matemáticas, particularmente en teoría de números y álgebra abstracta, el teorema de Wilson es una proposición clásica vinculada con la divisibilid...

Esto fue lo más cercano que encontre aunque aun me parece el razonamiento de los 0 y 1 algo muy original.

Claro eso evita el tener que calcular el Factorial del numero que está en la fila, y de todos modos permite saber si el número de la fila es primo o no...

Si lo que digo de la raíz cuadrada tambien es cierto sería otra ganancia importante en la velocidad para determinar que el numero sea primo, porque solo se revisaria la fila de 0 y 1 hasta la columna del numero primo que este por debajo de la raiz cuadrada del nuemro de la fila y si todos allí son iguales, entonces tambien obligatoriamente tendrian que ser iguales los siguientes y habriamos encontrado un nuevo nuemro primo, pero hay que investigar más sobre que cosas son ciertas y cuales no, pero me pareció una manera interesante de aproximarse a los números primos, y no de la forma tradicional.

Fijate que la página dice que :  "... El teorema de Wilson no se utiliza como test de primalidad en la práctica, ya que para calcular (n − 1)! módulo n para un número n grande es costoso (computacionalmente hablando), y se conocen tests más sencillos y rápidos. ..." y justamente con los ceros y unos se elimina el problema de tener que calcular el (n-1)! ese factorial es el que pone lento los calculos.

Así que tal vez dí por casualidad con una forma de OPTIMIZAR el Teorema de Wilson y ahora si se pueda utilizar como test de Primalidad, y si le agregamos lo de la raíz cuadrada para el análisis de la fila, la optimización tal vez pueda hacerse mucho mejor sería muchisimo mayor.

Saludos.
