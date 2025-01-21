# Para crear ramas en git:

Para verificar ramas `git branch` y el status `git status`

Para crear una nueva rama en Git, puedes usar el comando git switch -c <nombre_de_la_rama> Si deseas clonar la rama **main** y llamar a esta copia **dev**, primero debes asegurarte de estar en la rama main, y luego ejecutar el siguiente comando:

`git switch -c dev`

Este comando creará una nueva rama llamada dev basada en la rama actual, que debería ser main si no has cambiado de rama. Después de ejecutar este comando, estarás en la nueva rama dev.

Si quisiéramos borrar dev sería:

`git branch -b dev`

# Para subir una rama a github

1. Asegúrate de estar en la rama que deseas subir. Por ejemplo, si deseas subir la rama dev, puedes posicionarte primero en la rama en cuestión:
   `git switch dev`

2. Una vez que estés en la rama que deseas subir, en nuestro caso la rama dev, utiliza el siguiente comando para subir la rama al repositorio remoto (en este caso, GitHub):
   `git push --set-upstream origin dev`

Donde origin es el nombre del control remoto (el repositorio en GitHub) y dev es el nombre de la rama que deseas subir.

Una vez ejecutado este comando, la nueva rama debería estar disponible en tu repositorio en GitHub. Puedes verificarlo visitando tu repositorio en la interfaz web de GitHub.

# Para fusionar o "mergear" ramas

Para fusionar cambios de una rama (por ejemplo, la rama dev) con otra (la rama main), primero asegúrate de estar en la rama de destino (main). Puedes hacerlo utilizando el comando git checkout main. Luego, ejecuta el comando git merge seguido del nombre de la rama desde la cual deseas fusionar los cambios (dev en este caso).

1. Asegúrate de estar en la rama **main**:

`git switch main`

2. Fusiona los cambios de la rama **dev** en la rama **main**:

`git merge dev`

Este comando fusionará los cambios de la rama dev en la rama main. Si hay conflictos durante la fusión, Git te pedirá que los resuelvas manualmente. Una vez que los conflictos se resuelvan (si los hay), los cambios de la rama dev estarán integrados en la rama main.

Cuando haya conflictos y no queramos aceptar el mergeo, ponemos este comando

`git merge --abort`
