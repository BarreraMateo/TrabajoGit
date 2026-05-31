## git status
sirve para ver el estado actual de tu repositorio: qué archivos fueron modificados, cuáles están preparados para el próximo commit (staged), cuáles no, y si hay archivos nuevos sin seguimiento.

Supongamos que tienes este proyecto:

TP4/
├── app.js
├── package.json
└── README.md

Modificas app.js y creas un archivo nuevo llamado alumnos.json.

Si ejecutas:

git status

Podrías obtener algo como:

On branch main

Changes not staged for commit:
  (use "git add <archivo>..." to update what will be committed)

        modified:   app.js

Untracked files:
  (use "git add <archivo>..." to include in what will be committed)

        alumnos.json

no changes added to commit
¿Qué significa?
modified: app.js
→ Git detectó cambios en app.js, pero todavía no hiciste git add.
Untracked files: alumnos.json
→ Es un archivo nuevo que Git todavía no está siguiendo.

# git log 
sirve para ver el historial de commits de un repositorio. Te muestra quién hizo cada commit, cuándo lo hizo y el mensaje que escribió.

Lo que se ve : commit a1b2c3d4e5f67890abcdef1234567890abcdef12
Author: Mateo Barrera <mateo@email.com>
Date:   Sat May 30 10:15:22 2026 -0300

    Agrego endpoint para listar alumnos

commit b2c3d4e5f67890abcdef1234567890abcdef1234
Author: Mateo Barrera <mateo@email.com>
Date:   Fri May 29 18:42:10 2026 -0300

    Corrijo validaciones de notas

commit c3d4e5f67890abcdef1234567890abcdef123456
Author: Mateo Barrera <mateo@email.com>
Date:   Thu May 28 14:20:05 2026 -0300

    Versión inicial del proyecto

¿Qué muestra?
commit: identificador único del commit (hash).
Author: quién realizó el commit.
Date: fecha y hora.
Mensaje: descripción de los cambios realizados.

Ver historial resumido Muchas veces se usa:

git log --oneline

Salida:

a1b2c3d Agrego endpoint para listar alumnos
b2c3d4e Corrijo validaciones de notas
c3d4e5f Versión inicial del proyecto

Es mucho más cómodo porque muestra:

Hash corto del commit.
Mensaje del commit.

Ver los últimos 3 commits git log -3 o en formato resumido:

git log --oneline -3

Ejemplo:

a1b2c3d Agrego endpoint para listar alumnos
b2c3d4e Corrijo validaciones de notas
c3d4e5f Versión inicial del proyecto

               Flujo
git status          # Ver estado actual
git add .
git commit -m "Nueva funcionalidad"
git log --oneline   # Ver que el commit quedó registrado

Diferencia entre git status y git log
Comando	¿Para qué sirve?
git status	Ver cambios actuales que aún no están confirmados o enviados
git log	Ver el historial de commits realizados
git log --oneline	Ver el historial de forma resumida