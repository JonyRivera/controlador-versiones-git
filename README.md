# TAREA 1: GIT HUB.- CONTROLADOR DE VERSIONES

> Se comprende por controlador de versiones, al manejo de gestión y rastreo del código fuente en la elaboración de un proyecto de software, se puede deducir que es un sistema que registra los cambios en un repertorio, de tal menera que se puede identificar de una forma eficaz las modificaciones de código fuente  efectuadas, llevando un registro del mismo, otra de las ventajas es que no precisamente un programador debe esperar la finalización de un módulo para poder continuar con otra fase del proyecto de software, facilitando la revisión de los cambios conjuntamente con la colaboración en equipo, ya que prácticamente se lo denomina de código abierto.

## Comandos Principales Básicos en Git Hub

- git config --global user.name "Nombre de Usuario"
- git config --global user.email "correo electrónico"
- git init
- git config --list
- git add `nombredearchivo.extensión`
- git commit -m "Mensaje del Commit"
- git commit -m "Mensaje del Commit" -n
- git status
- git log
- git show
- git diff
- git add .
- git add -A

### Comando *git config --global user.name "Nombre de Usuario"*

> El comando **git config --global user.name "VeraJavier"** es utilizado para setear o configurar la preparación del usuario a utlizar.

### Comando *git config --global user.name "E-mail del Usuario"*

> El comando **git config --global user.email "VeraJavier@yahoo.es"** cumple la misma funcionalidad del comando explicado en el párrafo anterior, la diferencia es que este será utilizado para el registro del correo electrónico.

### Comando *git init*
> Este comando ejecuta la inicialización de las configuraciones previa al repositorio nuevo creado, por lo general solo se lo utiliza una sola vez durante el inicio de la configuración.

_git init_

> Su forma de ejecutar es exactamenete como se lo muestra en la línea que antecede.

### Comando *git config --list*
>Este comando **git config --list** se lo utiliza para revisar la configuración previa, ya una vez ejecutado los tres comandos anteriores para el *seteo* y la inicialización, dependiendo el sistema operativo a utilizar, se mostrarán varios parámetros de configuraciones, sin embargo deben aparecer el *nombre de usuario*, el *email* y el *init* insertos en los primeros comandos básicos de la lista, como se visualiza en el siguiente ejemplo, *user.name*, *user.email* e *init.defaultbranch*:

    diff.astextplain.textconv=astextplain
    filter.lfs.clean=git-lfs clean -- %f
    filter.lfs.smudge=git-lfs smudge -- %f
    filter.lfs.process=git-lfs filter-process
    filter.lfs.required=true
    http.sslbackend=openssl
    http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
    core.autocrlf=true
    core.fscache=true
    core.symlinks=false
    pull.rebase=false
    credential.helper=manager
    credential.https://dev.azure.com.usehttppath=true
    init.defaultbranch=master
    user.name=VeraJavier
    user.email=VeraJavier@yahoo.es
    core.repositoryformatversion=0
    core.filemode=false
    core.bare=false
    core.logallrefupdates=true
    core.symlinks=false
    core.ignorecase=true

>Como se puede visualizar en las líneas 14, 15 y 16 de la lista que antecede, se corrobora la configuración de iniciación, el seteo del nombre y del email:

* init.defaultbranch=master
* user.name=VeraJavier
* user.email=VeraJavier@yahoo.es

### Comando *git add `archivo.extensión`*

>Este comando permite agregar al archivo al controlador de versiones en git, para posteriormente ya poder ser comiteado o realizar el **commit**, su sintaxis del comando es la siguiente:

_git add index.js_

> Cabe recalcar que la extensión del archivo puede ser cualquiera, esto depende del programa con cual el programador decida trabajar.

#### _¿Qué es un commit?_

> Un **commit** se lo puede definir como la creación de un punto de partida o instatánea _snapshot_ con la cual se crea un identificador o _id_ este para ser utilizado en los cambios actuales del proyecto.

### Comando *git commit -m "Mensaje del Commit"*

> Como se explicó en el párrafo anterior, lo que es un commit, en este contexto se añade la sintaxis _-m_ más un _"Mensaje"_, lo que significa precisamente eso, la añadidura del nombre del commit, lo que por buenas prácticas este debe definir brevemente los cambios que se van a realizar dentro del _commit_, su forma de digitarla para la ejecución es la siguiente:

