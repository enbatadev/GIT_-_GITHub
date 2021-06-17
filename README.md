## **Fichero de muestra donde seguir la formación sobre GIT.**

### Primeros pasos:

_2021/06/16_ 
 
Creamos el directorio donde estará nuestro proyecto, programa o similar. En este caso será *GIT_&_GITHub*.

Creamos el stating (área de preparación) y repositorio local. 
```
% git init
```	

- Dandonos la siguiente respuesta: 
```
Initialized empty Git repository in /Users/enbata/Documents/Primeras Pruebas/GIT_&_GITHub /.git/
```
> > Nos indica que se ha creado el repositorio local vacio.
> >
Veremos el estatus del repositorio local.
```
% git status
```
- Dandonos la siguiente respuesta: 
```
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```
> > Nos indica que estamos en el branch master (mas adelante lo estudiaremos), que no a existido ningún commit (mas adelante lo estudiaremos). Además nos pide que creemos o copiemos un fichero en este directorio, ya usemos "git add" para añadirlo al repositorio.
> >
Le hacemos caso y creamos un fichero :grin: , README.md.
```
touch README.md
```
Mediante el programa Markdown Editor estoy modificando el fichero con este contenido :wink: .

Tras la modificación revisamos el estatus del repositorio local.
```
% git status
```
- Dandonos la siguiente respuesta: 
```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
```
> > Nos sigue indicando que estamos en la rama (branch) master, que no ha existido ningún commit, y que tenemos un fichero, en este caso el README.md en el estado untracked (aún no vive en GIT). Para realizar el commit nos pide que lo añadamos a git.
> >
Le hacemos caso y lo añadimos al git.
```
% git add README.md
```
> > Se ha añadido bien y no hay ninguna respuesta.
> >
Comprobamos de nuevo el estatus del repositorio local.
```
% git status
```
- Dandonos la siguiente respuesta: 
```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   README.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md
```
> > Nos sigue indicando que estamos en la rama (branch) master, que no ha existido ningún commit. y que tenemos un fichero, en este caso el README.md en el estado staged (vive en GIT, pero no es guardado definitivamente). Como lo he modificado, nos pide que lo añadamos a git de nuevo o descartemos las modificaciones restaurandolo a la copia anterior. Desde este punto nosotros ya generaremos el commit, para guardar los cambios en el repositorio local.
> >
Añadiremos de nuevo el fichero, para recoger los últimos cambios del fichero, y luego realizaremos el commit.
```
% git add README.md
% git commit -m "Generado fichero README.md"
```
- Dandonos la siguiente respuesta: 
```
[master (root-commit) 44b4b38] Generado fichero README.md
 1 file changed, 89 insertions(+)
 create mode 100644 README.md
```
> > Añadido el fichero a la rama master con el mesaje que hemos puesto.
> >

_2021/06/17_

Comprobamos de nuevo el estatus del repositorio local.
```
% git status
```
- Dandonos la siguiente respuesta: 
```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
> > Nos sigue indicando que estamos en la rama (branch) master. Como lo he vuelto a modificar :man_facepalming: , nos pide que lo añadamos a git de nuevo o descartemos las modificaciones restaurandolo a la copia anterior. Desde este punto nosotros ya generaremos el commit, para guardar los cambios en el repositorio local.
> >
<<<<<<< HEAD
[/Users/enbata/Desktop/Captura de pantalla 2021-06-17 a las 9.54.16.png](url)
=======
[https://github.com/enbatadev/GIT_-_GITHub/blob/main/Captura%20de%20pantalla%202021-06-17.png](url)
>>>>>>> 7992d12 (Generado fichero README.md)
> > Añadimo el fichero y vemos que se cambia verde, para indicarnos que está movido.
> >
Añadimos una captura de pantalla para ver los colores. Realizamoa el add de esta imagen. Y el commit, aunque de forma diferente a la anterior. Utilizaremos la opción del comando "--amend" para que en vez de generar un commit nuevo, se modifique añadiendose al anterior.
> > Abre el editor vi, apra modificar el texto del commit.
Ya tenemos los ficheros en el repositorio local.
```
% git status

On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   Captura de pantalla 2021-06-17 a las 9.54.16.png
	modified:   README.md
```

### Repositorio remoto:

Vamos a utilizar Github como repositorio remoto. Ya teniendo cuenta en Github, nos conectamos y creamos el repositorio desde la página de Github. Ahora uniremos el repositorio local con el remoto. Utilizaremos los comandos recomendados por Github.
```
% git remote add origin git@github.com:enbatadev/GIT_-_GITHub.git
```
Cambiaremos el nombre de la rama de Master a Main **(Tengo que investigar porque pide esto)**.
```
% git branch -M main
```
Subimos el repositorio local al remoto con push.
```
% git push -u origin main
```
 
> > He modificado la dirección de la captura para ver los colores.



























