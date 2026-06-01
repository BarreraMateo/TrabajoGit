# git status

## ¿Para qué sirve?

`git status` sirve para ver el estado actual del repositorio. Permite conocer qué archivos fueron modificados, cuáles están preparados para el próximo commit (staged), cuáles no, y si existen archivos nuevos sin seguimiento.

### Ejemplo

Supongamos que tenemos el siguiente proyecto:

```text id="4xmq1s"
TP4/
├── app.js
├── package.json
└── README.md
```

Se modifica `app.js` y se crea un nuevo archivo llamado `alumnos.json`.

Al ejecutar:

```bash id="w0zyx8"
git status
```

Obtendremos algo similar a:

```text id="0d0fwv"
On branch main

Changes not staged for commit:
  (use "git add <archivo>..." to update what will be committed)

        modified: app.js

Untracked files:
  (use "git add <archivo>..." to include in what will be committed)

        alumnos.json

no changes added to commit
```

### ¿Qué significa?

* **modified: app.js** → Git detectó cambios en el archivo, pero todavía no se ejecutó `git add`.
* **Untracked files** → Son archivos nuevos que Git todavía no está siguiendo.
* **Changes not staged for commit** → Existen cambios que aún no fueron preparados para un commit.

---

# git log

## ¿Para qué sirve?

`git log` sirve para visualizar el historial de commits realizados en un repositorio.

Muestra quién realizó cada commit, cuándo se realizó y el mensaje asociado.

### Ejemplo

```bash id="0axbsi"
git log
```

Resultado:

```text id="9ut04w"
commit a1b2c3d4e5f67890abcdef1234567890abcdef12
Author: Mateo Barrera <mateo@email.com>
Date: Sat May 30 10:15:22 2026 -0300

    Agrego endpoint para listar alumnos

commit b2c3d4e5f67890abcdef1234567890abcdef1234
Author: Mateo Barrera <mateo@email.com>
Date: Fri May 29 18:42:10 2026 -0300

    Corrijo validaciones de notas

commit c3d4e5f67890abcdef1234567890abcdef123456
Author: Mateo Barrera <mateo@email.com>
Date: Thu May 28 14:20:05 2026 -0300

    Versión inicial del proyecto
```

### ¿Qué muestra?

* **commit** → Identificador único del commit (hash).
* **Author** → Usuario que realizó el commit.
* **Date** → Fecha y hora de creación.
* **Mensaje** → Descripción de los cambios realizados.

---

## Historial resumido

Muchas veces se utiliza:

```bash id="4th0v2"
git log --oneline
```

Resultado:

```text id="1c6df2"
a1b2c3d Agrego endpoint para listar alumnos
b2c3d4e Corrijo validaciones de notas
c3d4e5f Versión inicial del proyecto
```

Esta opción es útil porque muestra:

* Hash corto del commit.
* Mensaje asociado al commit.

---

## Ver los últimos commits

Para visualizar únicamente los últimos tres commits:

```bash id="kmtd7l"
git log -3
```

O en formato resumido:

```bash id="8vc7nm"
git log --oneline -3
```

Resultado:

```text id="ckjgf6"
a1b2c3d Agrego endpoint para listar alumnos
b2c3d4e Corrijo validaciones de notas
c3d4e5f Versión inicial del proyecto
```

---

## Flujo de trabajo habitual

```bash id="8r3wmq"
git status
git add .
git commit -m "Nueva funcionalidad"
git log --oneline
```

Este flujo permite verificar cambios, prepararlos, registrarlos y comprobar que el commit quedó guardado correctamente.

---

## Diferencia entre git status y git log

| Comando             | Función                                                           |
| ------------------- | ----------------------------------------------------------------- |
| `git status`        | Muestra el estado actual del repositorio y los cambios pendientes |
| `git log`           | Muestra el historial completo de commits                          |
| `git log --oneline` | Muestra el historial de forma resumida                            |

### Conclusión

Los comandos `git status` y `git log` permiten conocer el estado actual del repositorio y consultar el historial de cambios realizados a lo largo del desarrollo del proyecto.
 
 git log --oneline --graph  suele usarse mucho para visualizar ramas y merges.