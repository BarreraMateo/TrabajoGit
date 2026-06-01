# git branch y git checkout

## git branch

### ¿Para qué sirve?

`git branch` sirve para crear, visualizar y administrar ramas dentro de un repositorio.

Las ramas permiten trabajar en nuevas funcionalidades o realizar pruebas sin modificar directamente la rama principal del proyecto.

### Ver las ramas existentes

```bash
git branch
```

Resultado:

```text
* main
  desarrollo
```

El asterisco (*) indica la rama en la que nos encontramos actualmente.

### Crear una nueva rama

```bash
git branch nueva-rama
```

Ejemplo:

```bash
git branch login
```

Con este comando se crea una rama llamada `login`, aunque todavía seguimos ubicados en la rama actual.

### Eliminar una rama

```bash
git branch -d login
```

Este comando elimina una rama que ya no se utiliza.

### Utilidad

Las ramas son muy utilizadas para:

* Desarrollar nuevas funcionalidades.
* Realizar pruebas sin afectar el proyecto principal.
* Trabajar en equipo sin modificar el trabajo de otros integrantes.
* Corregir errores de manera aislada.

---

# git checkout

## ¿Para qué sirve?

`git checkout` sirve para cambiar entre ramas o volver a versiones anteriores del proyecto.

### Cambiar de rama

Supongamos que tenemos una rama llamada `login`.

```bash
git checkout login
```

Resultado:

```text
Switched to branch 'login'
```

A partir de ese momento todos los cambios se realizarán en esa rama.

### Volver a la rama principal

```bash
git checkout main
```

Resultado:

```text
Switched to branch 'main'
```

### Crear y cambiar de rama al mismo tiempo

```bash
git checkout -b perfil
```

Este comando crea una nueva rama llamada `perfil` y cambia automáticamente a ella.

### Utilidad

`git checkout` permite:

* Cambiar entre ramas.
* Probar diferentes versiones del proyecto.
* Volver a commits anteriores.
* Trabajar en distintas funcionalidades de forma separada.

---

## Ejemplo de uso conjunto

```bash
git branch login
git checkout login
```

O de forma abreviada:

```bash
git checkout -b login
```

En ambos casos terminaremos trabajando en una rama llamada `login`.

---

## Resumen

| Comando                | Función                        |
| ---------------------- | ------------------------------ |
| `git branch`           | Muestra o administra ramas     |
| `git branch nombre`    | Crea una nueva rama            |
| `git branch -d nombre` | Elimina una rama               |
| `git checkout rama`    | Cambia de rama                 |
| `git checkout -b rama` | Crea y cambia a una nueva rama |

### Conclusión

Los comandos `git branch` y `git checkout` son fundamentales para trabajar con ramas en Git. Permiten organizar mejor el desarrollo, realizar pruebas de manera segura y mantener separado el trabajo de cada funcionalidad dentro de un proyecto.
