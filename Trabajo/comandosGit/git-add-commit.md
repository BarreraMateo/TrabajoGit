# git add

## ¿Para qué sirve?

`git add` sirve para preparar archivos para el próximo commit. Git toma los cambios seleccionados y los coloca en el área de preparación (staging area).

### Ejemplo

Supongamos que se modificó `app.js` y se creó un nuevo archivo llamado `alumnos.json`.

Al ejecutar:

```bash
git status
```

Obtendremos algo similar a:

```text
Changes not staged for commit:

        modified: app.js

Untracked files:

        alumnos.json
```

Luego agregamos los cambios:

```bash
git add .
```

Y verificamos nuevamente:

```bash
git status
```

Resultado:

```text
Changes to be committed:

        modified: app.js
        new file: alumnos.json
```

Los archivos ya están preparados para formar parte del próximo commit.

---

# git commit

## ¿Para qué sirve?

`git commit` sirve para guardar de manera permanente los cambios que fueron agregados previamente con `git add`.

Cada commit representa una versión o punto de control del proyecto.

### Ejemplo

```bash
git commit -m "Agrego gestión de alumnos"
```

Resultado:

```text
[main a1b2c3d]
Agrego gestión de alumnos

2 files changed, 15 insertions(+)
```

### ¿Qué realiza este comando?

* Guarda los cambios en el historial de Git.
* Genera un identificador único llamado hash.
* Asocia un mensaje descriptivo a los cambios realizados.

### Verificar el commit

Para comprobar que el commit fue registrado correctamente:

```bash
git log --oneline
```

### Resumen

| Comando                   | Función                                       |
| ------------------------- | --------------------------------------------- |
| `git add <archivo>`       | Prepara un archivo para el próximo commit     |
| `git add .`               | Prepara todos los cambios del proyecto        |
| `git commit -m "mensaje"` | Guarda los cambios preparados en el historial |

En el flujo normal de trabajo, primero se utiliza git add para preparar los cambios y luego git commit para almacenarlos en el historial del repositorio.