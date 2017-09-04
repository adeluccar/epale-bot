## ¿Como contribuir?

[Video Paso a Paso](https://www.youtube.com/watch?v=BJStp9ApkXs)

### Si es tu primera vez

1. Haz un fork a este repositorio
2. En tu sistema local, haz un `git clone git@github.com:tu-usuario/epale-bot.git` donde usuario es tu usuario en github si ya posees una llave SSH. O clona el repositorio mediante HTTPS ejecutando el comando `git clone https://github.com/tu-usuario/epale-bot.git`
3. Incluye el remoto original (upstream) del cual hiciste el fork:  `git remote add upstream git@github.com:adeluccar/epale-bot.git`. También puedes hacer esto mediante HTTPS ejecutando el comando `git remote add upstream https://github.com/adeluccar/epale-bot.git`

### Cuando comienza el día

Es buena idea hacer un `npm install` siempre que fusiones cambios nuevos del repositorio (recuerda que el repositorio indica lo que 'debe haber' mas no lo instala por ti).

`git checkout master`  
`git fetch upstream`  
`git rebase upstream/master`  
`npm install`
`git checkout tu-rama`  
`git rebase master`  

#### Explicación de los comandos

`git checkout master`  
Cambia la rama actual en el repositorio local a la rama master (maestra).

`git fetch upstream`  
Baja la rama maestra del repositorio remoto designado como upstream.  

`git rebase upstream/master`  
Reproduce los cambios existentes en el master del repositorio remoto upstream sobre el master del repositorio local.  
Recuerda que el `git checkout master` anterior nos coloca en dicho master a nivel local.

### Seguir el trabajo en una rama

`git checkout tu-rama`  
Cambia a la rama designada con tu-rama (por ejemplo, una rama en la que estas trabajando).

`git rebase master`  
Reproduce los cambios existentes en el master local en la rama actual. Si no hay conflictos, ya tienes tanto el master como la rama actualizados con los últimos cambios del repositorio autoritario (en este caso, upstream).

### Comenzar el trabajo en un rama nueva

`git checkout -b tu-nombre-de-la-rama`  
Crea una nueva rama y luego cambia git a esa rama.

### Mientras trabajas

`git add file-name`  
Añade los cambios en el archivo file-name al area de ensayo. Puedes continuar añadiendo otros archivos que se agrupen logicamente con ese commit que quieres realizar.

`git add -A` o tambien `git add --all`
Si usamos este parametro agrega todos los archivos, es una forma rapida de trabajar, pero usala con cuidado.

`git commit -m "Mensaje del Commit"`  
Confirma e inserta los cambios existentes en el area de ensayo junto al mensaje, el autor, correo, fecha de inserción y otros datos. Repite este proceso cuantas veces sea necesario.

### Subir el trabajo realizado (la rama) al repositorio remoto personal (origin)

Es buena idea repetir los pasos para actualizar la rama con el master (comienzo del día) antes de comenzar el proceso de preparar el pull request.

Luego, hay que hacer un squash de todos los commits para dejar la rama con un solo commit. El efecto secundario (positivo) de esto es que cuando se hacemos la fusión de la rama hacia el master, entra un solo commit. Eso mantiene la historia bastante limpia.

[Video paso a paso del squash de un rama](https://www.youtube.com/watch?v=lRCBHRbm-to)

`git reset --hard HEAD~X`  
Donde X es el numero de commits entre el primero y ultimo de la rama.
Es decir, si has hecho dos commits, X sería 2.

`git merge --squash HEAD@{1}`  
HEAD@{1} es una sintax especial para el commit donde estaba HEAD antes del reset anterior. Basicamente estamos diciendo, haz un merge desde donde estoy hasta donde empezó el reset.

`git commit -v`  
Haz el commit con todos los cambios. La ventaja de este metodo es que los commits previos apareceran en la descripción de este commit final.

`git push -u origin tu-rama`  
Sube los cambios existentes en la rama branch-name al repo remoto personal en Github. Se utiliza el switch `-u` la primera vez que se hace, para que subidas posteriores de esa rama puedan realizarse con un simple `git push`.

Luego, en la interfaz de github, ejecutas una pull-request desde esa rama tu-rama hacia el master en el repositorio autoritario (el upstream). Una vez que la rama es incluida en el master del repo autoritario, puede borrarse a nivel local, pues los cambios serán actualizados en el master local a través del proceso al inicio del día.
