# Solución ejercicios Git, GitHub y Markdown



## Repositorio masteruah (I)

1. Crear un repositorio en vuestro GitHub llamado **masteruah**.


![Crear un repositorio](../slides/img/git/github-new-repo.png)

## Repositorio masteruah (II)

1. Clonar vuestro repositio en local.

~~~
git clone git@github.com:asanzdiego/masteruah.git
~~~

## README

1. Crear (si no lo habéis creado ya) en vuestro repositorio local
un documento **README.md**.

> Notas: en este documento tendreís que ir poniendo los **comandos**
> que habéis tenido que utilizar durante todos los ejercicios
> y las **explicaciones y capturas de pantalla** que consideréis **necesarias**.

~~~
touch README.md
~~~

## Commit inicial

1. Añadir al README.md los comanddos utilizados hasta ahora
y hacer un coomit inicial con el mensaje **commit inicial**.

~~~
git add .
git commit -m "commit inicial"
~~~

## Push inicial

1. Subir los cambios al repositorio remoto.

~~~
git push origin master
~~~

## Ignorar archivos (I)

1. Crear en el repositorio local un fichero llamado **privado.txt**.

~~~
touch privado.txt
~~~

1. Crear en el repositorio local una carpeta llamada **privada**.

~~~
mkdir privada
~~~

## Ignorar archivos (II)

1. Realizar los cambios oportunos para que tanto el archivo como
la carpeta sean ignorados por git.

~~~
echo "privado.txt" > .gitignore
echo "/privada" > .gitignore
git add .
git commit -m "añadido fichero .gitignore"
~~~

## Añadir fichero 1.txt

1. Añadir fichero **1.txt** al repositorio local.

~~~
touch 1.txt
git add .
git commit -m "añadido 1.txt"
~~~

## Crear el tag v0.1

1. Crear un tag **v0.1**.

~~~
git tag v0.1
~~~

## Subir el tag v0.1

1. Subir los cambios al repositorio remoto.

~~~
git push --tag origin master
~~~

## Crear una rama v0.2

1. Crear una rama **v0.2**.

~~~
git branch v0.2
~~~

1. Posiciona tu carpeta de trabajo en esta rama.

~~~
git checkout v0.2
~~~

## Añadir fichero 1.txt

1. Añadir un fichero **2.txt** en la rama **v0.2**.

~~~
touch 2.txt
git add .
git commit -m "añadido 2.txt"
~~~

## Crear rama remota v0.2

1. Subir los cambios al reposiorio remoto.

~~~
git push origin v0.2
~~~

## Merge directo

1. Posicionarse en la rama **master**.

~~~
git checkout master
~~~

1. Hacer un merge de la rama **v0.2** en la rama **master**.

~~~
git merge v0.2 -m "merge v0.2 sin conflictos"
~~~

## Merge con conflicto (I)

1. En la rama **master** poner **Hola** en el fichero **1.txt** y hacer commit.

~~~
git checkout master
echo "Hola" >> 1.txt
git add .
git commit -m "hola en 1.txt"
~~~

## Merge con conflicto (II)

1. Posicionarse en la rama **v0.2** y poner **Adios** en el fichero "1.txt" y hacer commit.

~~~
git checkout v0.2
echo "Adios" >> 1.txt
git add .
git commit -m "adios en 1.txt"
~~~

## Merge con conflicto (III)

1. Posicionarse de nuevo en la rama **master** y hacer un merge con la rama **v0.2**

~~~
git checkout master
git merge v0.2
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"
~~~

## Listado de ramas

1. Listar las ramas con merge y las ramas sin merge.

~~~
git branch --merged
git branch --no-merged
~~~

## Arreglar conflicto

1. Arreglar el conflicto anterior y hacer un commit.

~~~
vim 1.txt
git add .
git commit -m "arreglado merge en 1.txt"
~~~

## Borrar rama

1. Crear un tag **v0.2**

~~~
git tag v0.2
~~~

1. Borrar la rama **v0.2**

~~~
git branch -d v0.2
~~~

## Listado de cambios

1. Listar los distintos commits con sus ramas y sus tags.

~~~
git config --global alias.list 'log --oneline --decorate --graph --all'
git list
~~~

## Cuenta de GitHub

1. Poner una foto en vuestro perfil de GitHub.

1. Poner el doble factor de autentificación en vuestra cuenta de GitHub.

1. Añadir (si no lo habéis hecho ya) la clave pública que se corresponde a tu ordenador.

## Uso social de GitHub

1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y sigueles.

1. Seguir los repositorios **masteruah** del resto de tus compañeros.

1. Añadir una estrella a los repositorios **masteruah** del resto de tus compañeros.

## Crear una tabla

1. Crear una tabla de este estilo en el fichero **README.md** con la información
de varios de tus compañeros de clase:

|        NOMBRE          |                     GITHUB                        |
|------------------------|---------------------------------------------------|
| Nombre del compañero 1 | [enlace a github 1](http://github.com/asanzdiego) |
| Nombre del compañero 2 | [enlace a github 1](http://github.com/asanzdiego) |
| Nombre del compañero 3 | [enlace a github 3](http://github.com/asanzdiego) |

## Colaboradores

1. Poner a [github.com/asanzdiego](http://github.com/asanzdiego) como colaborador
del repositorio **masteruah**

## Crear una organización

1. Crear una organización llamada **masteruah-tunombredeusuariodegithub**

## Crear equipos

1. Crear 2 equipos en la organización **masteruah-tunombredeusuariodegithub**,
uno llamado **administradores** con más permisos y otro **colaboradores** con menos permisos.

1. Meter a [github.com/asanzdiego](http://github.com/asanzdiego) y a 2 de vuestros
compañeros de clase en el equipo **administradores**.

1. Meter a [github.com/asanzdiego](http://github.com/asanzdiego) y a otros 2 de vuestros
compañeros de clase en el equipo **colaboradores**.

## Crear un index.html

1. Crear un index.html que se pueda ver como página web en la organización.

## Crear Pull-requests

1. Hacer 2 forks de 2 repositorios **masteruah-tunombredeusuariodegithub.github.io**
de 2 organizaciones de las que no seais ni administradiores ni colaboradores.

1. Crearos una rama en cada fork.

1. En cada rama modificar el fichero **index.html** añadiendo vuestro nombre.

1. Con cada rama hacer un pull-request.

## Gestionar Pull-requests

1. Aceptar los pull-request que lleguen a los repositorios de tu organización.
