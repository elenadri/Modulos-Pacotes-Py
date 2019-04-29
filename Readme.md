**crear un paquete**

Para crear un paquete lo que tenemos que hacer es crear un fichero especial init vacío en el directorio donde tengamos todos los módulos que queremos agrupar. De esta forma cuando Python recorra este directorio será capaz de interpretar una jerarquía de módulos:
`ifsul_tap/`
    `__init__.py`
    `modulo.py`

**Distribución**
Para crear un paquete distribuible tenemos que crear un fichero setup.py fuera de la raíz, indicando una información básica, de la siguiente forma:
`setup.py`
`ifsul_tap/`
    `__init__.py`
    `modulo.py`

`setup.py`

`from setuptools import setup`

`setup(`
    `name="ifsul_tap",`

    `version="0.1",`

    `description="Este es un jemplo",`

    `author="Elena Adriana Moura Bueno",`

    `author_email="elenaadrianamourabueno@gmail.com",`

    `packages=['ifsul_tap']`
`)`

Una vez hemos definido el distribuible con su información básica, incluyendo los paquetes y subpaquetes que lo forman, así como los posibles scripts, debemos crearlo. Para hacerlo utilizaremos el siguiente comando allí donde tenemos el setup.py:


`python setup.py sdist`

Para instalar un paquete en Python, y finalmente hacer que éste se pueda utilizar desde cualquier lugar lo haremos de la siguiente forma, desde el directorio donde tenemos el paquete comprimido:

>fichero zip en Windows o tar.gz si estamos en Linux. 

`pip install ifsul_tap-0.1.tar.gz`


Ahora, si utilizamos el comando pip3 list, podremos consultar todos los paquetes instalados en nuestro Python, y podremos ver también el nuestro. Si aparece correctamente podremos utilizar nuestro paquete desde cualquier script, pues se encuentra instalado dentro de Python.

**como ejecutar**
en termilar : from ifsul_tap import *

Finalmente utilizando el comando pip uninstall para desinstalarlo:
`pip uninstall ifsul_tap`

