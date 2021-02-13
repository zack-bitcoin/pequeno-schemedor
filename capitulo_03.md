Capitulo 3. Cons lo Magnífico
==============

Que es `(rembro a lat)` cuando `a` es menta y `lat` es `(cordero picante y gelatina de menta)`

`(cordero picante y gelatina de)`
    "rembro" significa 'rem'over un miem'bro'.

-----------------

`(rembro a lat)` cuando `a` es menta y
`lat` es `(cordero picante y gelatina de menta de sabor menta)`

`(cordero picante y gelatina de de sabor menta)`.

-----------------

`(rembro a lat)` cuando `a` es `pan` y `lat` es `(panzeta lechuga y tomate)`

`(panzeta lechuga y tomate)`.

-----------------

`(rembro a lat)` cuando a es `taza` y
`lat` es `(taza de cafe y taza de té)`

`(de cafe y taza de té)`.

-----------------

Que hace `(rembro a lat)`?

Toma un átomo y una lat por su argumentos, y crea nueva lat. El nuevo lat es similar a lo original, pero saqué lo primer ocurrencia de el átomo.

-----------------

Que hacemos para calcular rembro?

Primera vamos a hacer `(null? lat)`-- el Primer Mandamiento.

-----------------

Y si `(null? lat)` es verdad?

El resulto es ().

-----------------

Que sabemos si `(null? lat)` no es verdad?

Sabemos que debe ser por lo menos un átomo en la lat.

-----------------

Hay unas otras preguntas debemos preguntar sobre la lat?

No. Una lat puede ser vacio, o puede contener por lo menos un átomo.

-----------------

Que hacemos si sabemos que la lat tiene por lo menos un atomo?

Preguntamos si `a` es igual a `(car lat)`

-----------------

Como preguntamos?

Usando
```
(cond
    (____ ____)
    (____ ____))
```

-----------------

Como preguntamos si `a` es igual a `(car lat)`

`(eq? (car lat) a)`

-----------------

Que sería el valor de `(rembro a lat)` si `a` fue igual a `(car lat)`.

`(cdr lat)`.

-----------------

Que hacemos si `a` no es igual a `(car lat)`

Quieremos guardar `(car lat)`, pero tambien realizar si `a` es adentro el resto de lat.

-----------------

Como removemos la primera ocurrencia de `a` en el resto de `lat`.

`(rembro a (cdr lat))`

-----------------

Hay otros preguntas debemos preguntar?

No.

-----------------

Ahora, vamos a escribir que tenemos hasta ahora.
```
(define rembro
  (lambda (a lat)
    (cond
      ((null? lat) (quote ()))
      (else
        (cond
          ((eq? (car lat) a) (cdr lat))
          (else (rembro a
                  (cdr lat)))))))))
```
Que es el valor de `(rembro a lat)` cuando `a` es `y` y `lat` es `(panzeta lechuga y tomate)`.

`(panzeta lechuga tomate)`.
(ayuda: Copia eso función con `cons` y los argumentos `a` y `lat` para tener referencia con las siguentes preguntas)

-----------------

Ahora, vamos a ver si esa función funciona. Que es la primer pregunta?

`(null? lat)`.

-----------------

Que hacemos ahora?

Va a la siguente linea y preguntar la siguente pregunta.

-----------------

`else`

Verdad.

-----------------

¿Que es siguente?

Pregunta la siguente pregunta.

-----------------

(ea? (car lat) a)

Verdad, entonces el valor es `(cdr lat)`. En eso caso, es la lista `(lechuga y tomate)`.

-----------------

Eso es el resultado correcto?

Sí, poque es el original lista sin el atomo `panzeta`.

-----------------

Pero, eso fue buen ejemplo?

No sabemos. Vamos a probar otro ejemplo.

-----------------

Que hace `rembro`?

Se toma un atomo y un lat por su argumentos, y crea un nueva lat con la primera occurencia de el atomo en el viejo lat removido.

-----------------

¿Que hacemos ahora?

Comparamos cada atomo de la lat con el atomo `a`, y si el comparación es falso construyemos una lista que inicia con el atomo comparando justo.

-----------------

Que es el valor de `(rembro a lat)` cuando `a` es `y` y `lat` es `(panzeta lechuga y tomate)`

`(panzeta lechuga tomate)`.

-----------------

Vamos a ver si la funcion `rembro` funciona.
Que es la primera pregunta de `rembro`

`(null? lat)`

-----------------

Que hacemos ahora?

Vamos a la proxima pregunta.

-----------------

`else`

Bien, pregunta la proxima linea.

-----------------

`(eq? (car lat) a)`

No, entonces vamos a la proxima pregunta.

-----------------

Que significa `(else (rembro a (cdr lat)))`

`else` siempre es verdad. El resto de la linea dice que debemos hacer recursion con `a` y `(cdr lat)`, donde `a` es `y` y `(cdr lat)` es `(lechuga y tomate)`.

-----------------

`(null? lat)`

No, entonces vamos a la proxima linea.

-----------------

`else`

Verdad.

-----------------

`(eq? (car lat) a)`

No, entonces vamos a la proxima linea.

-----------------

Que significa `(rembro a (cdr lat))`

Hacemos recursion donde `a` es `y` y `(cdr lat)` es `(y tomate)`.

-----------------

`(null? lat)`

No, entonces vamos a la proxima linea, y preguntamos la proxima pregunta.

-----------------

`else`

Verdad.

-----------------

(pagina 37)



