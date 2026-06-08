## git fetch

## ¿Para qué sirve?

git fetch sirve para descargar los cambios del repositorio remoto hacia nuestra computadora, pero sin mezclarlos con nuestro código local. Permite revisar qué hicieron los demás integrantes en GitHub sin alterar nuestro trabajo.

### Ejemplo
Para actualizar el historial de lo que hay en el servidor remoto:

```git fetch```


Luego de usar este comando, podemos ver las ramas del servidor o revisar los comentarios antes de traer las modificaciones a nuestros archivos.

## git pull

## ¿Para qué sirve?

git pull sirve para descargar las novedades desde el repositorio remoto y mezclarlas directamente en la rama donde estamos parados. Es la unión de descargar los datos y unirlos al proyecto local. Se utiliza frecuentemente al comenzar a trabajar para actualizar nuestros archivos.

### Ejemplo
Si estamos ubicados en la rama principal y queremos tener lo último que se subió a GitHub:

```git pull origin main```

Si otra persona modificó la misma parte de un archivo que nosotros, el comando nos avisará que hay un conflicto que debemos revisar.

## git push
## ¿Para qué sirve?
git push sirve para enviar todos los cambios que guardamos localmente hacia el repositorio en GitHub. De esta manera, el resto del grupo puede acceder a nuestras actualizaciones.

### Ejemplo
Para subir las modificaciones de nuestra rama de trabajo al servidor remoto:

``` git push origin nombre-rama```


# Conclusión
Mientras que git fetch solo descarga información para revisar, git pull la descarga y la aplica directamente sobre nuestros archivos de trabajo. Por otro lado, git push realiza la acción inversa, subiendo nuestros propios cambios locales al servidor para compartirlos con el equipo