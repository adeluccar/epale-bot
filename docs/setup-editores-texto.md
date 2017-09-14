# Manual de instalación de ESLint.

## Sublime Text 3

### Instalación en Windows.

Para poder utilizar la herramienta ESLinter con el editor de texto Sublime Text 3 es necesario seguir los siguientes pasos:

1. Instalar Sublime Text 3 si aún no lo has hecho. Descárgalo desde la página oficial haciendo clic [aquí](https://www.sublimetext.com/).
1. Instalar el Package Control que es un gestor de paquetes y plugins para Sublime Text 3 y permite la fácil instalación de funcionalidades extras. Puedes seguir las instrucciones de instalación haciendo clic [aquí](https://packagecontrol.io/installation).

### Instalación SublimeLinter.

1. Una vez instalado el Package Control, debemos abrirlo para buscar el plugin SublimeLinter en el repositorio de paquetes. Los pasos son los siguientes:
1. Abrir el menu `Preferences>PackageControl`
1. En la lista desplegable ingresar la palabra `Install` y seleccionar la primera opción que dice `Package Control: Install Package`. Quizás haya una pausa mientras el Package Control encuentra los paquetes disponibles.
1. En la pantalla mostrada a continuación ingresar la palabra `linter` y seleccionar la opción `SublimeLinter`. Después de unos segundos el plugin de SublimeLinter estará instalado en el editor de texto.

### Instalación del plugin ESLinter.

1. A continuación se debe instalar el plugin `eslint` para que se muestren los errores en el Sublime Text.
1. Se deben realizar los mismos pasos 1 y 2 de la instalación del `SublimeLinter`
1. Una vez esté disponible la pantalla de búsquedas de paquetes, ingresar la palabra `eslint` y luego seleccionar la opción `SublimeLinter-contrib-eslint`.
1. Después de unos segundos el plugin `SublimeLinter-eslint` estará instalado en el editor de código.

Se recomienda en este punto **reiniciar el Sublime Text 3**.

Al abrir la carpeta raíz del proyecto desde Sublime Text 3 (después de haber ejecutado el `npm install` y obtener todas las dependencias necesarias), el plugin debería cargar el archivo de configuración `.eslintrc.json` automáticamente.

Al abrir un archivo Javascript se mostrarán los posibles errores que tuviera el mismo dependiendo de la configuración contenida en el archivo `.eslintrc.json`.
