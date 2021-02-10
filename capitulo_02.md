Capitulo 2: Hacelo, Hacelo otra vez, y otra vez, y otra vez...
==============

-----------------

Verdad o falso: `(lat? l)` cuando `l` es `(Juan Rollo no puede comer mas pollo)`

Verdad,
    porque cada expreción-S en `l` es un átomo.

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

Verdad o falso: una lat es una lista de átomos?

Verdad!
    Cada lat es una lista de átomos!

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

`(atom? (car l))` pregunta si `(car l)` es un átomo. Si es un átomo, el valor de la aplicación es `(lat? (cdr l))`. Si no, preguntamos la proxima pregunta. en eso caso `(car l)` es un átomo, entonces queiremos saber si el resto de la lista `l` es solo átomos.

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` es para saber si el resto de la lista `l` solo tiene átomos. Estamos usando el funcion `lat?` otra vez, pero eso ves, con el argumento `(cdr l)`, cual es `(huevos)`.

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

`(atom? (car l))` pregunta si `(car l)` es un átomo. Si es un átomo, el valor de la aplicación es `(lat? (cdr l))`. Si `(car l)` no es un átomo, preguntamos la proxima pregunta. En eso caso, `(car l)` es un átomo, entonces, otro vez vamos a ver `(lat? (cdr l))`

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` pregunta si el resto de la lista `l` solo tiene átomos. Usa el función `lat?`, con `l` transformando hasta el valor de `(cdr l)`.

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

Problamente no. La aplicación `(lat? l)` tiene el valor de #t cuando la lista `l` es una lista de átomos cuando `l` es `(panzeta y huevos)`.

-----------------

Puedes usar tu proprio palabras para explicar que hace `lat?`?

Aca son nuestro palabras:
  "`lat?` vea cada expresión-S en la lista. Pregunta si cada es un átomo, hasta que no hay mas. Si todo son átomos, el resulto es `#t`. Si encuentra una lista, el resulto es `#f` --- falso."
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

`(atom? (car l))` preguntas si `(car l)` es un átomo. Si es un átomo, el valor es `(lat? (cdr l))`. Si no es un átomo, vamos a la proxima pregunta. En ese caso, `(car l)` es un átomo, entonces vamos a ver si el resto de la lista `l` solo tiene átomos adrentro.

-----------------

Que significa `(lat? (cdr l))`

`(lat? (cdr l))` ver para saber si el resto de la lista `l` solo tiene átomos adrentro, eso vez usamos `(cdr l)` in lugar de `l`.

-----------------

Que significa la linea `((null? l) #t)` cuando `l` ahora es `((y huevos))`

`(null? l)` pregunta si `l` es la lista null. Si es null, el resulto es `#t`. Si no es null, vamos a la proxima pregunta. En eso caso, `l` no es null, entonces vamos a la proxima pregunta.

-----------------

Que es la proxima pregunta?

`(atom? (car l))`

-----------------

Que significa de la linea `((atom? (car l)) (lat? (cdr l)))` cuando `l` es ahora `((y huevos))`

`(atom? (car l))` pregunta si `(car l)` es un átomo. Si es un átomo, el valor es `(lat? (cdr l))`. Si no es, vamos a la proxima pregunta. En eso caso, `(car l)` no es un átomo, entonces vamos la proxima pregunta.

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

Porque una lista puede estar vacio, puede tener un átomo en la primera posición, o puede tener una lista en la primera posición.

-----------------

que significa la linea `(else #f)`

`else` es siempre verdad, entonces el resulto es `#f`.

-----------------

Que es `)))`

Son parentesis para cerrar `(cond`, `(lambda`, y `(define`. Ellos son en el inicio de la definición.

-----------------

Puede explicar como determinamos el valor `#f` por `(lat? l)` cuando `l` es `(panzeta (y huevos))`

Aca es una forma decir eso:
  "`(lat? l) mira cada argumento en `l` para saber si es un átomo. Si ya miró cada argumento, y no encontra un lista, `(lat? l)` es `#t`. Si encontra una lista, como pasa en ejemplo `(panzeta (y huevos))`, el valor de `(lat? l)` es `#f`.
  
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

Es verdad o falso que `a` es un miembro de `lat` cuando `a` es `té` y `lat` es `(café té o leche)` 

