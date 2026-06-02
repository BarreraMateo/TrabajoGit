# git help, man y alias

## git help

Sirve para ver la ayuda de un comando de Git.

Ejemplo:

```bash
git help log
```

Al ejecutarlo se abre la documentación relacionada con `git log`, donde se pueden consultar las opciones y parámetros disponibles.

Es útil cuando no recordamos cómo funciona un comando o qué opciones tiene.

---

## man

Sirve para abrir el manual de un comando desde la terminal.

Ejemplos:

```bash
man git-log
```

```bash
man git-diff
```

Al ejecutarlos se muestra información detallada sobre cada comando.

Es una forma rápida de consultar documentación oficial sin buscar en Internet.

---

## alias

Sirve para crear atajos para comandos que usamos frecuentemente.

Ejemplo:

```bash
git config --global alias.gl "log --oneline"
```

A partir de ese momento podremos ejecutar:

```bash
git gl
```

y obtendremos el mismo resultado que:

```bash
git log --oneline
```

Esto permite ahorrar tiempo y escribir menos cuando trabajamos con Git.

---

### Resumen

| Comando    | Función                             |
| ---------- | ----------------------------------- |
| `git help` | Muestra ayuda sobre un comando      |
| `man`      | Muestra el manual de un comando     |
| `alias`    | Permite crear atajos personalizados |

Estos comandos no modifican el repositorio, pero facilitan mucho el trabajo diario y la consulta de información cuando se utiliza Git.
