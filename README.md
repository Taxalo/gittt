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