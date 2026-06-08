# HEAD y commits anteriores

## ¿Qué es HEAD?

`HEAD` es una referencia que utiliza Git para indicar en qué commit nos encontramos actualmente.

Normalmente apunta al último commit de la rama en la que estamos trabajando.

Por ejemplo:

```text
main
  |
  v
A --- B --- C (HEAD)
```

En este caso, `HEAD` apunta al commit más reciente de la rama `main`.

---

## Ver el commit actual

Podemos ver el commit actual utilizando:

```bash
git log --oneline
```

Resultado:

```text
a1b2c3d Último commit realizado
b2c3d4e Corrección de errores
c3d4e5f Primera versión
```

En este ejemplo, `HEAD` apunta al commit `a1b2c3d`.

---

## Volver a un commit anterior

Git permite movernos temporalmente a un commit anterior.

Ejemplo:

```bash
git checkout b2c3d4e
```

Resultado:

```text
Note: switching to 'b2c3d4e'
```

A partir de ese momento podremos visualizar cómo estaba el proyecto en ese commit.

---

## HEAD~1 y HEAD~2

También es posible referirse a commits anteriores utilizando la notación `HEAD~`.

### Volver al commit anterior

```bash
git checkout HEAD~1
```

Significa:

```text
HEAD actual -> commit anterior
```

### Volver dos commits atrás

```bash
git checkout HEAD~2
```

Significa:

```text
HEAD actual -> dos commits anteriores
```

---

## Ejemplo

Supongamos el siguiente historial:

```text
A --- B --- C --- D (HEAD)
```

* `HEAD` → D
* `HEAD~1` → C
* `HEAD~2` → B
* `HEAD~3` → A

---

## Utilidad

HEAD permite:

* Identificar el commit actual.
* Consultar versiones anteriores del proyecto.
* Recuperar información de commits pasados.
* Utilizar comandos como `checkout`, `reset` y `revert`.

---

## Resumen

| Referencia | Significado        |
| ---------- | ------------------ |
| `HEAD`     | Commit actual      |
| `HEAD~1`   | Commit anterior    |
| `HEAD~2`   | Dos commits atrás  |
| `HEAD~3`   | Tres commits atrás |

### Conclusión

`HEAD` es una referencia fundamental dentro de Git, ya que indica la posición actual dentro del historial de commits. Gracias a ella es posible navegar entre distintas versiones del proyecto y consultar estados anteriores cuando sea necesario.
