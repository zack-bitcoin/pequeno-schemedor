Diez Mandamientos
===========

1-
Cuando estas usando recursion en una lista de atomos, `lat`, preguntas dos cosas sobre eso: `(null? lat)` y `else`.
Cuando estas usando recursion en un numero, `n`, preguntas dos cosas sobre eso: `(zero? n)` y `else`.
Cuando estas usando recusion en una lista de expresiones-S, `l`, preguntas tres cosas sobre eso: `(null? l)`, `(atom? (car l))` y `else`.

2-
Usas `cons` para construir listas.

3-
Cuando estas construyendo listas, descrubes la primer elemento typical, y `cons` eso con lo recusion natural.

4-
Cuando estas usando recusion, debes cambiar por lo menos un argumento cada vez.
Cuando estas usando recusion en un lista de atomos, `lat`, usas `(cdr lat)`
Cuando estas usando recusion en un numero, `n`, usas `(sub1 n)`.
Y cuando estas usando recusion en una lista de expresiones-S, `l`, usas `(car l)` y `(cdr l)` sino `(null? l)` tampoco `(atom? (car l))` son verdad.

Cada vez es necesario que eso es cambiando mas cerca el terminación.
Necesitas probar lo argumento cambiando cada vez por lo condicion de terminación:
cuando usando `cdr`, el condicion de terminación es `null?` y
cuando usando `sub1`, el condicion de terminación es `zero?`.

5-
Cuando construyendo un valor con `+`, siempre usas 0 por el valor de la linea de terminación, porque agregando con 0 no cambia el valor.
Cuando construyendo un valor con `*`, siempre usas 1 por el valor de la linea de terminación, porque multiplicando con 1 no cambia el valor.
Cuando construyendo un valor con `cons`, siempre considerar `()` por el valor de la linea de terminación.

6-
Simplificar un función solo despues de es correcto.

7-
Usas recursion en los partes de tiene mismo forma.
* en las sublistas de listas.
* en los subexpresiónes de un expresión.

8-
Usas mas funciónes to abstractar desde representaciónes.

9-
Usas nuevas funciónes para abstractar los patrones comones.

10-
Creas funciónes para recoger mas de uno valor en una vez.