Verdad,
    porque uno de los átomos de `lat`, `(café té o leche) es lo mismo de átomo `a`--`té`.

-----------------

Es `(miembro? a lat)` verdad o falso cuando `a` es `poché` y `lat` es `(huevos frito y huevos revueltos)`

Verdad,
    porque `a` no es uno de los átomos de `lat`.

-----------------

( eq? es abreviatura en Ingles por "equal", significa igual ).

Esa es la función `miembro?`
```
(define miembro?
  (lambda (a lat)
    (cond
      ((null? lat) #f)
      (else (or (eq? (car lat) a)
                (miembro? a (cdr lat)))))))
```
Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(papa puré y carne asada)`

#t,
    porque el átomo `carne` es uno de los átomos de `lat`, `(papa puré y carne asada)`.

-----------------

Como determinamos el valor `#t` por esa aplicación?

El valor es determinado por haciendo las preguntas sobre `(miembro? a lat)`.
ayuda: escribe la definición de la función `miembro?` y ver eso durante estas trabajando en las proximas preguntas.

-----------------

Que es la primera pregunta de `(miembro? a lat)`

`(null? lat)`.
    Eso tambien es la primera pregunta de `lat?`.

-----------------

El Primer Mandamiento
(preliminario)

Siempre pregunta `null?` por la primera pregunta en cualquier función.

-----------------

Que significa la linea `((null? lat) #f)` cuando `lat` es `(papa puré y carne asada)`

`(null? lat)` pregunta si `lat` es la lista null. Si es la lista null, el valor es `#f`, porque el átomo `carne` no esta en `lat`. Si no es la lista null, vamos a la proxima pregunta. En eso caso, no es null, entonces vamos a la proxima pregunta.

-----------------

Que es la proxima pregunta?

`else`.

-----------------

Por qué `else` es la proxima pregunta?

Porque no necesitamos preguntar nada mas.

-----------------

`else` es una pregunta, en serio?

Si, `else` es un pregunta que siempre tiene el valor verdad.

-----------------

¿Qué significa la linea `(else (or (eq? (car lat) a) (member? a (cdr lat))))`

Ahora sabemos que `lat` no es null, tenemos que encontrar si el `car` de `lat` es el mismo átomo de `a`, o si `a` es adentro el resto de `lat`. La repuesta `(or (eq? (car lat) a) (miembro? a (cdr lat)))` hace eso.

-----------------

Verdad o falso:
```
(or (eq? (car lat) a)
    (member? a (cdr lat)))
```
cuando `a` es carne y `lat` es `(papa puré y carne asada)`

Vamos a ir viendo cada pregunta para saber.

-----------------

Que es la sengunda pregunta de `(or ...)`

`(member? a (cdr lat))`.
    Esa es una referencia a la función con el argumento `lat` cambiada por `(cdr lat)`.

-----------------

Ahora que son los argumentos de `miembro?`

`a` es `carne` y `lat` es ahora `(cdr lat), especificamente `(puré y carne asada)`.

-----------------

Que es la proxima pregunta?

`(null? lat)`.
    Recuerda el Primer Mandaminto.

-----------------

Es `(null? lat)` verdad o valso cuando `lat` es `(puré y carne asada)`

#f--falso.

-----------------

Que hacemos ahora?

Hacemos la proxima pregunta.

-----------------

Que es la poxima pregunta?

`else`.

-----------------

Que es la significa de 
```
(or (eq? (car lat) a)
  (member? a (cdr lat)))
```

```
(or (eq? (car lat) a)
  (member? a (cdr lat)))
```
Realiza si `a` es `eq?` a la `car` de `lat` o si `a` es un miembro de la `cdr` de `lat` por referencia de la función.

-----------------

Es a `eq?` a el `car` de `lat`

No, porque `a` es `carne` y la `car` de `lat` es `puré`.

-----------------

Entonces, que hacemos siguente?

Preguntamos `(miembro? a (cdr lat))`

-----------------

Ahora, que son los argumentos de `miembro?`

`a` es `carne`, y `lat` es `(y carne asada)`.

-----------------

Que es la siguente pregunta?

`(null? lat)`.

-----------------

Que hacemos ahora?

Pasamos a la proxima pregunta, porque `(null? lat)` es falso.

-----------------

Que es la siguente pregunta?

`else`.

-----------------

Que es el valor de
```
(or (eq? (car lat) a)
    (miembro? a (cdr lat)))
```

El valor de `(miembro? a (cdr lat))`.

-----------------

Por qué?

Porque `(eq? (car lat) a)` es falso.

-----------------

Que hacemos ahora?

Recursion con referencia a la función con nuevos argumentos.

-----------------

Que son los nuevos argumentos?

`a` es `carne`, y `lat` es `(carne asada)`.

-----------------

Que es la siguente pregunta?

`(null? lat)`.

-----------------

Que hacemos ahora?

Porque `(null? lat)` es falso, vamos a la proxima pregunta.

-----------------

Que es la proxima pregunta?

`else`.

-----------------

Que es el valor de 
```
(or (eq? (car lat) a)
    (miembro? a (cdr lat)))
```

#t,
    porque `(car lat)` es `carne`, y `a` es `carne`. Son lo mismo átomo. Entonces, `(or ...)` resulta en `#t`.

-----------------

Que es el valor de el aplicación `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(carne asada)`

`#t`,
    porque `carne` es tambien un miembro de `(carne asada)`.

-----------------

Que es el valor de el aplicación `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(y carne asada)`

`#t`,
    porque `carne` es tambien un miembro de  la `lat` `(y carne asada)`.

-----------------

Que es el valor de el aplicación `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(puré y carne asada)`

`#t`,
    porque `carne` es tambien un miembro de  la `lat` `(puré y carne asada)`.

-----------------

Que es el valor de el aplicación `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(papa puré y carne asada)`

`#t`,
    porque `carne` es tambien un miembro de  la `lat` `(papa puré y carne asada)`. Y eso es nuestro `lat` original.

-----------------

Solo para estar seguta que entendiste correcto, vamos a hacerlo rapidamente otra vez. Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(papa puré y carne asada)`

`#t`
   Puede ayudar si ves la definición de `miembro?` y su argumentos en mismo tiempo con responder en la siguente preguntas.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

else

Sí.

-----------------

`(or (eq? (cat lat) a)
     (miembro? a (cdr lat)))`

Posiblemente

-----------------

`(eq? (car lat) a)`

No. Vamos a proxima pregunta.

-----------------

Que siguente?

Recursion con `a` y `(cdr lat)` cuando `a` es `carne` y `(cdr lat)` es `(papa puré y carne asada)`

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`else`

Sí, pero `(eq? (cat lat) a)` es falso.
Hace recursion con `a` y `(cdr lat)` cuando `a` es `carne` y `(cdr lat)` es `(y carne asada)`.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`else`

Sí, pero `(eq? (car lat) a)` es falso. Hace recusion con `a` y `(cdr lat)`. Eso vez `a` es `carne` y `(cdr lat)` es `(carne asada)`.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`(eq? (car lat) a)`

Sí, el valor es #t.

-----------------

`(or (eq? (car lat) a)
     (miembro? a (cdr lat)))`

#t

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(carne asada)`?

#t

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(y carne asada)`?

#t

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(puré y carne asada)`?

#t

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `carne` y `lat` es `(papa puré y carne asada)`?

#t

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `hidago` y `lat` es `(pan y salmon)`

#f.

-----------------

Vamos a ver porque es #f. Que es la primer pregunta de `miembro?`?

`(null? lat)`.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`else`

Sí, pero `(eq? (car lat) a)` es falso. Hace recusión con `a` y `(cdr lat)`. Esa vez `a` es `higado` y `(cdr lat)` es `(y salmon)`.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`else`

Sí, pero `(eq? (car lat) a)` es falso. Hace recursión con `a` y `(cdr lat)`. Esa vez `a` es `hidago` y `(cdr lat)` es `(salmon)`.

-----------------

`(null? lat)`

No. Vamos a la proxima linea.

-----------------

`else`

Sí, pero `(eq? (car lat) a)` es todavia falso. Hace recursión con `a` y `(cdr lat)`. Esa vez `a` es `hidago` y `(cdr lat)` es `()`.

-----------------

`(null? lat)`

Sí.

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `hidago` y `lat` es `()`.

`#f`

-----------------

Que es el valor de
```
(or (eq? (car lat) a)
    (miembro? a (cdr lat)))
```
cuando `a` es `hidago` y `lat` es `(salmon)`

`#f`

-----------------


Que es el valor de `(miembro? a lat)` cuando `a` es `hidago` y `lat` es `(salmon)`.

`#f`

-----------------

Que es el valor de
```
(or (eq? (car lat) a)
    (miembro? a (cdr lat)))
```
cuando `a` es `hidago` y `lat` es `(y salmon)`

`#f`

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `hidago` y `lat` es `(y salmon)`.

`#f`

-----------------

Que es el valor de
```
(or (eq? (car lat) a)
    (miembro? a (cdr lat)))
```
cuando `a` es `hidago` y `lat` es `(pan y salmon)`

`#f`

-----------------

Que es el valor de `(miembro? a lat)` cuando `a` es `hidago` y `lat` es `(pan y salmon)`.

`#f`

-----------------

¿Creas en todo eso? Entonces puedes descansar!






