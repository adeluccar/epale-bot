## Tips de instalación en varias plataformas

### Windows
1. Ir a [Pagina oficial de Node.js Foundation](https://nodejs.org/es/).
2. Descargar el instalador LTS de acuerdo a tu sistema operativo.
3. Ejecutar y seguir los pasos del instalador(con las opciones por defecto).

### Linux
1. Vamos a [Pagina oficial de Node.js](https://nodejs.org/es/) y hacemos click en "INSTALL". Descargaremos un .tar.gz.

2. Descomprimimos el archivo y veremos una carpeta como la siguiente:
`node-v0.10.13`

3. Entramos dentro de la carpeta:

```bash
cd node-v0.10.13/
```

4. Ejecutamos los siguientes comandos:

```bash
./configure
make
sudo make install
```

5. Comprobamos que se ha instalado correctamente:

```bash
node --version
```

6. Instalamos npm:

```bash
wget https://npmjs.org/install.sh --no-check-certificate; sudo sh install.sh
```

7. Comprobamos que se ha instalado correctamente:

```bash
npm --version
```

Bien, ya tenemos instalado node.js y npm en nuestra máquina.

### Mac
La mejor forma de instalar node en Mac es usando un gestor de ambientes node (en este caso, nodenv). Esta forma de instalar permite utilizar una versión de node especifica para cada proyecto.

Para ello vamos a utilizar Homebrew, el gestor de paquetes por excelencia en la Mac.

npm no es necesario instalarlo pues viene junto con node.

1. Instala [Homebrew](https://brew.sh/index_es.html) (si no lo tienes):

    ```bash
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

1. Actualiza Homebrew (no es necesario si acabas de instalarlo):

    ```bash
    brew update
    ```

1. Instala [nodenv](https://github.com/nodenv/nodenv):

    ```bash
    brew install nodenv
    ```

1. Inicializa nodenv (tienes que hacer esto una sola vez - cuando instalas nodenv):

    ```bash
    nodenv init
    ```

1. Instala node (6.11.2 en este ejemplo):

    ```bash
    nodenv install 6.11.2
    ```

1. Configura nodenv (hazlo siempre despues de instalar un node nuevo o la instalación de algún paquete node global):

    ```bash
    nodenv rehash
    ```
