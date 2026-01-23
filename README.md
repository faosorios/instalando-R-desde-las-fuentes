# Instalando R en linux desde las fuentes

Esta guia permite hacer la instalacion de R para el desarrollo de paquetes. Asumiremos que disponemos de un sistema Linux basado en Debian (como Ubuntu y sus derivados). Un enfoque alternativo es instalar `r-base-dev` usando, por ejemplo, el [Gestor de paquetes Synaptic](https://github.com/mvo5/synaptic).

## Instalando requerimientos

Instalaremos las herramientas necesarias para compilar R desde las fuentes usando `apt`. En la terminal, ingresar: 
```bash
sudo apt install binutils binutils-common binutils-x86-64-linux-gnu build-essential bzip2-doc dpkg-dev fakeroot g++ g++-13 gcc gcc-13 gfortran gfortran-x86-64-linux-gnu gfortran-13 gfortran-13-x86-64-linux-gnu icu-devtools libasan8 libatomic1 libbinutils libblas-dev libbz2-dev libc-dev-bin libc6-dev libcc1-0 libcrypt-dev libctf-nobfd0 libctf0 libcurl4-openssl-dev libfakeroot libgcc-13-dev libgfortran-13-dev libicu-dev libitm1 libjpeg-dev libjpeg-turbo8-dev libjpeg8-dev liblapack-dev liblsan0 liblzma-dev libncurses-dev libpcre2-dev libpng-dev libpng-tools libreadline-dev libstdc++-13-dev make zlib1g-dev
```

Es recomendable instalar las bibliotecas para desarrollo asociadas a Xorg, asi como el entorno de ejecucion de Java (JRE) y algunas fuentes
```bash
sudo apt install xorg-dev libtiff-dev libcairo2-dev default-jre openjdk-21-jdk openjdk-21-jre
sudo apt install t1-xfree86-nonfree ttf-xfree86-nonfree ttf-xfree86-nonfree-syriac xfonts-75dpi xfonts-100dpi
```

Si se desea usar [Tcl-Tk](https://www.tcl-lang.org/) con R, instalar las siguientes bibliotecas:
```bash
sudo apt install tcl-dev tk-dev libtcl-dev
```

## Descargando e instalando R

Las [fuentes](https://cran.r-project.org/sources.html) oficiales de R pueden ser encontradas en [CRAN](https://cran.r-project.org/). Si se desea desarrollar paquetes para R es recomendable descargar la version de *desarrollo*. Una vez que se ha descargado, por ejemplo, el fichero `R-devel.tar.gz`. En la terminal ir al directorio donde se encuentra el archivo (para fines de este ejemplo, asumiremos que este archivo se encuentra en el directorio `Descargas`), e ingresar los siguientes comandos:
```bash
sudo tar xvfz R-devel.tar.gz
sudo cd R-devel
sudo ./configure --enable-R-shlib --with-tcltk
sudo make
sudo make install
```
una vez que este proceso termina (el cual puede demorar bastante), en la propia terminal usar el comando `R`. Usted deberia ver algo como lo siguiente:

![R terminal](/images/R-term.jpg)
