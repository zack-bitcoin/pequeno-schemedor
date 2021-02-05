Capitulo 2: Hacelo, Hacelo otra vez, y otra vez, y otra vez...
==============

-----------------

Verdad o falso: `(lat? l)` cuando `l` es `(Juan Rollo no puede comer mas pollo)`

Verdad,
    porque cada expreción-S en `l` es un atomo.

-----------------

Verdad o falso: `(lat? l)` cuando `l` es `((Juan) Rollo no puede comer mas pollo)`

Falso,
    porque `(car l)` es una lista.

-----------------

Verdad o falso: `(lat? l)` cuando `l` es `(Juan (Rollo no) puede comer mas pollo)`

Falso,
    porque uno d los expreciónes-S en `l` es una lista.

-----------------

Verdad o falso: `(lat? l)` cuando `l` es `()`

Verdad,
    porque no hay lista adentro

-----------------

Verdad o falso: una lat es una lista de atomos?

Verdad!
    Cada lat es una lista de atomos!

-----------------

Escribe el función `lat?` usando unos, pero no necesariamente todo, de esos funciónes: `car` `cdr` `cons` `null?` `atom?` y `eq?`

No tenemos expectacion que puedes hacer eso todavia. Porque faltas unos ingredientes. Haces los siguentes preguntas. Buena suerte.

-----------------

Estas descansado?

-----------------

```
(define lat?
  (lambda (l)
    (cond
      ((null? l) #t)
      ((atom? (car l)) (lat? (cdr l)))
      (else #f))))
```
Que es el valor de `(lat? l)` cuando `l` es el argumento `(panzeta y huevos)`

`#t`.
    Eso aplicación `(lat? l)` cuando `l` es `(panzeta y huevos)` tiene el valor `#t` -- verdad -- porque `l` es un lat.

-----------------

Como podemos saber es `#t` por la aplicación `(lat? l)`

No tenemos expectacion que puedes hacer eso tampoco.
Sabemos porque podemos ver que preguntas lat?.
Estrategia: Escribe la definición del función `lat?` y ver eso por las siguentes preguntas.

-----------------

Que es la primera pregunta de `(lat? l)`

`(null ?)`

recuerda:
  `(cond ...)` para iniciar las preguntas;
  `(lambda ...)` crea una función; y
  `(define ...)` da una nombre.

-----------------

Que significa la linea 
  `((null? l) #t)`
cuando
  `l` es `(panzeta y huevos)`

`(null? l)` pregunta si el argumento `l` es la lista null. Si es, el valor de el aplicación es verdad `#t`. Si no, preguntamos la proxima pregunta. En eso caso, `l` no es la lista null, entonces preguntamos la proxima pregunta.

-----------------

Que es la proxima pregunta?

`(atom? (car l))`

-----------------

Que significa la linea
  `((atom? (car l)) (lat? (cdr l)))`
cuando
  `l` es `(y huevos)`

`(atom? (car l))` pregunta si `(car l)` es un atomo. Si es un atomo, el valor de la aplicación es `(lat? (cdr l))`. Si no, preguntamos la proxima pregunta. en eso caso `(car l)` es un atomo, entonces queiremos saber si el resto de la lista `l` es solo atomos.

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` es para saber si el resto de la lista `l` solo tiene atomos. Estamos usando el funcion `lat?` otra vez, pero eso ves, con el argumento `(cdr l)`, cual es `(huevos)`.

-----------------

Que es la proxima pregunta?

`(null? l).

-----------------

Que es la significa de la linea
  `((null? l) #t)`
cuando
  `l` es ahora `(huevos)`

`(null? l)` pregunta si el argumento `l` es la lista null. Si es, el valor de el aplicación es `#t` -- verdad. Si no, vamos a la proxima pregunta. En eso caso, `l` no es null, entonces vamos a la proxima pregunta.

-----------------

Que es la proxima pregunta?

`(atom? (car l))`.

-----------------

Que significa la linea
  `((atom? (car l)) (lat? (cdr l)))`
cuando
  `l` es `(huevos)`

