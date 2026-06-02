# git merge y git rebase

## git merge

### ¿Para qué sirve?

`git merge` sirve para unir los cambios de una rama con otra.

Generalmente se utiliza cuando terminamos de trabajar en una funcionalidad dentro de una rama y queremos incorporar esos cambios a la rama principal.

### Ejemplo

Supongamos que estamos trabajando en una rama llamada `login`.

Primero cambiamos a la rama principal:

```bash
git checkout main
```

Luego unimos los cambios de la rama `login`:

```bash
git merge login
```

Resultado:

```text
Updating a1b2c3d..b2c3d4e
Fast-forward
 app.js | 10 ++++++++++
```

Los cambios realizados en la rama `login` ahora forman parte de la rama `main`.

### Utilidad

`git merge` permite:

* Unir ramas.
* Incorporar nuevas funcionalidades al proyecto principal.
* Integrar el trabajo realizado por distintos integrantes de un equipo.
* Mantener el historial de desarrollo.

---

## git rebase

### ¿Para qué sirve?

`git rebase` también sirve para integrar cambios entre ramas, pero lo hace reorganizando el historial de commits.

Su objetivo principal es mantener un historial más limpio y ordenado.

### Ejemplo

Supongamos que estamos en una rama llamada `login` y queremos actualizarla con los cambios más recientes de `main`.

```bash
git checkout login
```

```bash
git rebase main
```

Git tomará los commits de la rama `login` y los volverá a aplicar sobre la última versión de `main`.

### Utilidad

`git rebase` permite:

* Mantener un historial más lineal.
* Evitar commits de merge innecesarios.
* Actualizar una rama con los últimos cambios de otra rama.

### Importante

Cuando se trabaja en equipo se debe tener cuidado al utilizar `rebase`, ya que puede modificar el historial de commits.

Por este motivo suele utilizarse principalmente en ramas locales antes de compartir cambios con otros desarrolladores.

---

## Diferencia entre git merge y git rebase

| Comando      | Función                                                     |
| ------------ | ----------------------------------------------------------- |
| `git merge`  | Une dos ramas conservando el historial original             |
| `git rebase` | Reorganiza los commits para generar un historial más lineal |

### Ejemplo de flujo

```bash
git checkout login
git add .
git commit -m "Agrego formulario"

git checkout main
git merge login
```

En este ejemplo, los cambios desarrollados en la rama `login` se incorporan a la rama principal.

---

## Conclusión

Los comandos `git merge` y `git rebase` permiten integrar cambios entre ramas. El primero conserva el historial original de desarrollo, mientras que el segundo reorganiza los commits para obtener un historial más limpio y ordenado.
