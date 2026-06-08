 ## git reset
Función: Mueve el puntero HEAD a un commit anterior.
Nivel de acción: Cambia el historial local, puede borrar commits.
git reset --hard HEAD~1

Cuando usarlo:Cuando querés deshacer commits recientes y no te importa perder cambios; si ya compartiste esos commits en un repositorio remoto, puede generar conflictos.

## git revert
Función: Crea un nuevo commit que revierte otro commit existente.
Nivel de acción: No altera el historial, mantiene trazabilidad.
git revert <id-del-commit>

Cuando usarlo: Cuando querés revertir un commit sin eliminarlo, ideal para repositorios compartidos porque conserva el historial intacto.

## git restore
Función: Restaura archivos al estado anterior.
Nivel de acción: Solo afecta el working directory (los archivos locales).
git restore archivo.txt

Cuando usarlo: Cuando querés descartar cambios locales en archivos sin tocar commits ni historial.