`(atom? (car l))` pregunta si `(car l)` es un atomo. Si es un atomo, el valor de la aplicación es `(lat? (cdr l))`. Si `(car l)` no es un atomo, preguntamos la proxima pregunta. En eso caso, `(car l)` es un atomo, entonces, otro vez vamos a ver `(lat? (cdr l))`

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` pregunta si el resto de la lista `l` solo tiene atomos. Usa el función `lat?`, con `l` transformando hasta el valor de `(cdr l)`.

-----------------

Ahora, que es el argumento por `lat?`

`()`.

-----------------

Que significa la linea
  `((null? l) #t)`
cuando
  `l` es ahora `()`

`(null? l)` pregunta si `l` es la lista null. Si es, el valor de el aplicación es el valor #t. Si no, preguntamos la proxima pregunta. En eso caso, () es la lista null. Entonces, el valor de la aplicación `(lat? l)` cuando
  `l` es `(panzeta y huevos)`, es #t --- verdad.

-----------------

Recuerdas la preguntas sobre `(lat? l)`

Problamente no. La aplicación `(lat? l)` tiene el valor de #t cuando la lista `l` es una lista de atomos cuando `l` es `(panzeta y huevos)`.

-----------------

Puedes usar tu proprio palabras para explicar que hace `lat?`?

Aca son nuestro palabras:
  "`lat?` vea cada expresión-S en la lista. Pregunta si cada es un atomo, hasta que no hay mas. Si todo son atomos, el resulto es `#t`. Si encuentra una lista, el resulto es `#f` --- falso."
Ahora vamos a ver un ejemplo que resulto en falso.

-----------------

Aca es el función `lat?` otra vez:
```
(define lat?
  (lambda (l)
    (cond
      ((null? l) #t)
      ((atom? (car l)) (lat? (cdr l)))
      (else #f))))
```
Que es el valor de `(lat? l)` cuando
  `l` es `(panzeta (y huevos))`

#f,
  porque la lista `l` tiene un expresión-S adentro que es una lista.

-----------------

que es la primer pregunto?

`(null? l)`.

-----------------

Que es la significa de la linea
  `((null? l) #t)`
cuando `l` es `(panzeta (y huevos))`

`(null? l)` pregunta si `l` es la lista null. Si eso es la lista null, el valor es `#t`. Si `l` no es la lista null, vamos a la proxima pregunta. En ese caso, no es null, entonces, preguntamos la proxima pregunta.

-----------------

Que es la proxima pregunta?

    `(atom? (car l))`

-----------------

Que es la significa de la linea
    `((atom? (car l)) (lat? (cdr l)))`
cuando
    `l` es `(panzeta (y huevos))`

`(atom? (car l))` preguntas si `(car l)` es un atomo. Si es un atomo, el valor es `(lat? (cdr l))`. Si no es un atomo, vamos a la proxima pregunta. En ese caso, `(car l)` es un atomo, entonces vamos a ver si el resto de la lista `l` solo tiene atomos adrentro.

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` ver para saber si el resto de la lista `l` solo tiene atomos adrentro, eso vez usamos `(cdr l)` in lugar de `l`.

-----------------

Que significa la linea `((null? l) #t)` cuando `l` ahora es `((y huevos))`

`(null? l)` pregunta si `l` es la lista null. Si es null, el resulto es `#t`. Si no es null, vamos a la proxima pregunta. En eso caso, `l` no es null, entonces vamos a la proxima pregunta.

-----------------

Que es la proxima pregunta?

`(atom? (car l))`

-----------------

Que significa de la linea `((atom? (car l)) (lat? (cdr l)))` cuando `l` es ahora `((y huevos))`

`(atom? (car l))` pregunta si `(car l)` es un atomo. Si es un atomo, el valor es `(lat? (cdr l))`. Si no es, vamos a la proxima pregunta. En eso caso, `(car l)` no es un atomo, entonces vamos la proxima pregunta.

-----------------

Que es la proxima pregunta?

`else`.

-----------------

Que significa la pregunta `else`?

`else` significa verdad.

-----------------

`else` significa verdad?

Sí, porque la pregunta `else` es siempre verdad!

-----------------

`else`

verdad.

-----------------

Porqué `else` es la ultima pregunta?

Porque no necisitamos nada mas preguntas.

-----------------

Porqué no necesitams nada mas preguntas?

Porque una lista puede estar vacio, puede tener un atomo en la primera posición, o puede tener una lista en la primera posición.

-----------------

que significa la linea `(else #f)`

`else` es siempre verdad, entonces el resulto es `#f`.

-----------------

Que es `)))`

Son parentesis para cerrar `(cond`, `(lambda`, y `(define`. Ellos son en el inicio de la definición.

-----------------

Puede explicar como determinamos el valor `#f` por `(lat? l)` cuando `l` es `(panzeta (y huevos))`

Aca es una forma decir eso:
  "`(lat? l) mira cada argumento en `l` para saber si es un atomo. Si ya miró cada argumento, y no encontra un lista, `(lat? l)` es `#t`. Si encontra una lista, como pasa en ejemplo `(panzeta (y huevos))`, el valor de `(lat? l)` es `#f`.
  
-----------------

"or" es la palabra en inglés por "o".

Es `(or (null? l1) (atom? l2))` verdad o falso cuando `l1` es `()` y `l2` es `(d e f g)`

Verdad,
  porque `(null? l1)` es verdad cuando `l1` es `()`.

-----------------

Es `(or (null? l1) (null? l2))` verdad o false cuando `l1` es `(a b c)` y `l2` es `()`

Verdad,
   porque `(null? l2)` es verdad cuando `l2` es `()`.
   
-----------------

Es `(or (null? l1) (null? l2))` verdad o false cuando `l1` es `(a b c)` y `l2` es `(atom)`

Falso,
    porque `(null? l1)` y `(null? l2)` no son verdades cuando `l1` es `(a b c)` y `l2` es `(atom)`.
    
-----------------

Que hace `(or ...)`?

Hace dos preguntas, uno y despues el otro. Si uno es verdad, termina y el resultado es verdad. Si la primer no es verdad, vamos a la segunda pregunta y el resultado es el resultado de la seguda pregunta.

-----------------
