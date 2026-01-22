# Instalando R en linux desde las fuentes

Esta guia permite hacer la instalacion de R para el desarrollo de paquetes. Asumiremos que disponemos de un sistema Linux basado en Debian (como Ubuntu y sus derivados). Un enfoque alternativo es instalar `r-base-dev` usando, por ejemplo, el [Gestor de paquetes Synaptic](https://github.com/mvo5/synaptic).

## Instalando los requerimientos

Instalaremos las herramientas necesarias para compilar R desde las fuentes usando `apt`. En la terminal, ingresar: 
```bash
sudo apt install binutils binutils-common binutils-x86-64-linux-gnu build-essential bzip2-doc dpkg-dev fakeroot g++ g++-13 gcc gcc-13 gfortran gfortran-x86-64-linux-gnu gfortran-13 gfortran-13-x86-64-linux-gnu icu-devtools libasan8 libatomic1 libbinutils libblas-dev libbz2-dev libc-dev-bin libc6-dev libcc1-0 libcrypt-dev libctf-nobfd0 libctf0 libcurl4-openssl-dev libfakeroot libgcc-13-dev libgfortran-13-dev libicu-dev libitm1 libjpeg-dev libjpeg-turbo8-dev libjpeg8-dev liblapack-dev liblsan0 liblzma-dev libncurses-dev libpcre2-dev libpng-dev libpng-tools libreadline-dev libstdc++-13-dev make zlib1g-dev
```

Es recomendable instalar las bibliotecas para desarrollo asociadas a Xorg, asi como el entorno de ejecucion de Java (JRE) y algunas fuentes
```bash
sudo apt install xorg-dev libtiff-dev libcairo2-dev default-jre openjdk-21-jdk openjdk-21-jre
sudo apt install t1-xfree-nonfree ttf-xfree86-nonfree ttf-xfree86-nonfree-syriac xfonts-75dpi xfonts-100dpi
```
