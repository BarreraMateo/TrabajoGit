# git diff

### ¿Para qué sirve?
git diff sirve para ver las diferencias exactas, línea por línea, entre los cambios que estamos haciendo en nuestros archivos y el último commit guardado. Nos muestra en color rojo lo que se borró y en verde lo que se agregó.

### Ejemplo
Para comparar las modificaciones actuales antes de agregarlas al área de preparación:
```git diff```

# git show
¿Para qué sirve?
git show sirve para inspeccionar los detalles de un punto de control específico en el historial. Nos muestra el autor, la fecha, el mensaje y todos los cambios exactos que introdujo ese commit usando su identificador único (hash).

# Ejemplo
Para revisar qué se modificó en un commit determinado:

```git show a1b2c3d ```

# git blame
¿Para qué sirve?
git blame sirve para ver el historial de modificaciones de un archivo línea por línea. Nos muestra de forma detallada qué usuario del grupo escribió cada renglón y en qué commit lo hizo, siendo una herramienta clave para la autoría en el trabajo en equipo.

Ejemplo
Para examinar quién modificó las líneas del archivo principal:
``` git blame README.md ```
Conclusión
Mientras que git diff nos ayuda a revisar nuestros cambios en tiempo real antes de guardarlos, git show y git blame nos permiten auditar el historial pasado para entender el recorrido del proyecto y la participación de cada integrante.