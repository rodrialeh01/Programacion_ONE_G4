# Git

## Inicializar un repositorio

Para inicializar un repositorio en una carpeta, se debe ejecutar el siguiente comando:

```bash
git init
```

## Ver el estado del repositorio

Para ver el estado del repositorio, se debe ejecutar el siguiente comando:

```bash
git status
```

## Agregar archivos al repositorio

Para agregar archivos al repositorio, se debe ejecutar el siguiente comando:

```bash
git add <nombre_archivo>
```

Para agregar todos las modificaciones archivos al repositorio, se debe ejecutar el siguiente comando:

```bash
git add .
```

## Crear un commit

Para crear un commit, se debe ejecutar el siguiente comando:

```bash
git commit -m "Mensaje del commit"
```

Debe ser un mensaje descriptivo de lo que se hizo en el commit.

## Configurar el usuario global

Para configurar el usuario, se debe ejecutar el siguiente comando:

```bash
git config --global user.name "Nombre de usuario"
git config --global user.email "Correo electrónico"
```

## Configurar el usuario local

Para configurar el usuario de forma local, se debe ejecutar el siguiente comando:

```bash
git config --local user.name "Nombre de usuario"
git config --local user.email "Correo electrónico"
```

## Ver el nombre

Para ver el nombre registrado, se debe ejecutar el siguiente comando:

```bash
git config user.name
```

## Ver el correo electrónico

Para ver el correo electrónico registrado, se debe ejecutar el siguiente comando:

```bash
git config user.email
```

## Ver el historial de commits

Para ver el historial de commits, se debe ejecutar el siguiente comando:

```bash
git log
```

## Ver el historial de commits en una línea

Para ver el historial de commits (locales), se debe ejecutar el siguiente comando:

```bash
git log --oneline
```

## Ver las modificaciones de los archivos en los commits

Para ver las modificaciones de los archivos en los commits, se debe ejecutar el siguiente comando:

```bash
git log -p
```

Para salir de ver las modificaciones de los archivos en los commits, se debe ejecutar el siguiente comando:

```bash
:q
```

## Ver el historial de commits customizado

Para ver el historial de commits customizado, se debe ejecutar el siguiente comando:

```bash
git log --pretty=format:"%h - %an, %ar : %s"
```
Donde:
- %h: hash del commit
- %an: nombre del autor
- %ar: fecha del commit
- %s: mensaje del commit

## Visualizar los ultimos N commits

```bash
git log -n <cantidad de los ultimos commits a visualizar>
```

## Ignorar archivos en el repositorio

Crear un archivo llamado `.gitignore` en la raíz del proyecto y agregar los archivos que se quieren ignorar.

## Descartar los cambios hechos en un archivo

Para descartar los cambios hechos en un archivo, se debe ejecutar el siguiente comando:

```bash
git restore <nombre_archivo>
```

## Descartar los cambios hechos luego de agregarlo al repositorio

Para descartar los cambios hechos luego de agregarlo al repositorio, se debe ejecutar el siguiente comando:

```bash
git restore --staged <nombre_archivo>
```

## Revertir un commit

Para revertir un commit, se debe ejecutar el siguiente comando:

```bash
git revert <hash_commit>
```

## Guardar temporalmente los cambios

Para guardar temporalmente los cambios, se debe ejecutar el siguiente comando:

```bash
git stash
```

## Ver los cambios guardados temporalmente

Para ver los cambios guardados temporalmente, se debe ejecutar el siguiente comando:

```bash
git stash list
```

## Recuperar los cambios guardados temporalmente

Para recuperar los cambios guardados temporalmente, se debe ejecutar el siguiente comando:

```bash
git stash apply <id>
```

## Recuperar los cambios guardados temporalmente y eliminarlos de la lista

Para recuperar los cambios guardados temporalmente y eliminarlos de la lista, se debe ejecutar el siguiente comando:

```bash
git stash pop
```


---

## Repositorios remotos
### Crear Repositorio Remoto

Para crear un servidor remoto, se debe ejecutar el siguiente comando:

```bash
git init --bare
```

