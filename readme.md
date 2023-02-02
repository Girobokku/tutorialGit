# Instalación de Git en Windows

> Descargar el instalador de Git más reciente para Windows.

1. Para ello accedemos a https://git-scm.com/download/win y clicamos sobre `64-bit Git for Windows Setup`. La versión actual en el momento de la descarga es la `2.39.0.2`.

> Ejecutar el instalador.

1. Cuando hayas iniciado correctamente el instalador, deberías ver la pantalla del
asistente de configuración de Git. Selecciona las opciones `Next` (Siguiente)
y `Finish` (Finalizar) para completar la instalación. Las opciones predeterminadas
son las más lógicas en la mayoría de los casos.

# Configuración básica de usuario en Git

> Abrir el Git Bash o símbolo de sitema.

1. Abre el símbolo del sistema (o Git Bash si durante la instalación seleccionaste no
usar Git desde el símbolo del sistema de Windows).

> Configurar tu nombre de usuario y mail en Git.

2. Ejecuta los siguientes comandos para configurar tu nombre de usuario y
dirección de correo electrónico de Git. Esta información se asociará a todas las
confirmaciones que hagas:

```
git config --global user.email “vazquez.penamaria.enrique.ald@gmail.com"
```
```
git config --global user.name "Quique Vázquez Peñamaría"
```
# Crear un nuevo repositorio.
1. Creamos un directorio con el archivo `hola.txt` y `git.txt` e inicializamos el repositorio introduciendo en el terminal `git init`.
2. El siguiente paso será añadir los archivos al repositorio que acabamos de crear. Como en el directorio que hemos creado tenemos dos archivos y queremos subir ambos al repositorio, utiliozaremos el comando `git add  . `, que añade todos los archivos del directorio. En caso de haber más archivos y que no nos interese añadir alguno, sería necesario crear el archivo `.gitignore`. Más adelante se explicará su uso.
3. Ahora es el momento de hacer nuestro primer commit. Para ellos se ejecuta el comando siguiente: `git commit -m "Mi primer commit"`
4. Con el comando `git log --oneline --graph --decorate –all` podemos obtener información del commit en el que estamos trabajando, de la rama en la que estamos...
5. Ahora podemos definir el remote, que viene a ser establecer la URL de nuestro repositorio (https://github.com/Girobokku/tutorialGit.git). Esto es obligatorio para que podamos hacer el git push. Usamos `git remote add origin https://github.com/Girobokku/tutorialGit.git`
6. Establecido el remote definiremos la rama. Usamos para ello el comando `git branch -M main`
7. Ahora hacemos el push con `git push -u origin main`

```
git init
git add .
git commit -m "Mi primer commit"
git log --oneline --graph --decorate –all
git remote add origin https://github.com/Girobokku/tutorialGit.git
git branch -M main
git push -u origin main
```

# Clonar un repositorio existente.
>Si lo que sucede es que tenemos un repositorio en GitHub y queremos seguir trabajando desde casa o hemos borrado los archivos de nuestro PC siempre podemos clonar lo que ya hemos subido y recuperar nuestro repositorio a local.

1. Para ello abrimos el terminal y solo tenemos que introducir el comando `git clone https://github.com/Girobokku/tutorialGit.git`

```
git clone https://github.com/Girobokku/tutorialGit.git
```
