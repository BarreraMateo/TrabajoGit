# PULL, PUSH y FETCH

## GIT PULL
`git pull` sirve para traer los cambios que existan en el GitHub del repositorio remoto y fusionarlos con tu repositorio local 

### EJEMPLO

Antes del git pull

```text 
[Repositorio en GitHub] ────► Contiene la versión antigua
│
├─── Tu compañero sube un cambio ───► El repositorio ahora tiene los nuevos cambios subidos
│
[Tu Computadora] ───────► Sigue teniendo la versión antigua
```
Si queres subir cambios sin antes hacer el `git pull origin main`, git no te va a dejar.

## GIT PUSH

`git push` Sirve para enviar los commits locales a el repositorio remoto 

### EJEMPLO
```bash
git add index.html

git commit -m "Agregado el botón de inicio de sesión"

git push -u origin main
```
```text 
push = subir cambios
origin = remoto
main = rama principal
```


## GIT FETCH

`git fetch` Trae la información del repositorio remoto pero, a diferencia del git pull lo hace de forma segura haciendo que no haya ningun conflicto.

```bash
git fetch origin

```


Git te responde 

```text
* branch            dev        -> FETCH_HEAD
```
```bash
git merge origin/dev
```

Esto te actualiza tu rama y trae los cambios del repositorio remoto sin crear ninguna colision

