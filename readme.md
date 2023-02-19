# Instalación de Git en Windows.

> Descargar el instalador de Git más reciente para Windows.

1. Para ello accedemos a https://git-scm.com/download/win y clicamos sobre `64-bit Git for Windows Setup`. La versión actual en el momento de la descarga es la `2.39.0.2`.

> Ejecutar el instalador.

1. Cuando hayas iniciado correctamente el instalador, deberías ver la pantalla del
asistente de configuración de Git. Selecciona las opciones `Next` (Siguiente)
y `Finish` (Finalizar) para completar la instalación. Las opciones predeterminadas
son las más lógicas en la mayoría de los casos.

# Configuración básica de usuario en Git.

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
3. Ahora es el momento de hacer nuestro primer commit. Para ellos se ejecuta el comando siguiente: `git commit -m "Mi primer commit"`.
4. Con el comando `git log --oneline --graph --decorate –all` podemos obtener información del commit en el que estamos trabajando, de la rama en la que estamos...
5. Ahora podemos definir el remote, que viene a ser establecer la URL de nuestro repositorio (https://github.com/Girobokku/tutorialGit.git). Esto es obligatorio para que podamos hacer el git push. Usamos `git remote add origin https://github.com/Girobokku/tutorialGit.git`.
6. Establecido el remote definiremos la rama. Usamos para ello el comando `git branch -M main`.
7. Ahora hacemos el push con `git push -u origin main`.

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

1. Para ello abrimos el terminal y solo tenemos que introducir el comando `git clone https://github.com/Girobokku/.tutorialGit.git`.

```
git clone https://github.com/Girobokku/tutorialGit.git
```
# Comprobar el estado del repositorio.

> El comando `git status` te mostrará los diferentes estados de los archivos en tu directorio de trabajo y área de ensayo. Qué archivos están modificados y sin seguimiento y cuáles con seguimiento pero no confirmados aún. En su forma normal, también te mostrará algunos consejos básicos sobre cómo mover archivos entre estas etapas.

```
git status
```
# Historial de confirmaciones.

> El comando `git log` se utiliza para mostrar la historia registrada alcanzable de un proyecto desde la más reciente instantánea confirmada hacia atrás. Por defecto sólo se mostrará la historia de la rama en la que te encuentres, pero pueden ser dadas diferentes e incluso múltiples cabezas o ramas desde la que hacer el recorrido. También se utiliza a menudo para mostrar las diferencias entre dos o más ramas a nivel de commit.

```
git log
```

1. En el siguiente ejemplo muestro con `git log` el estado actual del historial antes de hacer un nuevo commit:

```
PS C:\Users\quiqu\Desktop\6.- Control de versiones - Entrega> git log
commit 382664a55882064bdc5eae17a330a94063fdfde0 (HEAD -> main, origin/main)
Author: Quique Vázquez Peñamaría <vazquez.penamaria.enrique.ald@gmail.com>
Date:   Thu Feb 2 13:14:00 2023 +0100

    Añadimos clonar al tutorial

commit dd327c41a84da66bb918ec7154a95b044ee248c4
Author: Quique Vázquez Peñamaría <vazquez.penamaria.enrique.ald@gmail.com>
Date:   Thu Feb 2 10:25:23 2023 +0100
```
2. Ahora muestro de nuevo con `git log` el estado del historial: 

```
PS C:\Users\quiqu\Desktop\6.- Control de versiones - Entrega> git log
commit 4eca9937b3921a418163b7caa75f9e25b43527f6 (HEAD -> main, origin/main)
Author: Quique Vázquez Peñamaría <vazquez.penamaria.enrique.ald@gmail.com>
Date:   Fri Feb 3 09:36:23 2023 +0100

    Cambio en el historial

commit bdb60faea373c5aba9a0aff07fbd6dc82261f92b
Author: Quique Vázquez Peñamaría <vazquez.penamaria.enrique.ald@gmail.com>
Date:   Fri Feb 3 09:33:18 2023 +0100
```
> NOTA: Para salir del historial de confirmaciones pulsamos la tecla `q`.

# Mostrar diferencias entre versiones.

> El comando `git diff` se utiliza cuando deseas ver las diferencias entre dos árboles. Esto prodría ser la diferencia entre tu entorno de trabajo y tu área de ensayo (`git diff` por sí mismo), entre tu área de ensayo y tu última confirmación o commit (`git diff --staged`), o entre dos confirmaciones (`git diff master branchB`).

# Haciendo ramas.

> Para crear una rama se utiliza el comando `git branch Nombre`.

```
git branch Nombre
```

> Ahora, para poder trabajar en esta rama que hemos creado es necesario utilizar el comando `git checkout Nombre`. Así cambiamos a la rama en la que nos interese trabajar.

```
git checkout Nombre
```

> Para consultar las ramas existestes se puede usar el comando `git branch -av`.

```
git branch -av
```

# Haciendo merge en ramas.

> Hacer merge en Git crea un commit especial que tiene dos padres diferentes.

```
git merge Nombre
```

# Haciendo rebase.

> Similar al merge, el rebase nos da un resultado más "elegante", simplificando visualmente el resultado.

```
git rebase Nombre
```