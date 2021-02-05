Las Cinca Reglas
===============

La Regla de Car
   La primitiva `car` tiene definición solo para listas que no son vacias.

La Regla de Cdr
   La primitiva `cdr` tiene definición solo para listas que no son vacias. El `cdr` de una lista que no es vacia siempre es otra lista.

La Regla de Cons
   La primitiva `cons` toma dos argumentos. La segunda argumento por `cons` debe ser una lista. El resulto es una lista.

La Regla de Null?
   La primitiva `null?` tiene definition solo para listas.

La Regla de Eq?
   La primitiva `eq?` toma dos argumentos. Cada necesita ser un atom, y no pueden ser numero.