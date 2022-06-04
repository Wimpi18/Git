# CLASE 1
## Repositorio
Es todo proyecto que tiene un seguimiento por Git.
## COMANDO: git init
Comando para inicializar Git en un directorio.
## COMANDO: git add
Indica a Git que quieres incluir actualizaciones en un archivo/directorio concreto en la próxima confirmación.
## COMANDO: git commit
Comando para el generar un registro de un cambio. [Tipo commmit: descripción de 40 caracteres máximo]
<<<<<<< HEAD
1. git commit nomArchivo
2. git commit -m "Descrp"
3. git commit nomArchivo -m "Descrp" 
=======
1. git commit file
2. git commit -m "Descrp"
3. git commit file -m "Descrp" 
>>>>>>> Pruebas
## COMANDO: git log
Comando para ver el historial de cambios.
## Markdown
Es la carta de presentación de un proyecto.

# CLASE 2
## COMANDO: git branch 
Devuelve todas las ramas existentes.
## COMANDO: git branch nomRama
<<<<<<< HEAD
Crea la rama a partir de la rama padre, los cambios que ocurren en una rama no afectan a otras hasta utilizar un merge.
=======
Crea la rama a partir de la rama padre (en la que nos encontramos), los cambios que ocurren en una rama no afectan a otras hasta utilizar un merge.
>>>>>>> Pruebas
## COMANDO: git checkout nomRama
Nos permite navegar entre las ramas.
## COMANDO: git merge nomRama
Obtiene los cambios de la rama indicada en el comando y los actualiza en la rama en la que nos encontramos.
## COMANDO: git config
1. --global user.name "NombreUsuario"
2. --global user.email "Email"
## File explorer y las ramas
Los archivos y sus cambios se van a mostrar de acuerdo a la rama en la que nos encontremos.
## Conflictos
Dos ramas modifican el mismo archivo, entonces Git no sabes que version del archivo implementar.

# CLASE 3
## Ramas
1. Main/Master.- Es la rama principal.
2. Otras ramas.- Son bifurcaciones de la rama principal, son copias del proyecto pero separada para poder ser trabajadas.
<p></p>

<<<<<<< HEAD
<center><img src="Ramas.png"></center>

## Fast forward
Una rama se adhiere a la rama padre, la operación contraria sería que se crea una nueva rama como combinación de 2 ramas. 
## COMANDO: --no--ff
## --ours y --theirs
## github repositorio en la nube
## pull request
Petición para hacer cambio en la rama main.
=======

<center><img src="Ramas.png"></center>

## Fast forward
Una rama A se fusiona a la rama B incluyendo los commits **(git merge rama)**.
## No fast forward
Una rama A se fusiona a la rama B integrados los cambios de A en B, pero con la diferencia de que la visualización de la rama A queda separada de la rama B **(git merge rama --no-ff)**.
*Tanto si usamos Fast forward como No fast forward solo cambiara la forma en la que visualizaremos el histórico de nuestro repositorio*
## COMANDO: git merge --ours rama
Los cambios de la rama A se conservan mientras no hayan conflictos con la rama B, en caso de conflicto se prioriza lo que está en la rama B.
## COMANDO: git merge --theirs rama
Los cambios de la rama A se conservan mientras no hayan conflictos con la rama B, en caso de conflicto se prioriza lo que está en la rama A.
## pull request
Petición para hacer cambios en la rama main.

# CLASE 4
## GitHub
Es un repositorio en la nube, existen otros como GitLab o Bitbucket.
## COMANDO: git remote -v
Nos permite ver el repositorio remoto al que estamos conectados.
## COMANDO: git remote add origin link
Obtenemos acceso al repositorio en la nube. <p>
Origin es el fuente/origen del repositorio en el que trabajaremo en GitHub.
## COMANDO: git push 
Subimos una rama al repositorio origin.
1. **git push -u origin main**
## COMANDO: git clone link
Comando para clonar la rama principal de un repositorio pero con **git checkout rama** podemos ingresar a las otras ramas existentes del repositorio.
## COMANDO: git pull
Comando para agregar una rama a nuestro repositorio local, luego debemos escribir ***git checkout rama*** para ingresar a la rama y así poder visibilizarla con el **git branch**.
1. **git pull origin nomRama**
>>>>>>> Pruebas

# OTRAS FUENTES
## Flujo de trabajo
1. Computador.- Trabajo realizado en los distintos archivos de un proyecto.
2. Stage.- Con git add seleccionamos los archivos que pasamos a la etapa stage para poder verificar los cambios de un archivo.
3. Commit.- Con git commit comprometemos cambios de un archivo para poder pasarlos al repositorio.
4. Server.- Con git push pasamos los cambios seleccionados a un servidor

## Otros comandos
<<<<<<< HEAD
1. Quitar un elemento que fue añadido al stage: **git restore --stager nomArchivo**
=======
1. Quitar un elemento que fue añadido al stage: **git restore --staged file**
2. Recuperar un archivo eliminado: **git restore file**
3. 
>>>>>>> Pruebas
