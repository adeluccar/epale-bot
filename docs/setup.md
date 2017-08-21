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