### Agregar un servidor remoto a un servidor local

Para agregar un servidor remoto a un servidor local, se debe ejecutar el siguiente comando:

```bash
git remote add nombreservidorlocal <url_servidor>
```

### Enlista los repositorios remotos

Para enlista los repositorios remotos, se debe ejecutar algunos de los siguientes comandos:

```bash
git remote
git remote -v
```

### Clonar un repositorio

Para clonar un repositorio, se debe ejecutar el siguiente comando:

```bash
git clone <url_repositorio>
```

### Clonrar un repositorio y cambiar el nombre de la carpeta

Para clonar un repositorio y cambiar el nombre de la carpeta, se debe ejecutar el siguiente comando:

```bash
git clone <url_repositorio> <nombre_carpeta>
```

### Enviar los cambios al repositorio remoto

Para enviar los cambios al repositorio remoto, se debe ejecutar el siguiente comando:

```bash
git push <nombre_repositorio_remoto> <nombre_rama>
```

### Renombrar un repositorio remoto

Para renombrar un repositorio remoto, se debe ejecutar el siguiente comando:

```bash
git remote rename <nombre_repositorio_remoto> <nuevo_nombre_repositorio_remoto>
```

### Recibir los cambios hechos en el repositorio remoto

Para recibir los cambios hechos en el repositorio remoto, se debe ejecutar el siguiente comando:

```bash
git pull <nombre_repositorio_remoto> <nombre_rama>
```

### Subir un repositorio local a un repositorio remoto en github

Para pushear un repositorio local a un repositorio remoto, se debe ejecutar el siguiente comando:

```bash
git remote add origin <url_repositorio>
git push origin master
```

Luego solicitara loguearse a github (solo si no esta previamente logueado en su computadora).

---

## Ramas

### Ver las ramas

Para ver las ramas, se debe ejecutar el siguiente comando:

```bash
git branch
```

### Crear una rama

Para crear una rama, se debe ejecutar el siguiente comando:

```bash
git branch <nombre_rama>
```

### Cambiar de rama

Para cambiar de rama, se debe ejecutar el siguiente comando:

```bash
git checkout <nombre_rama>
```

### Crear una rama y cambiar a ella

Para crear una rama y cambiar a ella, se debe ejecutar el siguiente comando:

```bash
git checkout -b <nombre_rama>
```

### Llevar el trabajo de una rama a otra

Para llevar el trabajo de una rama a otra, se debe ejecutar el siguiente comando:

```bash
git merge <nombre_rama_destino>
```

Y para salir de ese commit, se debe ejecutar el siguiente comando:

```bash
:x
```

### Hacer un rebase

Para hacer un rebase y solo se actualiza lo de esa rama a la rama destino sin afectar las demas ramas, se debe ejecutar el siguiente comando:

```bash
git rebase <nombre_rama>
```

### Ver las ramas de forma grafica en la terminal

Para ver las ramas en la terminal, se debe ejecutar el siguiente comando:

```bash
git log --graph
```

## Navegar en entre commits

### Ver los commits

Para ver el proyecto del commit destino, se debe ejecutar el siguiente comando:

```bash
git checkout <hash_commit>
```

## Ver las diferencias entre dos commits

Para ver las diferencias entre dos commits, se debe ejecutar el siguiente comando:

```bash
git diff <hash_commit_inicio>..<hash_commit_final>
```

## Ver la diferencia entre mi codigo y el ultimo commit

Para ver la diferencia entre mi codigo y el ultimo commit, se debe ejecutar el siguiente comando:

```bash
git diff
```

---

## Manejo de Etiquetas

### Crear una Tag

Para la creación de etiquetas, se debe ejecutar el siguiente comando:

```bash
git tag -a <nombre de la etiqueta> -m "Mensaje"
```

### Visualizar las etiquetas

Para visualizar las etiquetas, se debe ejecutar el siguiente comando:

```bash
git tag
```

### Subir la etiqueta

Para pushear la etiqueta, se debe ejecutar el siguiente comando:

```bash
git push origin <nombre_tag>
```

