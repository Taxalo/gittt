# gittt

## Comandos y pasos a seguir: 
1. Tras crear los archivo hola.txt y git.txt inicializamos el repositorio con `git init`
2. Tras hacer eso, añadimos los archivos, en este caso como en la carpeta solo hay 2 archivos podemos hacer `git add  .`. Si hubiera más archivos que no querríamos añadir pero queremos añadir todo habría que crear un archivo .gitignore
3. Ahora hacemos el commit de ambos archivos con `git commit -m "Mensaje"`
4. Con el comando `git log --oneline --graph --decorate –all` sabemos en qué commit estamos trabajando, la rama…
5. Ahora definimos el remote, es decir, la URL del repo (https://github.com/Taxalo/gittt). Esto es necesario para pushear. Y ponemos la branch como main (aunque ya la tenemos por defecto) usamos `git remote add origin https://github.com/Taxalo/gittt` y después `git branch -M main` para definir la rama.
6. Ya que hemos creado un archivo readme.md debemos hacer un pull ignorando los errores. Para esto usamos `git pull origin main --alow-unrelated-histories`
7. Ahora hacemos el push con `git push -u origin main`

## Otros:
> `git clone [url]` clona un repositorio remoto para tenerlo como local.

## PRACTICA 3:

1. Se puede usar el comando `git diff` para ver la diferencia entre dos origenes o ramas o con respecto a la última versión guardada de nuestro repositorio.
2. Se puede usar el comando `git show` para ver aún más detalles sobre commits o ramas.
3. El comando `git annotate (fichero)` se puede usar para ver quien ha hecho cambios sobre un archivo.

## PRACTICA 4:

1. El comando `git checkout` se puede utilizar para deshacer los cambios realizados, volviendo a la versión que estaba en el repositorio. Para eso se necesita especificarela rchivo que queremos hacer volver a su estado del respositorio con `git checkout -- (archivo)` o `git checkout -- . ` para todos los de la carpeta. 
2. El comando `git restore stage` para deshacer un git add o hacer simplemente `git restore (archivo)` para deshacer los cambios que hicimos a un archivo.
3. El comando `git reset` sirve para borrar cambios en diferentes partes, se puede especificar el archivo y la versión a la que resetear. Tiene 3 posibles atributos (principales) siendo estos:
    > `--soft` El cual reseteará los cambios en el HEAD, es decir, el commit.
    > `--mixed` que borrará el commit y el git add
    > `--hard` que borrará elc ommit, el git add y los cambios en nuestro repositorio local.

## PRACTICA 5:

1. El comando `git branch (nombre_branch)` sirve para crear una rama nueva, que es básicamente una especie de puntero desde el último commit hecho.
    > `git branch -av` indicará una lista de ramas.
    > `git branch -d (nombre_branch)` eliminará la rama especificada.
2. El comando `git checkout (nombre_branch)` cambiará la branch actual a la especificada.
3. El comando `git merge (nombre_branch)` mergeará (unirá, juntará...) la rama especificada con la actual.