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

# Comandos y pasos a seguir: 

# Otros:
> `git clone [url]` clona un repositorio remoto para tenerlo como local.

# PRACTICA 3:

1. Se puede usar el comando `git diff` para ver la diferencia entre dos origenes o ramas o con respecto a la última versión guardada de nuestro repositorio.
2. Se puede usar el comando `git show` para ver aún más detalles sobre commits o ramas.
3. El comando `git annotate (fichero)` se puede usar para ver quien ha hecho cambios sobre un archivo.

# PRACTICA 4:

1. El comando `git checkout` se puede utilizar para deshacer los cambios realizados, volviendo a la versión que estaba en el repositorio. Para eso se necesita especificarela rchivo que queremos hacer volver a su estado del respositorio con `git checkout -- (archivo)` o `git checkout -- . ` para todos los de la carpeta. 
2. El comando `git restore stage` para deshacer un git add o hacer simplemente `git restore (archivo)` para deshacer los cambios que hicimos a un archivo.
3. El comando `git reset` sirve para borrar cambios en diferentes partes, se puede especificar el archivo y la versión a la que resetear. Tiene 3 posibles atributos (principales) siendo estos:
    > `--soft` El cual reseteará los cambios en el HEAD, es decir, el commit.
    > `--mixed` que borrará el commit y el git add
    > `--hard` que borrará elc ommit, el git add y los cambios en nuestro repositorio local.

# PRACTICA 5:

1. El comando `git branch (nombre_branch)` sirve para crear una rama nueva, que es básicamente una especie de puntero desde el último commit hecho.
    > `git branch -av` indicará una lista de ramas.
    > `git branch -d (nombre_branch)` eliminará la rama especificada.
2. El comando `git checkout (nombre_branch)` cambiará la branch actual a la especificada.
3. El comando `git merge (nombre_branch)` mergeará (unirá, juntará...) la rama especificada con la actual.

* asd
* asd
    * asd

1. asdasd
2. 