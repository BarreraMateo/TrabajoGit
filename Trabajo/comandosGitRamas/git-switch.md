## GIT switch 
Es un comando introducido en versiones más recientes de Git (a partir de la 2.23) que sirve para cambiar de rama de una forma más clara y específica que git checkout.
Git decidió separar funciones:

git switch → cambiar de rama.
git restore → restaurar archivos.
Así se evita la confusión que generaba git checkout, que hacía ambas cosas.

## Los usos más comunes son:

Cambiar a una rama existente: git switch nombre-de-rama
Crear una nueva rama y moverte a ella en un solo paso:git switch -c nueva-rama
Volver a la rama anterior:git switch -

## ¿Para qué sirve?
-Para moverte entre ramas de forma más intuitiva.

-Para crear y cambiar a una nueva rama rápidamente.

-Para evitar errores al usar git checkout, ya que switch solo se ocupa de ramas y no de archivos.
