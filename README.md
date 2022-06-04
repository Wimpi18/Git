# CLASE 1
## Repositorio
Es todo proyecto que tiene un seguimiento por Git.
## COMANDO: git init
Comando para inicializar Git en un directorio.
## COMANDO: git add
Indica a Git que quieres incluir actualizaciones en un archivo/directorio concreto en la próxima confirmación.
## COMANDO: git commit
Comando para el generar un registro de un cambio. [Tipo commmit: descripción de 40 caracteres máximo]
1. git commit nomArchivo
2. git commit -m "Descrp"
3. git commit nomArchivo -m "Descrp" 
## COMANDO: git log
Comando para ver el historial de cambios.
## Markdown
Es la carta de presentación de un proyecto.

# CLASE 2
## COMANDO: git branch 
Devuelve todas las ramas existentes.
## COMANDO: git branch nomRama
Crea la rama a partir de la rama padre, los cambios que ocurren en una rama no afectan a otras hasta utilizar un merge.
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

<center><img src="Ramas.png"></center>

## Fast forward
Una rama se adhiere a la rama padre, la operación contraria sería que se crea una nueva rama como combinación de 2 ramas. 
## COMANDO: --no--ff
## --ours y --theirs
## github repositorio en la nube
## pull request
Petición para hacer cambio en la rama main.

# OTRAS FUENTES
## Flujo de trabajo
1. Computador.- Trabajo realizado en los distintos archivos de un proyecto.
2. Stage.- Con git add seleccionamos los archivos que pasamos a la etapa stage para poder verificar los cambios de un archivo.
3. Commit.- Con git commit comprometemos cambios de un archivo para poder pasarlos al repositorio.
4. Server.- Con git push pasamos los cambios seleccionados a un servidor

## Otros comandos
1. Quitar un elemento que fue añadido al stage: **git restore --stager nomArchivo**