_git commit -m "Mi primer commit"_

### Comando *git commit -m "Mensaje del Commit" -n*

> Colocar el comando _-n_ al final del _commit_ este lo que hace es ignorar por completo el _commit_ aquel comando se lo utiliza cuando ya el proyecto está en etapas avanzadas y se requiere realizar pruebas, por lo tanto habrán _commit_ que no será necesario ejecutarlos en ciertas instancias.

### Comando *git status*

> Permite saber el estado actual del proceso, donde se encuentran, qué cambios se han realizado, qué es lo que hay que cambiar o la diferencia de un transcurso a comparación de algún otro, su sintaxis es la siguiente:

_git status_

### Comando *git log*

> Básicamente muestra todos los _commit_ que se han hecho o ejecutado dentro del repositorio, detallando el autor y la fecha con la hora de la creación.

_git  log_

### Comando *git show*

> Este comando permite visualizar el cambio o los cambios que se ha obtenido en un _commit_

### Comando *git diff*

> Muestra los cambios o las modificaciones ejecutados dentro de los archivos, comparándolos entre sí, se lo ejecuta aplicando la siguiente sintaxis:

_git diff_

### Comando *git add .*

> Este comando sirve para agregar todos los archivos al _commit_, también se utiliza _git add -A_ que es prácticamente lo mismo.

### Comando *git add -A*

_git add ._

> Efectúa la misma función del comando _git add ._

## Comandos intermedios en Git Hub

- git branch `NombredelBranch`
- git checkout `Nombredelbranch`
- git branch -m `Nombreactual` `Nombrearenombrar`
- git checkout -b `nombredeusuariodelbranch/especificacartarea`
- git checkout -- .
- git merge
- conflics

#### _¿Qué es un branch?_

> El branch o los branch son líneas de desarrollo independientes, es la subdivisión de la rama principal, donde sea realizan tareas específicas de un tema determinado.

### Comando *git branch `nombredelbranch`*

> Este comando _git branch nombre_ sirve específicamente para la creación del branch, así como se explicó en el párrafo anterior, este es una rama para realizar tareas independiente del _main_ o _master_., se lo ejecuta de la siguiente manera:

_git branch tarea1_

> El _git branch_ muestra todos los branch o ramas existentes.

### Comando *git branch `Nombredelbranch`*

> En la ocasión que se realice un _git branch_ con un nombre ya existente, este se traslada o dirige al branch especificado, por ejemplo si se quiere pasar al branch **tarea1** es suficiente con aplicar el comando _git branch tarea1_

### Comando *git branch -m `Nombreactual` `Nombrearenombrar`*

> Este comando sirve para renombrar un branch, es decir para cambiar de nombre a un branch específico, el ejemplo se lo muestra en la siguiente sitaxis:

_git branch -m tarea1 tarea2_

> Con la ejecución de la línea de código anterior, el nombre del branch es actualizado a **tarea2**

### Comando *git chechkout -b*

> Este comando es muy similiar al _git branch_ la diferencia es que al ejejcutalo _git checkout -b `nombretarea/especificacion` se crea el branch y se dirige directamente dentro del mismo, para ejecutar las acciones ya en el branch creado.

### Comando *git checkout -- .*
> Este comando permite eliminar los cambios dentro del un _branch_ sin ya tener la opción de recuperarlos.

_git checkout -- ._

### Comando *git merge*

>El _git merge_ `branch_a_anidar` añade o anida los cambios de un branch específico dentro de otro, para realiar la acción de añadir el branch, se debe colocar en la rama que se va a insertar, como por dar un ejemplo, este puede ser el _main_ o _master_

_git merge `tarea2`_

### *conflicts*

>En esta ocasión la palabra reversada _conflicts_ no es precisamente un comando en sí, sin embago comunmente aparece cuando hay redundancia en los códidos por lo general después de aplicar un _merge_, por lo que es de gran guía identificar los problemas de sobrescritura de código en la misma línea o espacio de comandos.

## ETIQUETAS  - VERSIONADO SEMÁNTICO
>El versionamiento semántico es un tipo de convención de nomenclatura para nombrar las diferentes versiones del proyecto o softwarwe por ejemplo: x,y,z sería equivalente a una versión software _Foxit 10.2.1_

>Donde el primer número **(10)** antes del punto, equivale a la versión con mayor jerarquría del software.

