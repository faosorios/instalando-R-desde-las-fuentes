# Instalando R en linux desde las fuentes

Esta guia permite hacer la instalacion de R para el desarrollo de paquetes. Asumiremos que disponemos de un sistema Linux basado en Debian (como Ubuntu y sus derivados). Un enfoque alternativo es instalar `r-base-dev` usando, por ejemplo, el [Gestor de paquetes Synaptic](https://github.com/mvo5/synaptic).

## Instalando los requerimientos

Instalaremos las herramientas necesarias para compilar R desde las fuentes usando `apt`. En la terminal, ingresar: 

```bash
sudo apt install bzip2-doc gfortran gfortran-13 gfortran-13-x86-64-linux-gnu gfortran-x86-64-linux-gnu icu-devtools libblas-dev libbz2-dev libgfortran-13-dev libicu-dev libjpeg-dev libjpeg-turbo8-dev libjpeg8-dev liblapack-dev liblzma-dev libncurses-dev libpcre2-dev libpng-dev libpng-tools libreadline-dev zlib1g-dev
```
