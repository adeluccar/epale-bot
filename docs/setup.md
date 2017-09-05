## Tips de instalación en varias plataformas

### Windows
1. Ir a [Pagina oficial de Node.js Foundation](https://nodejs.org/es/).
2. Descargar el instalador LTS de acuerdo a tu sistema operativo.
3. Ejecutar y seguir los pasos del instalador(con las opciones por defecto).

### Linux

Este metodo de instalacion es mediante gestores de paquetes.
Como queremos la version LTS, realizaremos los siguientes pasos

#### Distros de Linux basadas en Debian y Ubuntu


```bash
> curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
> sudo apt-get install -y nodejs
```

#### Arch Linux


```bash
> pacman -S nodejs npm
```

Con esto ya tendremos node y npm. Para verificar realizamos lo siguiente:

```bash
> node -v
v6.11.2
> npm -v
3.10.10
```

#### IMPORTANTE

En caso de que `npm -v` les arroje otra version, pueden cambiarla haciendo

```bash
> npm install -g npm@3.10.10
... si esto les da error por falta de permisos
... ejecutenlo como sudo (en debian/ubuntu)
> npm -v
3.10.10
```

Bien, ya tenemos instalado node.js y npm en nuestra máquina. Cualquier
inconveniente, visitar [esta pagina](https://nodejs.org/es/download/package-manager/)

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
