Capitulo 1: Jugetes
===========

-----------------

Es verdad que eso es un átomo?
  `atom`

Sí,
   porque `atom` es un hilo de caracteres iniciando con la letra `a`.

-----------------

Es verdad que eso es un átomo?
  `pavo`

Sí,
   porque `pavo` es un hilo de caracteres iniciando con un letra.

-----------------

Es verdad que eso es un átomo?
   `1492`

Sí,
   porque `1492` es un hilo de digitos.

-----------------

Es verdad que eso es un átomo?
   `u`

Sí,
   porque `u` es un hilo de un caracter, que es un letra.

-----------------

Es verdad que eso es un átomo?
   `*abc$`
   
Sí,
   porque `*abc$` es un hilo de caracteres, iniciando con un letra o caractere especial otro de izquierda "(" o derecho ")" parentesis.

-----------------

Es verdad que eso es una lista?
   `(átomo)`

Sí,
   porque `(átomo)` es un átomo adentro de parentesis.

-----------------

Es verdad que eso es una lista?
   `(átomo pavo o)`

Sí,
   porque eso es un coleccion de átomos adentro de parentesis.

-----------------

Es verdad que eso es una lista?
   `(átomo pavo) o`

No,
   porque eso es actualmente dos expresiones-S no adentro de parentesis. El primer es una lista de dos átomos, y la segunda es un átomo.

-----------------

Es verdad que eso es una lista?
   `((átomo pavo) o)`

Sí,
   porque los dos expressiones-S ahora son adentro de parentesis.

-----------------

Es verdad que eso es un expresión-S?
   `xyz`

Sí,
   porque todos átomos son expresiónes-S.

-----------------

Es verdad que eso es un expresión-S?
   `(x y z)`

Sí,
   porque es una lista.

-----------------

Es verdad que eso es un expresión-S?
   `((x y) z)`

Sí,
   porque todas listas son expresiónes-S.

-----------------

Es verdad que eso es una lista?
   `(como estas haciendo hasta ahora)`

Sí,
   porque eso es una colección de expresiónes-S adentro de parentesis.

-----------------

Cuantos expresiónes-S son adentro la lista `(como estas haciendo hasta ahora)` y que son?

Cinco,
        `como`, `estas`, `haciendo`, `hasta`, y, `ahora`.

-----------------

Es verdad que eso es una lista?
   `(((como) estas) ((haciendo) (hasta)) ahora)`

Sí,
    porque es un colección de expreciónes adentro de parentesis.

-----------------

Cuantos expresiónes-S son adentro la lista
   `(((como) estas) ((haciendo) (hasta)) ahora)`
y que son?

Tres,
     `((como) estas)`, `((haciendo) (hasta))`, y `ahora`.

-----------------

Es verdad que esa es una lista?
   `()`

Sí,
   porque eso contiene cero expresiónes adentro de parentesis. Eso especial tipo de expresión-S se llama el null (o vacia) lista.

-----------------

Es verdad que eso es un átomo?
   `()`

No,
   porque `()` es una lista.

-----------------

Es verdad que eso es una lista?
   `(()()()())`

Sí,
    porque es un colección de expresiónes-S adentro de parentesis.

-----------------

Que es el `car` de `l` cuando `l` es el argumento `(a b c)`?

`a`,
    porque `a` es el primer átomo de esta lista.

-----------------

Que es el `car` de `l` cuando `l` es `((a b c) x y z)`?

`(a b c)`,
    porque `(a b c)` es el primer expresión-S de esa lista que no es vacia.
    
-----------------

Que es el `car` de `l` cuando `l` es `salchicha`?

no responde,
    porque no puede preguntar por el `car` de un átomo.

-----------------

Que es el `car` de `l` cuando `l` es `()`?

no responde,
    porque no puedes preguntar por el `car` de una lista vacia.
    
-----------------

La Regla de Car
   La primitiva `car` tiene definición solo para listas que no son vacias.

-----------------

Que es el `car` de `l` cuando `l` es `(((salchichas))(y)(pickle) repollo)`

((salchichas)),
   leer como: "la lista de la lista de salchichas"
   `((salchichas))` es la pirmera expreción-S de `l`.

-----------------

Que es `(car l)` cuando `l` es `(((salchichas))(y)(pickle) repollo)`

