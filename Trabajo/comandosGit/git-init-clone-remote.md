# git init

## ¿Para qué sirve?

`git init` sirve para iniciar un repositorio Git en una carpeta. A partir de ese momento, Git comenzará a controlar los cambios de los archivos dentro de ese proyecto.

### Ejemplo

Supongamos que tenemos una carpeta con algunos archivos:

```text
MiProyecto/
├── app.js
└── package.json
```

Ejecutamos:

```bash
git init
```

Resultado:

```text
Initialized empty Git repository in C:/MiProyecto/.git/
```

Git crea una carpeta oculta llamada `.git`, donde almacena toda la información del repositorio.

```text
MiProyecto/
├── .git/
├── app.js
└── package.json
```

### Uso típico

Cuando se crea un proyecto desde cero:

```bash
mkdir MiProyecto
cd MiProyecto
git init
```

---

# git clone

## ¿Para qué sirve?

`git clone` sirve para descargar una copia completa de un repositorio remoto a una computadora.

Además de descargar los archivos, configura automáticamente la conexión con el repositorio original.

### Ejemplo

Supongamos que existe el siguiente repositorio en GitHub:

```text
https://github.com/usuario/proyecto.git
```

Para copiarlo localmente:

```bash
git clone https://github.com/usuario/proyecto.git
```

Resultado:

```text
Cloning into 'proyecto'...
Receiving objects: 100% (120/120)
Resolving deltas: 100% (45/45)
```

Git crea una carpeta con el contenido del proyecto:

```text
proyecto/
├── app.js
├── package.json
└── README.md
```

Además, el repositorio queda vinculado automáticamente al repositorio remoto.

---

# git remote

## ¿Para qué sirve?

`git remote` sirve para administrar las conexiones entre un repositorio local y los repositorios remotos.

Un repositorio remoto es una copia del proyecto alojada en un servidor, desde donde se pueden descargar cambios (`fetch` o `pull`) o enviar cambios (`push`).

### Ver repositorios remotos

```bash
git remote
```

Resultado:

```text
origin
```

`origin` es el nombre que Git asigna por defecto al repositorio remoto principal.

### Ver la URL del repositorio remoto

```bash
git remote -v
```

Resultado:

```text
origin  https://github.com/usuario/proyecto.git (fetch)
origin  https://github.com/usuario/proyecto.git (push)
```

* **fetch:** URL utilizada para descargar cambios.
* **push:** URL utilizada para subir cambios.

### Agregar un repositorio remoto

```bash
git remote add origin https://github.com/usuario/proyecto.git
```

Este comando permite vincular un proyecto local con un repositorio remoto.

### Cambiar la URL de un remoto

```bash
git remote set-url origin https://github.com/usuario/nuevo-proyecto.git
```

Permite modificar la dirección del repositorio remoto.

### Eliminar un remoto

```bash
git remote remove origin
```

Elimina la conexión con el repositorio remoto configurado.

---

## Resumen

| Comando                           | Función                             |
| --------------------------------- | ----------------------------------- |
| `git init`                        | Inicializa un repositorio Git local |
| `git clone <url>`                 | Descarga un repositorio remoto      |
| `git remote`                      | Muestra los remotos configurados    |
| `git remote -v`                   | Muestra los remotos y sus URLs      |
| `git remote add origin <url>`     | Agrega un repositorio remoto        |
| `git remote set-url origin <url>` | Cambia la URL del remoto            |
| `git remote remove origin`        | Elimina un remoto                   |

### Conclusión

Los comandos `git init`, `git clone` y `git remote` permiten crear repositorios, copiar proyectos existentes y administrar la conexión entre el repositorio local y los repositorios remotos.
