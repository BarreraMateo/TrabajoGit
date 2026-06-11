## git rm
El comando git rm sirve para borrar archivos del proyecto y que Git registre esa eliminación. Es una forma más práctica de eliminar archivos porque Git ya sabe que ese archivo dejó de existir y lo deja listo para el próximo commit.

## Sintaxis
git rm nombreArchivo
Ejemplo : git rm informe.txt

Con este comando se elimina el archivo informe.txt y Git detecta automáticamente el cambio.

## ¿Para qué se usa?
-Para eliminar archivos que ya no se van a usar.
-Para mantener el proyecto más ordenado.
-Para que Git registre correctamente que un archivo fue eliminado.
## Utilidades:
Cuando trabajamos en un proyecto, muchas veces hay archivos de prueba o documentos que dejan de ser necesarios. Con git rm podemos eliminarlos y Git guarda ese cambio para que quede registrado en el historial.
Commit de la eliminación: git commit -m "Eliminé el archivo informe.txt"

## git mv
El comando git mv se usa para cambiar el nombre de un archivo o moverlo de carpeta sin perder el seguimiento que hace Git sobre él.

## Sintaxis
git mv nombreActual nuevoNombre
Ejemplo para renombrar: git mv documento.txt informe.txt

En este caso, el archivo cambia de nombre y Git registra la modificación.

Ejemplo para mover un archivo: git mv informe.txt documentos/informe.txt
El archivo se mueve a la carpeta documentos.

## ¿Para qué se usa?
-Para renombrar archivos.
-Para mover archivos entre carpetas.
-Para reorganizar el proyecto sin perder el historial de cambios.
## Utilidades:
Este comando resulta útil cuando el proyecto empieza a crecer y necesitamos ordenar mejor los archivos. En lugar de moverlos manualmente, Git registra todo el proceso y mantiene el control de versiones correctamente.

Commit del cambio: git commit -m "Moví y renombré archivos del proyecto"

## Conclusión
Los comandos git rm y git mv son herramientas muy útiles para administrar los archivos de un repositorio. Con git rm podemos eliminar archivos que ya no sirven y con git mv podemos moverlos o cambiarles el nombre de forma más ordenada. Ambos ayudan a mantener el proyecto organizado y a que todos los cambios queden registrados en Git.