>La representación del segundo número **(2)** pertenece a los cambios de mediana relevancia del sofware.

>Y la representación del último número **(1)** hace referencia a los pequeños cambios del proyecto o del software.

>El comando que se utiliza para agregar etiquetas y realizar el versionamiento semántico es  _git tag `Nombre`_

* git tag `Nombre`

>Este comando se lo utiliza para crear la etiqueta o la nomenclatura de las versiones, por lo general se usa el formato de números _0.0.1_ ya esto permite facilitar la secuencia de los mismos.

>Comunmente se identifica los _tag_ en cada _branch_ del proyecto de software para tener el versionado actual del mismo.

## ARCHIVOS BINARIOS Y SENSIBLES

* .gitignore
* secrets.yml
* hooks

### .gitignore

>El _**.gitignore**_ es un archivo de texto en el cual se añaden todos los archivos que no se necesitan o se requieran ser leídos al momento de la ejecución, este es sensible a mayúsculas y minúsculas, el cual se colocan parámetros como _logs_ para llevar un registro, comentarios o procesos internos en los cuales son propios de cada programador en sus apuntes personales.

>Dentro del Archivo _.gitinore_ para que este ignore toda una carpeta, este direcotrio debe escribirse _/`NombreCarpeta`_ anteponiendo la barra o el slash **/** seguidamente del nombre de la carpeta, para ignorar un arhivo, este debe estar insertado de la misma forma que se creó `secrets.yml` 

### secrets.yml

>Los archivos _secrets.yml_ se utilizan prácticamente para registrar los códigos internos, contraseñas o apikey propias del proyecto, este archivo de _secrets.yml_ nunca debe estar subido en los repositorios del proyecto, ya que contiene información netamente confidencial.

### hooks

> Los hooks son tareas programadas que se ejecutan conjuntamente en respuestas a una acción o acciones de un repositorio git, mismos que se encuentran en la carpeta oculta del git, por lo general se la localiza en **/.git**

> Estos _hooks_ se utilizan en algunas acciones como se muentra en la siguiente lista

    applypatch-msg.sample* 
    commit-msg.sample*  
    fsmonitor-watchman.sample* 
    post-update.sample* 
    pre-applypatch.sample* 
    pre-commit.sample*
    pre-merge-commit.sample*
    pre-push.sample* 
    pre-rebase.sample* 
    pre-receive.sample*
    prepare-commit-msg.sample*
    push-to-checkout.sample*
    sendemail-validate.sample*
    update.sample*

## GIT AVANZADO - COMANDOS

- git rebase
- git rebase -i HEAD~n
- git stash
- git stash list
- git stash pop
- git stash apply stash@{n}
- git stash pop stash{n}
- git cherry-pick
- git revert

### git rebase

> El comando _git rebase_ se utiliza o este permite cambiar un grupo o series de procesos que han sido confirmados, de tal manera que permite modificar _(edita, ordena, combina)_ el historal del repositorio git.

> Se lo utiliza escribiendo el comando _git rebase_ seguidamente del nombre del branch, por ejemplo:

_git rebase -i `master`_

### git rebase -i HEAD~n

> Sirve para sobrescribir los commit y determinar qué se puede realizar con ellos, se lo puede determinar como un _commit_ interactivo, se puede digitar de las siguientes maneras:

_git rebase -i `nombreDelCommit`_  - ejemplo: _git rebase -i 2769957b40e1b376e268b42e99be445bdf2da464_

_git rebase -i HEAD~`NúmeroDelCommit`_ - ejempo: _git rebase -i HEAD~3_

> Al ejecutar cualquiera de estos comandos, se incrusta a la configuración del _commit_ donde se pueden visualizar los _commit_ agregados, mismo que faclitan los siguiente comandos a utilizar:

- `p`, pick 
- `r`, reword 
- `e`, edit 
- `s`, squash 
- `f`, fixup

> La lista anterior que se muestra, esta indica que se pueden utilzar los comandos de ambas formas, ya sea con la letra de inicio o la palabra completa.

#### `p`, pick

> Este comando sirve para usar el _commit_ directamente, es decir que quede tal cual como se encuentra actualmente.

#### `r`, reword

> Este comando sirve para usar el mismo _commit_ pero con la diferencia que se le cambia el mensaje, es decir cambia la descripción del _commit_.

#### `e`, edit 

