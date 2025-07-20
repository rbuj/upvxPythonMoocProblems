# 1. Preparación del entorno

Para ejecutar los *notebooks* dentro de VS Code se tiene que:

* Instalar [VS Code](https://code.visualstudio.com/),
* Instalar la extensión [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) para VS Code,
* Crear un entorno virtual con Conda

Primero se tiene que instalar [VS Code](https://code.visualstudio.com/) y la [extensión de Python para VS Code](https://marketplace.visualstudio.com/items?itemName=ms-python.python).

> [!TIP]
> Para lanzar VS Code (por ejemplo `code .`) desde un terminal, añadiremos la siguiente línea al archivo `~/.bash_profile`:
>
> `alias code='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'`

A continuación detallaremos los pasos para crear un entorno virtual con `Conda`.

## 1.1. Instalación de miniconda

En macOS:

```sh
brew install --cask miniconda
conda init
conda config --set auto_activate_base False
source ~/.bash_profile
```

Después hay que aceptar los términos del servicio de los canales de instalación:

```sh
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r
```

## 1.2. Creación del entorno virtual con conda

Para crear entornos locales en VS Code mediante Conda, abrimos `Command Palette` (⇧⌘P), buscamos y seleccionamos el comando `Python: Create Environment`.

![](./img/create_environment.avif)

Se muestra una lista con los tipos de entornos virtuales: `Venv` o `Conda`. Seleccionamos `Conda`.

![](./img/create_environment_dropdown.avif)

El comando muestra una lista con las versiones de Python que se pueden utilizar en el proyecto. Seleccionamos Python 3.11:

![](./img/conda_environment_python_versions.avif)

Se instalaran automáticamente las bibliotecas definidas en el archivo [environment.yml](environment.yml).
