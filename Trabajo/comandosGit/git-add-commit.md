# git add .
sirve para preparar archivos para el próximo commit. Git toma los cambios que selecciones y los coloca en el área de preparación.

Se cambio app.js y alumnos.json (ejemplo)
Ejemplo: git status
hanges not staged for commit:

        modified: app.js

Untracked files:

        alumnos.json

Agregamos archivos        git add .
git status para visualizar: 
Changes to be committed:

        modified: app.js
        new file: alumnos.json

Los archivos ya están preparados para formar parte del próximo commit.



# git commit
sirve para guardar de manera permanente los cambios que fueron agregados con git add.
Cada commit representa una versión o punto de control del proyecto.
Ejemplo: 
git commit -m "Agrego gestión de alumnos"
[main a1b2c3d]
Agrego gestión de alumnos

2 files changed, 15 insertions(+)

Guarda los cambios en el historial de Git.
Genera un identificador único (hash).
Asocia un mensaje descriptivo al cambio realizado.

Verificar si el commit esta visible : git log --oneline

git add <archivo>	Prepara un archivo para el próximo commit
git add .	Prepara todos los cambios del proyecto
git commit -m "mensaje"	Guarda los cambios preparados en el historial