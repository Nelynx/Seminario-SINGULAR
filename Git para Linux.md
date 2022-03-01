* Descargar `gh` y `git`
* 

### Usar `git` en un nuevo ordenador
Utiliza el comando `gh auth login`.
La CLI te ayudará a registrar tu cuenta de usuario Git en tu ordenador.

### Crear un repositorio desde mi ordenador
Crea una carpeta (`mkdir <folder>`) o entra en la carpeta donde tengas tus archivos (`cd <folder>`) e introduce el comando `git init`.

### Descargar un repositorio existente a mi ordeandor
Utiliza el comando `git clone <url_repo> [folder]`.
Por defecto, `git` guardará el repositorio en `$pwd`.

### Descargar cambios en el repositorio
Para descargar los cambios en el repositorio, utiliza `git pull`.

### Crear y cambiar ramas
Utiliza el comando `git branch` para listar ramas existentes.
Puedes cambiar entre ramas existentes utilizando `git checkout <branch>`.
Si la rama no existe, la puedes crear (y entrar en ella) utilizando `git checkout -b <branch>`.

### Añadir cambios a una rama 
Utiliza el comando `git add <files>` (`.` añadirá todos los archivos en `$pwd`) seguido de `git commit -m [commit_msg]`.
Ahora utiliza `git push -u origin <branch>` para subir los archivos a la rama.

También puedes utilizar `git config push.default current` para añadir cambios a la rama donde estás actualmente.
La bandera `--global` hará que este sea el comportamiento global de `git` en tu ordenador.
