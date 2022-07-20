# CLASE 1
## Repositorio
Es todo proyecto que tiene un seguimiento por Git.
## COMANDO: git init
Comando para inicializar Git en un directorio.
## COMANDO: git add
Indica a Git que quieres incluir actualizaciones en un archivo/directorio concreto en la próxima confirmación.
## COMANDO: git commit
Comando para el generar un registro de un cambio. [Tipo commmit: descripción de 40 caracteres máximo]
1. git commit `<file>`
2. git commit -m "`<descripción>`"
3. git commit file -m "`<descripción>`"
## COMANDO: git log
Comando para ver el historial de cambios.
1. Muestra los SHA en una sola línea: **git log --oneline**
2. Muestra todas las ramas: **git log --graph**
## README
Es la carta de presentación de un proyecto, está elaborado en Markdown.

# CLASE 2
## COMANDO: git branch 
Devuelve todas las ramas existentes.
## COMANDO: git branch nomRama
Crea la rama a partir de la rama padre (en la que nos encontramos), los cambios que ocurren en una rama no afectan a otras hasta utilizar un merge.
## COMANDO: git checkout nomRama
Nos permite navegar entre las ramas.
## COMANDO: git merge nomRama
Obtiene los cambios de la rama indicada en el comando y los actualiza en la rama en la que nos encontramos.
## COMANDO: git config
1. --global user.name "`<nombreUsuario>`"
2. --global user.email "`<email>`"
## File explorer y las ramas
Los archivos y sus cambios se van a mostrar de acuerdo a la rama en la que nos encontremos.
## Conflictos
Dos ramas modifican el mismo archivo, entonces Git no sabes que version del archivo implementar.

# CLASE 3
## Ramas
1. Main/Master.- Es la rama principal.
2. Otras ramas.- Son bifurcaciones de la rama principal, son copias del proyecto pero separada para poder ser trabajadas.
<p></p>

<center><img src="Ramas.png"></center>

## Fast forward
Una rama A se fusiona a la rama B incluyendo los commits **(git merge `<rama>`)**.
## No fast forward
Una rama A se fusiona a la rama B integrados los cambios de A en B, pero con la diferencia de que la visualización de la rama A queda separada de la rama B **(git merge `<rama>` --no-ff)**.
*Tanto si usamos Fast forward como No fast forward solo cambiara la forma en la que visualizaremos el histórico de nuestro repositorio*
## COMANDO: git merge -s ours `<rama>`
Los cambios de la rama A se conservan mientras no hayan conflictos con la rama B, en caso de conflicto se prioriza lo que está en la rama B.
## COMANDO: git merge -s theirs `<rama>`
Los cambios de la rama A se conservan mientras no hayan conflictos con la rama B, en caso de conflicto se prioriza lo que está en la rama A.
## pull request
Petición para hacer cambios en la rama main.

# CLASE 4
## GitHub
Es un repositorio en la nube, existen otros como GitLab o Bitbucket.
## COMANDO: git remote -v
Nos permite ver el repositorio remoto al que estamos conectados.
## COMANDO: git remote add origin `<link>`
Obtenemos acceso al repositorio en la nube. <br>
Origin es el fuente/origen del repositorio en el que trabajaremo en GitHub.
## COMANDO: git push 
Subimos una rama al repositorio origin.
1. **git push -u origin main**
## COMANDO: git clone link
Comando para clonar la rama principal de un repositorio pero con **git checkout rama** podemos ingresar a las otras ramas existentes del repositorio.
## COMANDO: git pull
Comando para agregar una rama a nuestro repositorio local, luego debemos escribir ***git checkout `<rama>`*** para ingresar a la rama y así poder visibilizarla con el **git branch**.
1. **git pull origin `<rama>`**

# CLASE 5
## Flujo de Trabajo en equipos
Conjunto de reglas a las cuales se rige un repositorio.
## Basic Workflow
Usualmente se usa individualmente en un proyecto pequeño.
## Feature Branch Workflow
Suele ser usado en trabajos en equipo para proyectos pequeños. 
## Gitflow Workflow
Se utilizan en trabajos en equipo para proyectos más grandes y extensos.
1. Main.- Es la versión del proyecto, en esta rama se añaden los proyectos ya finalizados y que hayan pasado por el release o hotfix en algunos casos.
2. Hotfix.- Es un parcheo o arreglo inmediato del proyecto. De aquí nacen las versiones 1.2, 2.1.2, etc
3. Release.- Últimos detalles como revisiones, documentación concisa y testeo.
4. Develop.- Desarrollo y documentación de código.
5. Feature.- Ramas de desarrollo pertenecientes a cada integrante del equipo. <br>
**De la rama Main al Develop son únicas**
## Forking Workflow
Consiste en clonar el repositorio y emplear algunos de los anteriores Workflow

# OTRAS FUENTES
## Flujo de trabajo en GIT
1. Computador.- Trabajo realizado en los distintos archivos de un proyecto.
2. Stage.- Con git add seleccionamos los archivos que pasamos a la etapa stage para poder verificar los cambios de un archivo.
3. Commit.- Con git commit comprometemos cambios de un archivo para poder pasarlos al repositorio.
4. Server.- Con git push pasamos los cambios seleccionados a un servidor

## Otros comandos
1. Quitar un elemento que fue añadido al stage: **git restore --staged file**
2. Recuperar un archivo eliminado: **git restore file**
3. Nos permite ver todos los repositorios remotos: **git remote**
4. Deshacer los cambios que hemos hecho: **git revert `<idRama>`**
5. Para ver los cambios del archivo: **git show `<archivo>`**

## Links interesantes de Platzi
1. Flujo de trabajo profesional y comandos oscuros: https://platzi.com/blog/flujo-de-trabajo-y-comandos-oscuros-de-git/
2. Todos los comandos del curso: https://platzi.com/tutoriales/1557-git-github/4037-todos-los-comandos-del-curso-v20/
3. Resumen de comandos: https://platzi.com/tutoriales/1557-git-github/333-resumen-de-comandos/ 