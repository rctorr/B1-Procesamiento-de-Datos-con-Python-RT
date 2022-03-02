
## Sesión 01: Fundamentos de Python

### 1. Objetivos

1. Asignar variables, operadores matemáticos y tipos de datos.
2. Realizar interpolación de Strings.
3. Realizar comparaciones y estructuras de control de flujo.

### 2. Contenido

<ins>Revisión de Software</ins>

Asegurarse de haber realizado la instalación de Miniconda Python de forma local en tú equipo, en caso contrario Miniconda puede ser descargado desde [aquí](https://docs.conda.io/en/latest/miniconda.html), sólo descarga el adecuado para tu sistema operativos (Linux, Mac o Windows) y el que corresponda a la versión más reciente de Python (3.9 al momento de escribir estas notas).

Para realizar la instalación a continuación tienes acceso a las guías para cada sistema operativo:
- [Guía para instalación en Linux](https://conda.io/projects/conda/en/latest/user-guide/install/linux.html)
- [Guía para instalación en Mac](https://drive.google.com/file/d/1piNWy2urb_b9lkCaax9WwIs551ngho0v/view?usp=sharing)
- [Guía para instalación en Windows](https://drive.google.com/file/d/1YdOj9SSxw5FQOGcShM8eSO3LQlPCFP4W/view?usp=sharing)

También es necesario que hayas realizado el clonado del repositorio de GitHub en tú equipo, de preferencia en una carpeta de facil acceso como puede ser la del **Escritorio**.

Si no cuentas con el link al repo es buen momento para solicitarlo.

En caso de que aún no hayas clonado el repo lo puedes hacer abriendo una **Terminal** (git-bash en Windows) y ejecutando los siguientes comandos:

```console
$ cd Desktop
Desktop $ git clone link-al-repo
...
...

Desktop $ cd TECP0013ADDAOL2103
Desktop/TECP0013ADDAOL2103 $
```
Y al final nos cambiamos a esta carpeta que será nuestra carpeta de trabajo.

---

<ins>Instalación y ejecución de Jupyter Lab</ins>

Para realizar la instalación de Jupyter Lab es necesario abrir una terminal llamada **Anaconda Prompt** en Windows o una **Terminal** para Linux o Mac.

Ya en la terminal se utiliza el comando `pip install jupyterlab` y un ejemplo del proceso de instalación se muestra a continuación:

```console
$ pip install jupyterlab
Collecting jupyterlab
  Using cached jupyterlab-3.0.16-py3-none-any.whl (8.2 MB)
Collecting tornado>=6.1.0
  Downloading tornado-6.1-cp38-cp38-manylinux2010_x86_64.whl (427 kB)
     |████████████████████████████████| 427 kB 544 kB/s 
Collecting jupyter-core
  Downloading jupyter_core-4.7.1-py3-none-any.whl (82 kB)
     |████████████████████████████████| 82 kB 397 kB/s 
Collecting jupyterlab-server~=2.3
  Using cached jupyterlab_server-2.6.0-py3-none-any.whl (55 kB)
Collecting packaging
  Downloading packaging-20.9-py2.py3-none-any.whl (40 kB)
     |████████████████████████████████| 40 kB 287 kB/s 
Collecting jupyter-server~=1.4
  Using cached jupyter_server-1.8.0-py3-none-any.whl (382 kB)
Collecting nbclassic~=0.2
  Using cached nbclassic-0.3.1-py3-none-any.whl (18 kB)
Collecting ipython
  Downloading ipython-7.24.1-py3-none-any.whl (785 kB)
     |████████████████████████████████| 785 kB 122 kB/s 
Collecting jinja2>=2.1
  Using cached Jinja2-3.0.1-py3-none-any.whl (133 kB)
Collecting traitlets
  Using cached traitlets-5.0.5-py3-none-any.whl (100 kB)
Collecting json5
  Using cached json5-0.9.5-py2.py3-none-any.whl (17 kB)
Collecting jsonschema>=3.0.1
  Using cached jsonschema-3.2.0-py2.py3-none-any.whl (56 kB)
Collecting requests
  Using cached requests-2.25.1-py2.py3-none-any.whl (61 kB)
Collecting babel
  Using cached Babel-2.9.1-py2.py3-none-any.whl (8.8 MB)
Collecting pyparsing>=2.0.2
  Using cached pyparsing-2.4.7-py2.py3-none-any.whl (67 kB)
Collecting pyzmq>=17
  Downloading pyzmq-22.1.0-cp38-cp38-manylinux2010_x86_64.whl (1.1 MB)
     |████████████████████████████████| 1.1 MB 234 kB/s 
Collecting nbformat
  Downloading nbformat-5.1.3-py3-none-any.whl (178 kB)
     |████████████████████████████████| 178 kB 435 kB/s 
Collecting prometheus-client
  Downloading prometheus_client-0.11.0-py2.py3-none-any.whl (56 kB)
     |████████████████████████████████| 56 kB 371 kB/s 
Collecting terminado>=0.8.3
  Downloading terminado-0.10.1-py3-none-any.whl (14 kB)
Collecting argon2-cffi
  Using cached argon2_cffi-20.1.0-cp35-abi3-manylinux1_x86_64.whl (97 kB)
Collecting Send2Trash
  Using cached Send2Trash-1.5.0-py3-none-any.whl (12 kB)
Collecting jupyter-client>=6.1.1
  Downloading jupyter_client-6.1.12-py3-none-any.whl (112 kB)
     |████████████████████████████████| 112 kB 630 kB/s 
Collecting nbconvert
  Downloading nbconvert-6.0.7-py3-none-any.whl (552 kB)
     |████████████████████████████████| 552 kB 141 kB/s 
Collecting anyio<4,>=3.1.0
  Using cached anyio-3.1.0-py3-none-any.whl (74 kB)
Collecting ipython-genutils
  Using cached ipython_genutils-0.2.0-py2.py3-none-any.whl (26 kB)
Collecting websocket-client
  Using cached websocket_client-1.1.0-py2.py3-none-any.whl (68 kB)
Collecting notebook<7
  Downloading notebook-6.4.0-py3-none-any.whl (9.5 MB)
     |████████████████████████████████| 9.5 MB 122 kB/s 
Collecting pexpect>4.3; sys_platform != "win32"
  Using cached pexpect-4.8.0-py2.py3-none-any.whl (59 kB)
Collecting prompt-toolkit!=3.0.0,!=3.0.1,<3.1.0,>=2.0.0
  Using cached prompt_toolkit-3.0.18-py3-none-any.whl (367 kB)
Collecting jedi>=0.16
  Using cached jedi-0.18.0-py2.py3-none-any.whl (1.4 MB)
Collecting backcall
  Using cached backcall-0.2.0-py2.py3-none-any.whl (11 kB)
Collecting matplotlib-inline
  Using cached matplotlib_inline-0.1.2-py3-none-any.whl (8.2 kB)
Collecting decorator
  Using cached decorator-5.0.9-py3-none-any.whl (8.9 kB)
Collecting pickleshare
  Using cached pickleshare-0.7.5-py2.py3-none-any.whl (6.9 kB)
Collecting pygments
  Using cached Pygments-2.9.0-py3-none-any.whl (1.0 MB)
Requirement already satisfied: setuptools>=18.5 in ./miniconda3/envs/temporal/lib/python3.8/site-packages (from ipython->jupyterlab) (47.3.1.post20200622)
Collecting MarkupSafe>=2.0
  Downloading MarkupSafe-2.0.1-cp38-cp38-manylinux2010_x86_64.whl (30 kB)
Collecting six>=1.11.0
  Using cached six-1.16.0-py2.py3-none-any.whl (11 kB)
Collecting attrs>=17.4.0
  Downloading attrs-21.2.0-py2.py3-none-any.whl (53 kB)
     |████████████████████████████████| 53 kB 1.1 MB/s 
Collecting pyrsistent>=0.14.0
  Downloading pyrsistent-0.17.3.tar.gz (106 kB)
     |████████████████████████████████| 106 kB 1.5 MB/s 
Collecting chardet<5,>=3.0.2
  Using cached chardet-4.0.0-py2.py3-none-any.whl (178 kB)
Requirement already satisfied: certifi>=2017.4.17 in ./miniconda3/envs/temporal/lib/python3.8/site-packages (from requests->jupyterlab-server~=2.3->jupyterlab) (2020.6.20)
Collecting idna<3,>=2.5
  Using cached idna-2.10-py2.py3-none-any.whl (58 kB)
Collecting urllib3<1.27,>=1.21.1
  Using cached urllib3-1.26.5-py2.py3-none-any.whl (138 kB)
Collecting pytz>=2015.7
  Using cached pytz-2021.1-py2.py3-none-any.whl (510 kB)
Collecting ptyprocess; os_name != "nt"
  Using cached ptyprocess-0.7.0-py2.py3-none-any.whl (13 kB)
Collecting cffi>=1.0.0
  Downloading cffi-1.14.5-cp38-cp38-manylinux1_x86_64.whl (411 kB)
     |████████████████████████████████| 411 kB 392 kB/s 
Collecting python-dateutil>=2.1
  Using cached python_dateutil-2.8.1-py2.py3-none-any.whl (227 kB)
Collecting testpath
  Downloading testpath-0.5.0-py3-none-any.whl (84 kB)
     |████████████████████████████████| 84 kB 424 kB/s 
Collecting mistune<2,>=0.8.1
  Using cached mistune-0.8.4-py2.py3-none-any.whl (16 kB)
Collecting bleach
  Downloading bleach-3.3.0-py2.py3-none-any.whl (283 kB)
     |████████████████████████████████| 283 kB 805 kB/s 
Collecting defusedxml
  Downloading defusedxml-0.7.1-py2.py3-none-any.whl (25 kB)
Collecting jupyterlab-pygments
  Downloading jupyterlab_pygments-0.1.2-py2.py3-none-any.whl (4.6 kB)
Collecting entrypoints>=0.2.2
  Using cached entrypoints-0.3-py2.py3-none-any.whl (11 kB)
Collecting pandocfilters>=1.4.1
  Downloading pandocfilters-1.4.3.tar.gz (16 kB)
Collecting nbclient<0.6.0,>=0.5.0
  Downloading nbclient-0.5.3-py3-none-any.whl (82 kB)
     |████████████████████████████████| 82 kB 917 kB/s 
Collecting sniffio>=1.1
  Using cached sniffio-1.2.0-py3-none-any.whl (10 kB)
Collecting ipykernel
  Downloading ipykernel-5.5.5-py3-none-any.whl (120 kB)
     |████████████████████████████████| 120 kB 1.6 MB/s 
Collecting wcwidth
  Using cached wcwidth-0.2.5-py2.py3-none-any.whl (30 kB)
Collecting parso<0.9.0,>=0.8.0
  Using cached parso-0.8.2-py2.py3-none-any.whl (94 kB)
Collecting pycparser
  Using cached pycparser-2.20-py2.py3-none-any.whl (112 kB)
Collecting webencodings
  Using cached webencodings-0.5.1-py2.py3-none-any.whl (11 kB)
Collecting async-generator
  Downloading async_generator-1.10-py3-none-any.whl (18 kB)
Collecting nest-asyncio
  Downloading nest_asyncio-1.5.1-py3-none-any.whl (5.0 kB)
Building wheels for collected packages: pyrsistent, pandocfilters
  Building wheel for pyrsistent (setup.py) ... done
  Created wheel for pyrsistent: filename=pyrsistent-0.17.3-cp38-cp38-linux_x86_64.whl size=119650 sha256=22cef7c0e4fc9702ba773c5bfae1b6db87e104f4810d4b5090f67ff4add64272
  Stored in directory: /home/rctorr/.cache/pip/wheels/3d/22/08/7042eb6309c650c7b53615d5df5cc61f1ea9680e7edd3a08d2
  Building wheel for pandocfilters (setup.py) ... done
  Created wheel for pandocfilters: filename=pandocfilters-1.4.3-py3-none-any.whl size=7991 sha256=0aa17215e8d90da3d4a46b1034105e67544689b762b10fb12e585b847ed8deef
  Stored in directory: /home/rctorr/.cache/pip/wheels/fc/39/52/8d6f3cec1cca4ceb44d658427c35711b19d89dbc4914af657f
Successfully built pyrsistent pandocfilters
Installing collected packages: tornado, ipython-genutils, traitlets, jupyter-core, json5, six, attrs, pyrsistent, jsonschema, pyparsing, packaging, MarkupSafe, jinja2, pyzmq, nbformat, prometheus-client, ptyprocess, terminado, pycparser, cffi, argon2-cffi, Send2Trash, python-dateutil, jupyter-client, testpath, mistune, pygments, webencodings, bleach, defusedxml, jupyterlab-pygments, entrypoints, pandocfilters, async-generator, nest-asyncio, nbclient, nbconvert, sniffio, idna, anyio, websocket-client, jupyter-server, chardet, urllib3, requests, pytz, babel, jupyterlab-server, pexpect, wcwidth, prompt-toolkit, parso, jedi, backcall, matplotlib-inline, decorator, pickleshare, ipython, ipykernel, notebook, nbclassic, jupyterlab
Successfully installed MarkupSafe-2.0.1 Send2Trash-1.5.0 anyio-3.1.0 argon2-cffi-20.1.0 async-generator-1.10 attrs-21.2.0 babel-2.9.1 backcall-0.2.0 bleach-3.3.0 cffi-1.14.5 chardet-4.0.0 decorator-5.0.9 defusedxml-0.7.1 entrypoints-0.3 idna-2.10 ipykernel-5.5.5 ipython-7.24.1 ipython-genutils-0.2.0 jedi-0.18.0 jinja2-3.0.1 json5-0.9.5 jsonschema-3.2.0 jupyter-client-6.1.12 jupyter-core-4.7.1 jupyter-server-1.8.0 jupyterlab-3.0.16 jupyterlab-pygments-0.1.2 jupyterlab-server-2.6.0 matplotlib-inline-0.1.2 mistune-0.8.4 nbclassic-0.3.1 nbclient-0.5.3 nbconvert-6.0.7 nbformat-5.1.3 nest-asyncio-1.5.1 notebook-6.4.0 packaging-20.9 pandocfilters-1.4.3 parso-0.8.2 pexpect-4.8.0 pickleshare-0.7.5 prometheus-client-0.11.0 prompt-toolkit-3.0.18 ptyprocess-0.7.0 pycparser-2.20 pygments-2.9.0 pyparsing-2.4.7 pyrsistent-0.17.3 python-dateutil-2.8.1 pytz-2021.1 pyzmq-22.1.0 requests-2.25.1 six-1.16.0 sniffio-1.2.0 terminado-0.10.1 testpath-0.5.0 tornado-6.1 traitlets-5.0.5 urllib3-1.26.5 wcwidth-0.2.5 webencodings-0.5.1 websocket-client-1.1.0
$ 
```
Esperar unos minutos, se veran pasar varios mensajes indicando que el proceso de instalación se está realizando, por lo que hay que esperar hasta que aparezca nuevamente el prompt o símbolo de sistema ($ o > según sea el sistema operativo) y no aparezca alguno que diga ERROR, si ese fuera el caso será necesario realizar la instalación nuevamente.

**NOTA**: Es posible que en algunos equipos aparezca un mensaje de error y la instalación nisiquiera comience, en ese caso remplazar el comando `pip` por `pip3`.

Ahora para ejecutar Jupyter Lab en la misma **Terminal** (Anaconda Prompt en Windows) hay que cambiarse o moverse a la carpeta de trabajo y entonces ejecutar el comando `jupyter-lab`, a continuación un ejemplo de su ejecución:

```console
$ cd Desktop/TECP0013ADDAOL2103
Desktop/TECP0013ADDAOL2103 $ jupyter-lab
[I 2021-06-16 16:22:21.259 ServerApp] jupyterlab | extension was successfully linked.
[W 2021-06-16 16:22:21.263 NotebookApp] 'password' has moved from NotebookApp to ServerApp. This config will be passed to ServerApp. Be sure to update your config before our next release.
[I 2021-06-16 16:22:21.444 ServerApp] jupyterlab_github | extension was found and enabled by nbclassic. Consider moving the extension to Jupyter Server's extension paths.
[I 2021-06-16 16:22:21.444 ServerApp] jupyterlab_github | extension was successfully linked.
[I 2021-06-16 16:22:21.444 ServerApp] nbclassic | extension was successfully linked.
[I 2021-06-16 16:22:21.465 ServerApp] nbclassic | extension was successfully loaded.
[I 2021-06-16 16:22:21.466 LabApp] JupyterLab extension loaded from /home/rctorr/miniconda3/lib/python3.7/site-packages/jupyterlab
[I 2021-06-16 16:22:21.466 LabApp] JupyterLab application directory is /home/rctorr/miniconda3/share/jupyter/lab
[I 2021-06-16 16:22:21.470 ServerApp] jupyterlab | extension was successfully loaded.
[I 2021-06-16 16:22:21.470 ServerApp] jupyterlab_github | extension was successfully loaded.
[I 2021-06-16 16:22:21.471 ServerApp] Serving notebooks from local directory: /home/rctorr/Cursos/B1-Procesamiento-de-Datos-con-Python-2020
[I 2021-06-16 16:22:21.471 ServerApp] Jupyter Server 1.8.0 is running at:
[I 2021-06-16 16:22:21.471 ServerApp] http://localhost:8888/lab
[I 2021-06-16 16:22:21.471 ServerApp]     http://127.0.0.1:8888/lab
[I 2021-06-16 16:22:21.471 ServerApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```
Después el último comando Jupyter-Lab se abre en el navegador y ya está listo para trabajar.

---

<ins>Jupyter Notebooks</ins>

Ya hablamos sobre Jupyter Notebooks en el Prework. Vamos a hacer un pequeño repaso para que quede claro cómo aprovechar al máximo este REPL.

[**`Ejemplo 1`**](Ejemplo-01/notebook_de_practica.ipynb)

---

<ins>Variables en Python</ins>

En Python usamos `variables` para asignarles contenido que queremos utilizar después.

- La sintaxis es:

`nombre_de_variable = valor`

`valor` puede ser muchas cosas, que ya iremos aprendiendo poco a poco.

> Me parece muy importante hablar sobre la convención de nombramiento en Python: todas las variables y nombres de funciones se escriben en camel_case, sin excepciones. No es necesario mencionar la convención para clases en este momento, ya que ese tema no se tocará en este módulo.

[**`Ejemplo y Reto 2`**](Ejemplo-02/variables.ipynb)

---

<ins>Operaciones numéricas</ins>

Hemos estado asignando números a variables. En Python podemos realizar operaciones matemáticas de una forma muy sencilla. Simplemente tenemos que usar los `operadores aritméticos` que ya conocemos para hacer operaciones entre las variables que hayamos definido previamente. Los operadores aritméticos en Python son los siguientes:

- Suma: `+`
- Resta: `-`
- Multiplicación: `*`
- División: `/`
- Exponente: `**`
- Cociente entero: `//`
- Residuo de una división o también llamado módulo: `%`

¡Practiquemos con ellos!

> En el Ejemplo se va a usar la función `print`. No es necesario ahondar mucho en el tema, pero sí hay que mencionar la sintaxis básica de cómo llamar estas funciones.

[**`Ejemplo y Reto 3`**](Ejemplo-03/operaciones_numericas.ipynb)

---

<ins>Tipos de datos en Python</ins>

Python tiene diferentes tipos de datos para representar diferentes cosas. Por el momento vamos a aprender los 4 más básicos y esenciales:

- `int` => números enteros
- `float` => números decimales
- `string` => secuencias de caracteres (texto)
- `boolean` => booleanos (True o False)

Por el momento no importa si no entiendes para qué sirven las strings y los booleanos. Eso lo veremos más adelante.

> Explicar por qué necesitamos diferentes tipos de datos, por qué a Python no le da igual leer un "1" que un 1. En el Ejemplo se va a usar la función `type` Hay que explicar cómo funciona llamar una función y pasarle el resultado a otra función.

[**`Ejemplo 4`**](Ejemplo-04/tipos_de_datos.ipynb)

---

<ins>Interpolación de Strings</ins>

Más adelante veremos que las Strings pueden contener información muy relevante dentro de nuestros conjuntos de datos (como nombres de personas, descripciones de procesos, categorías, etc). Por lo pronto, vamos a utilizar nuestras Strings para imprimir anotaciones en nuestros `outputs`. Queremos obtener resultados que se vean más o menos así:

`Suma de variable_1 y variable_2: 10`

Vamos a ver cómo hacer eso.

> Elegí f-strings por sobre las otras formas de interpolar strings porque son las más modernas y su sintaxis se parece mucho a la sintaxis de interpolación de otros lenguajes de programación (como JS y Swift).

[**`Ejemplo y Reto 5`**](Ejemplo-05/interpolacion_de_strings.ipynb)

---

<ins>Booleanos y operadores de comparación</ins>

Ya practicamos con `ints`, `floats` y `strings`. Sólo nos falta entender para qué usar los `booleanos`. Nuestros programas necesitan una manera de "tomar decisiones". Nosotros en la vida real solemos tomar decisiones haciendo comparaciones entre las opciones y tomando la decisión que más nos convenga tomando en cuenta el contexto. El primer paso para lograr esto son los `operadores de comparación`. Sirven para comparar valores. Regresan un booleano `True` cuando la comparación es cierta y un booleano `False` cuando la comparación es falsa.

Python tiene los siguientes `operadores de comparación`:

```
Mayor que: >
Mayor o igual que: >=
Menor que: <
Menor o igual que: <=
Igual que: ==
No igual (distinto) que: !=
```

Veamos cómo funcionan.

> Creo que es muy útil hacer esta referencia de las decisiones que tomamos en la vida real. ¿Cómo es que funciona la inteligencia humana? Y ¿cómo es que los programas emulan esta inteligencia para variar su output dependiendo del input que reciban?

[**`Ejemplo y Reto 6`**](Ejemplo-06/operadores_de_comparacion.ipynb)

---

<ins>Estructuras de control de flujo</ins>

Para finalizar, vamos a juntar todo lo que hemos aprendido el día de hoy y vamos a darle a nuestro programa la capacidad de tomar decisiones. Los programas tienen datos de entrada (inputs) y datos de salida (outputs). Varían sus outputs dependiendo del input que reciban. Para poder tomar decisiones, utilizan las llamadas `estructuras de control de flujo`. Que se ven así:

```
if var_1 > var_2:
    print("OK")
else:
    print("ERROR")
```

Vamos a ver cómo funcionan.

> Lo más importante de aclarar me parece que es la indentación de los bloques de las sentencias if. Se habló sobre ello en el Prework, pero es algo que puede ser confuso. Hay que mencionarlo repetidas veces para que los alumnos entiendan que lo que está indentado pertenece al bloque del if, y lo que no está indentando ya no pertenece.

[**`Ejemplo y Reto 7`**](Ejemplo-07/estructuras_de_control_de_flujo.ipynb)

---

### 3. Postwork

[**`Postwork Sesión 1`**](Postwork/Readme.md)
