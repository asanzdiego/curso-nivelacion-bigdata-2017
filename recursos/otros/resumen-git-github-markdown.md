# Chuleta Git, GitHub y Markdown

## Git

- Pro GIT (temas 1, 2, 3 y 6): <https://git-scm.com/book/es/v2>

- Codecademy: <https://www.codecademy.com/learn/learn-git>

- Sistema Control de Versiones Distribuido (más autonomía, menos vulnerable, más limpio)

- Configuración inicial

~~~
git config --global user.name "Nombre que quieras mostrar"
git config --global user.email "correo@electronico.es"
~~~

- Iinicializar un reposiorio

~~~
git init
~~~

- Ver el estado de los archivos

~~~
git status
~~~

-  Ver las diferencias

~~~
git diff
~~~

- Añadir archivos

~~~
git add .
~~~

- Grabar los cambios

~~~
git commit -m "mensaje corto descriptivo con los cambios"
~~~

- Alias

~~~
git config --global alias.list 'log --oneline --decorate --graph --all'
~~~

- Ignorar archivos con .gitignore

- Descargar y combinar

~~~
git pull alias-repositorio-remoto nombre-rama-repositorio-remoto
~~~

- Enviar datos

~~~
git push alias-repositorio-remoto nombre-rama-repositorio-remoto
~~~

- Clonar repositorios

~~~
git clone url-repositorio-remoto
~~~

- Crear una rama

~~~
git branch nombre-rama
~~~

- Cambiar de rama

~~~
git checkout nombre-rama
~~~

- Fusionar ramas

~~~
git merge nombre-rama
~~~

## GitHub

- Claves SSH: <https://help.github.com/articles/generating-ssh-keys/>

- Avatar

- Doble factor de autenticación

- Añadir colaboradores

- Crear organizaciones

- Forkear proyectos

- Pull-requets

- Issues y wikis

- GitHub pages

- Fichero README.md

- Webhooks & services

- Gists

## Markdown

- Sintaxis de Markdown: <http://warpedvisions.org/projects/markdown-cheat-sheet>

- Encabezados

- Listados

- Formato (negrita, cursiva, tachado)

- Tablas

- Citas

- Código

- Enlaces

- Imágenes