`((salchichas))`,
    porque `(car l)` es otro forma para preguntar "el `car` de la lista `l`."

-----------------

Que es `(car (car l))` cuando `l` es `(((salchichas))(y))`

`(salchichas)`.

-----------------

Que es el `cdr` of `l` cuando `l` es `(a b c)`

`(b c)`
    porque `(b c)` es la list `l` sin `(car l)`.

"cdr" se llama cuder

-----------------

Que es el `cdr` de `l` cuando `l` es `(hamberguesa)`

().

-----------------

que es `(cdr l)` cuando `l` es `((x) t r)`

`(t r)`
    porque `(cdr l)` es solo otra forma de preguntar por "el `cdr` de la lista `l`".

-----------------

Que es `(cdr a)` cuando `a` es `salchichas`

No responde,
    no puede preguntar por el `cdr` de un átomo.

-----------------

Que es `(cdr l)` cuando `l` is `()`

No responde.
   no puede preguntar por el `cdr` de la lista null.

-----------------

La Regla de Cdr
   La primitiva `cdr` tiene definición solo para listas que no son vacias. El `cdr` de una lista que no es vacia siempre es otra lista.

-----------------

Que es `(car (cdr l))` cuando `l` es `((b)(x y)((c)))`

`(x y)`,
    porque `((x y)((c)))` es `(cdr l)`, y `(x y)` es el `car` de `(cdr l).

-----------------

Que es `(cdr (cdr l))` cuando `l` es `((b)(x y)((c)))`

`(((c)))`,
    porque `((x y)((c)))` es `(cdr l)`, y `(((c)))` es el `cdr` de `(cdr l)`.
    
-----------------

Que es `(cdr (car l))` cuand `l` es `(a (b (c)) d)`

No responde,
   porque `(car l)` es un átomo, y `cdr` solo tiene definicion por listas. Veas La Regla de Cdr.

-----------------

Que acepta `car` por un argumento?

`car` acepta cualquier lista que no es vacia.

-----------------

Que acepta `cdr` por un argumento?

`cdr` acepta cualquier lista que no es vacia.

-----------------

Que es el `cons` de el átomo `a` y la lista `l` cuando `a` es `mani` y `l` es `(manteca y marmelada)`. Eso puede ser escrito "(cons a l)". leas como "cons el átomo a encima la lista l".

`(mani manteca y marmelada)`
    porque `cons` construye una lista. El primer argumento es en el frente de nueva lista.
    
-----------------

Que es el `cons` of `s` y `l` cuando `s` es `(banana y)` y `l` es `(mani manteca y marmelada)`

`((banana y) mani manteca y marmelada)`
    porque `cons` construye nueva lista, y puede hacer cualquier expreción-S en el frente de la nueva lista.

-----------------

Que es `(cons s l)` cuando `s` es `((ayudame) eso)` y `l` es `(es muy ((dificil) para aprender))`

`(((ayudame) eso) es muy ((dificil) para aprender))`.

-----------------

Que acepta `cons` por su argumentos?

`cons` acepta dos argumentos. El primer es cualquier expresión-S, y la segunda es cualquir lista.

-----------------

Que es `(cons s l)` cuando `s` es `(a b (c))` y `l` es ()

`((a b (c)))`
    porque `()` es una lista.

-----------------

Que es `(cons s l)` cuando `s` is `a` y `l` es `()`

`(a)`.

-----------------

Que es `(cons s l)` cuando `s` es `((a b c))` y `l` es `b`

No responde,
   porque el secundo argumento `l` necesita ser una lista.

-----------------

Que es `(cons s l)` cuando `s` is `a` y `l` es `b`

No responde. Porque?

-----------------

La Regla de Cons

   La primitiva `cons` toma dos argumentos. La segunda argumento por `cons` debe ser una lista. El resulto es una lista.

-----------------

Que es `(cons s (car l))` cuando `s` es `a` y `l` es `((b) c d)`

`(a b)`.
   porque?

-----------------

Que es `(cons s (cdr l))` cuando `s` es `a` y `l` es `((b) c d)`

`(a c d)`.
    porque?

-----------------

Es verdad que la lista `l` es la lista null cuando `l` es `()`

Sí,
    porque eso es la lista con cero expreciónes'S. Eso pregunta tambien pueden estar escrito `(null? l)`.

-----------------

Que es `(null? (quote ()))`

Verdad,
    porque `(quote ())` es un forma para escribir la lista null.
    
-----------------

Es `(null? l)` verdad o falso cuando `l` es `(a b c)`

Falso,
    porque `l` es un lista que no es vacia.

-----------------

Es `(null? a)` verdad o falso cuando `a` es `spaghetti`

No responde,
    porque no puedes preguntar `null?` de un átomo.
    
-----------------

La Regla de Null?
    La primitiva `null?` tiene definition solo para listas.

-----------------

Es verdad o falso que `s` es un átomo cuando `s` es `Harry`

Verdad,
    porque `Harry` es un hilo de caracteres iniciando con una letra.

-----------------

Es `(atom? s)` verdad o falso cuando `s` es `Harry`

Verdad,
    porque `(atom? s)` es otra forma de preguntar "Es `s` un átomo?"

-----------------

Es `(atom? s)` verdad o falso cuando `s` es `(Harry tiene una pila de manzanas)`

Falso,
   porque `s` es una lista.

-----------------

Cuantos argumentos acepta `atom?` y que son?

Acepta un argumento. El argumento puede ser cualquier expresión-S.

-----------------

Es `(atom? (car l))` verdad o falso cuando `l` es `(Harry tiene una pila de manzanas)`

Verdad,
    porque `(car l)` es `Harry`, y `Harry` es un átomo.

-----------------

Es `(atom? (cdr l))` verdad o falso cuando `l` es `(Harry tiene una pila de manzanas)`

Falso.

-----------------

Es `(atom? (cdr l))` verdad o falso cuando `l` es `(Harry)`

Falso,
    porque la lista `()` no es un átomo.

-----------------

Es `(atom? (car (cdr l)))` verdad o falso cuando `l` es `(uno dos tres cuatro)`

Verdad,
   porque `(cdr l)` es `(dos tres cuatro)` y `(car (cdr l))` es `dos`. `dos` es un átomo.

-----------------

Es `(atom? (car (cdr l)))` verdad o falso cuando `l` es `(uno (dos tres) cuatro)`

Falso,
    porque `(cdr l)` es `((dos tres) cuatro)`, y `(car (cdr l))` es `(dos tres)`. `(dos tres)` es una lista, no un átomo.

-----------------

Verdad o falso, `a1` y `a2` son lo mismo átomo cuando `a1` es `Harry` y `a2` es `Harry`

Verdad,
   porque `a1` es el átomo `Harry` y `a2` es el átomo `Harry`.

-----------------

Is `(eq? a1 a2)` verdad o falso cuando `a1` es `Harry` y `a2` es `Harry`

Verdad,
    porque `(eq? a1 a2)` es otra forma de preguntar, "`a1` y `a2` son lo mismo non-numero átomo?"
    
-----------------

Es `(eq? a1 a2)` verdad o falso cuando `a1` es `margarina` y `a2` es `mantequilla`?

False,
    porque `a1` y `a2` son átomos diferentes.
    
-----------------

Cuantos argumentos acepta `eq?` y que son?

Acepta dos argumentos. Los dos necesita ser átomos, y no pueden ser numeros.

-----------------

Es `(eq? l1 l2)` verdad o falso cuando `l1` es `()` y `l2` es `(fresa)`

No responde,
    `()` y `(fresa)` son listas.

-----------------

Es `(eq? n1 n2)` verdad o falso cuando `n1` es `6` y `n2` es `7`

No responde,
   `6` y `7` son numeros.
   
-----------------

La Regla de Eq?
   La primitiva `eq?` toma dos argumentos. Cada necesita ser un atom, y no pueden ser numero.

-----------------

Es `(eq? (car l) a)` verdad o falso cuando `l` es `(Mary tiene carne de vaca)` y `a` es `Mary`

Verdad,
    porque `(car l)` es el átomo `Mary`, y el argumento `a` es tambien el átomo `Mary`.
    
-----------------

Es `(eq? (cdr l) a)` verdad o falso cuando `l` es `(acido lactico)` y `a` es `lactico`

No responde,
    Miras La Reglas de Eq? y Cdr.

-----------------

Es `(eq? (car l) (car (cdr l)))` verdad o falso cuano `l` es `(frijoles frijoles necesitamos frijoles dulces)`

Verdad,
    porque es un comparación de el primer y segundo átomos en la lista.

-----------------

