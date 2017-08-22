## Manual de uso para Git  

Antes de comenzar primero debemos realizar la instalación de git para eso te dejamos un link con los pasos para realizar las instalaciones en los diferentes sistemas operativos:
https://www.hostinger.es/tutoriales/instalar-git-en-distintos-sistemas-operativos.

### Subir un proyecto a GitHub usando Git:
1. Debemos estar situados en el directorio donde se encuentran los archivos que se deseen subir, Estando en el directorio debemos crear un repositorio local para ello emitimos el siguiente comando en nuestra terminal: `git init`

2. El siguiente paso es agregar lo que hemos hecho al repositorio local con el comando: `git add <nombre del archivo.extension>` para agregar un archivo especifico o `git add --all` para agregar todo el directorio.

3. Luego demos subir los cambios a nuestro repositorio en GitHub con el comando: `git commit –m 'mensaje que se quiera agregar'` con este comando agregaremos a GitHub lo que en el paso anterior subimos al repo local. usando el `"-m"` seguido de un mensaje que debe estar entre comillas, este mensaje es importante para saber cuáles son los cambios hechos en un archivo o una breve descripción de lo que se realizó antes del commit.

Nota: el –m se puede omitir si no se quiere enviar ningún mensaje junto al commit pero es una buena práctica enviar el mensaje para tener una buena comunicación entre equipo de trabajo.

4. Colocamos el link del repositorio remoto (el cual conseguimos en la página de github) con el comando: `git remote add origin <link>`

5. Por último, hacemos el push a GitHub escribiendo: `git push -u origin master` donde `"origin"` es alias y `"master"` es el Branch de origen donde se está trabajando.

### Como hacer el fork de un proyecto:

1. Has el fork en la página para que se agregue el repositorio a tu perfil.

2. Luego debemos clonar el repositorio en local emitimos el comando: `git clone <link>` donde link es la dirección tu repositorio, esto creara una carpeta en el directorio donde nos encontremos con todos los archivos del repositorio.

3. Entramos en el directorio donde está la carpeta creada.

4. Luego conectamos con el repositorio original `git remote add upstream <link>` este link es el del repositorio donde hiciste el fork (no el que está en tu cuenta si no al que le hiciste el fork) 

5. De aquí en adelante después de hacer los cambios que quieras debes subir los archivos al repositorio local y luego al repositorio remoto (realizar los mismo pasos de la sección como subir un proyecto a GitHub usando git desde el paso 2 en adelante).