> Como su nombre lo indica, siver para editar el commit, aunque su uso es muy poco frecuente.

#### `s`, squash 

> Quiere decir que se va a utilizar el mismo _commit_, integrando el mensaje del anterior _commit_ es decir si se tienen dos _commit_ y al segundo se le aplica el `squash` este se unirá al que antecede manteniendo su descripción.

#### `f`, fixup

> Este comando hace la añadidura del _commit_ que antecede, pero se pierde la refencia, será como fusionar directamente al _commit_ anterior.

### git stash

> El comando _git stash_ es básicamente una estructura de datos en forma de pila, la que permite guardar o gestionar cambios temporales evitanto hacer un _commit_ se uso directo es el siguiente:

_git stash_

> Al ejecutar el comando _git stash_ lo que realiza es guardar temporalmente todos esos cambios a realizar y dejar al branch en su posición como se encontraba

### git stash list

> Muestra todas la pilas que se encuentran en **WIP** _(Work In Progress)_ indicando la posición e identificador correspondiente.
 
_git stash list_

### git stash pop

> Este comando extrae y elimina al mismo tiempo los cambios que se encuentran dentro de la pila

_git stash pop_

### git stash apply stash@{n}

> Este comando extrae los cambios que se encuentran en la pila, a diferencia del _git stash pop_ este no los elimina, solo lo aplica, su estructura `{n}` significa el número de posición, por ejemplo si se quiere trabajar en la posición cero (0), la sintaxis en la siguiente:

_git stash apply stash@{0}_

### git stash pop stash@{n}

> Este comando lo que realiza es eliminar un cambio temporal de la pila, su sintaxis es similar al comando anterior explicado en el párrafo que antecede.

_git stash pop stash@{0}_

### git cherry-pick `IdentificadorDelCommit`
> La función de este comando es selecionar un _commit_ en espefícico y aplicarlo en otro _branch_ directametne, se lo usa generalmente en _commit_ que nunca vayan a hacerse _merge_ es la opción recomendada.

_git cherry-pick `commit`_

### git revert `IdentificadorDelCommit`

> Es un comando que crea un commit para poder revertir un cambio, en ocasiones que no sea el cambio deseado, se puede aplicar un _git revert_ sobre el nuevo `commit` del _git revert_ ejecutado.

git revert `IdentificadorDelCommit`

## GITHUB Y COLABORACIÓN EN EQUIPO

> Github es una plataforma en la nube para poder trabajar remotamente con proyectos, de tal manera que facilita el trabajo de conexión entre programadores para la colaboración común entre diferentes sesiones o módulo.

> Una de las principales ventajas de Github, es que permite adjuntar proyectos personales y en este estar a dispisición de demás usuarios para revisiones de su código fuente, esctuctura, arquitectura, etc.

### Comandos para subir proyecto a Github

- git remote add origin https://github.com/`user/ruta`
- git remote -v
- git branch -M main
- git push -u origin `main`
- git push
- git config -e
- git clone

### git remote add origin https://github.com/`user/ruta`
> Este comando permite crear un remoto desde el sitio local hacia la plataforma de GitHub, cabe mencionar que toda la línea de comando se copia desde la interfaz Web de GibHut, el parámetro `user/ruta` es generado dependiendo de la insersión de datos personales de cada usario.

### git remote -v

> Este comando permite observar la creación del remote, que este se haya creado satisfactoriamente, su sintaxis en la misma que se muestra en el título que antecede.

### git branch -M `main`

> Este comando lo que hace es cambiar la convención, hay usarios que obtienen el _branch_ `main` y sin embargo otros aparecerá con `master`.

### git push -u origin `main`

> Sirve para subir a remoto los cambios que se obtienen en el repositorio local, reorganiza los cambios a la plataforma de GitHub.

### git push

> Este comando _git push_ se utiliza para subir cada cambio del proyecto, ya no es necesario ejecutar _git push -u origin `main`_ cuando ya ha sido ejectudo en primera instancia, ya que se identició el `origin`

### git config -e

> Este comando permite el ingreso a la configuración del archivo remoto `origin`, de tal manera que se puede editar y resolver los problemas lógicos o de redirección.

### git clone

> Este comando sirve para clonar un repositorio ya configurado, con los mismos parámetros ya establecidos y para poder hacer modificacioes específicas.

_git clone https://github.com/JonyRivera/controlador-versiones-git.git_
