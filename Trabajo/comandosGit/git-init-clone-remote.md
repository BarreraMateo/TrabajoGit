
## git init
sirve para iniciar un repositorio Git en una carpeta. A partir de ese momento, Git comenzará a controlar los cambios de los archivos dentro de ese proyecto.
Ejemplo: tenemos unas carpetas ya realizadas
git init
Initialized empty Git repository in C:/MiProyecto/.git/
Git crea una carpeta oculta llamada .git donde almacena toda la información del repositorio: 
MiProyecto/
├── .git/
├── app.js
└── package.json

Uso típico:
Cuando se crea un proyecto desde cero:

mkdir MiProyecto
cd MiProyecto
git init

## git clone
sirve para descargar una copia completa de un repositorio remoto a tu computadora. Además de descargar los archivos, configura automáticamente la conexión con el repositorio original.
Supongamos que tienes este repositorio en GitHub: https://github.com/usuario/proyecto.git
Para copiarlo a tu computadora ejecutas: git clone https://github.com/usuario/proyecto.git

Resultado:

Cloning into 'proyecto'...
Receiving objects: 100% (120/120)
Resolving deltas: 100% (45/45)

Git crea una carpeta:
proyecto/
├── app.js
├── package.json
└── README.md
Y ya queda vinculada al repositorio remoto.

## git remote---Fetch--push--actividades que se pueden hacer 
sirve para administrar las conexiones entre tu repositorio local y los repositorios remotos (por ejemplo, en GitHub).
Un repositorio remoto es una copia de un proyecto alojada en un servidor, a la que puedes enviar (push) o desde la que puedes descargar (pull) cambios.
Al hacer git remote , puede salir "origin" de resultado que es el nombre que Git asigna por defecto al repositorio remoto principal. Luego con el git remote -v podemos ver la url del repo : ejemplo: 
origin  https://github.com/usuario/proyecto.git (fetch) URL utilizada para descargar cambios.
origin  https://github.com/usuario/proyecto.git (push) URL utilizada para subir cambios.

Con el git remote add origin https://github.com/usuario/proyecto.git tenemos un  repositorio en GitHub y lo podemos vincular en un  proyecto local.
Con el git remote set-url origin https://github.com/usuario/nuevo-proyecto.git podemos cambiar de URL de un remoto.
Con el git remote remove origin podemos eliminar un remoto.
