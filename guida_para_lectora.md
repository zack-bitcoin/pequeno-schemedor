Guida para la lectora
=================

      Debe leer despacio, y con cuidado. Debe tener por los menos dos descansos durante leyendo, no leas todo en un vez. Lee los capitulos en lo correcto orden. Si no entiende un capitulo entera, va a entender lo siguiente menos. Cada pregunta es mas dificil. Debe tener poder responder a las mas facil antes de hace los mas dificiles.
      Eso libro es una conversacion sobre programas interesantes. Si puedes, debes hacer los ejemplos durante leyendo. Software para hacer la idoma Scheme es muy disponible. Son pocos diferencias en cada Scheme, pero todos son basicamente mismo en todo mundo. Para usar Scheme por eso libro, necesita definar los functiones `atom?`, `sub1`, y `add1`. Aca es un definición por `atom?`.
```
(define atom?
  (lambda (x)
    (and (not (pair? x)) (not (null? x )))))
```
     Para saber si tu Scheme tiene lo corecto definición de `atom?`, proba `(atom? (quote ()))`. debe resultar en `#f`. Eso libro tambien puede funciar con un lisp mas moderna, como Common Lisp. Para funciar con Lisp, puede crear la función `atom?` como asi:
```
(defun atom? (x)
  (not (listp x)))
```
y las porgramas quizas necesita estar modificada un poco.
  En capitulo 4 creamos los basicos de aritmetico usando los operaciónes `add1`, `sub1`, y `zero?`. Necesitas crear `add1` y `sub1` porque no existe por defaulto en scheme.
  Eso Libro no tiene definiciónes formales. Puedes crear su proprio definición, y como asi es mas facil recuerdar y entender. Pero debes saber y entender los Reglas Y Mandamientos antes de pasar por ellos. La estrategia para aprender Scheme es en saber los patrones. Los Mandamientos son patrones que ya veaste. En el principio del libro los conceptos son sincilla, y mas tarde expandimos en ellos. Deben saber tambien que todo en eso libro si es Scheme, pero tambien Scheme tiene mas que pueden explicar en eso libro introductoria. Despues de estas maestro de eso libro, puedes leer y entender otro libros mas comprehensivos sobre Scheme.
  Estas lista iniciar. Buena suerte! Esperamos que puedes disfrutar los desafíos en los siguente paginas.


