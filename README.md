# GIT
## ¿Qué es GIT?
- Git es un software de control de versiones creado por Linus Torvalds.
- Es un software libre.
- Facilita el desarrollo y el mantenimiento de aplicaciones tanto de foram individual como sobre todo al trabajar en equipo.
- Guarda un registro de todos los cambios que sufran los archivos.

## Funcionamiento
- Git captura el estado del programa junto a un codigo alfanumerico (351df3 "Inicio" -> 23sdd11 "Agregamos funciones" -> ...)
- Las capturas se encuentran cronologicamente
- Esto nos permire regresar a un estado en concreto en el pasado 
- Permite que multiples programadores trabajen con el mismo proyecto haciendo que ellos tengan sus propias instantaneas

## Estructura
Git crea dos áreas:
- **Área de ensayo (staging area):** El comando ***git add*** mueve los archivos al área de ensayo.
- **Repositorio local:** El comando ***git commit*** mueve los archivos al repositorio local.

## Tags
- Indica que el proyecto se encuentra en su primera version y futuras versiones.

## Rama o Branch
- Es la linea de tiempo de los commit (las rama principal se llama master).
- Podemos crear otras ramas paralelas a la rama master.
- Posteriormente podemos fusionar la nueva rama con la rama master en un proceso llamado merge.


## Comandos 
Crear el repositorio:
```
git init
```
Listar los archivos y directorios que estan en la carpeta del proyecto:
```
git status -s
```
Hacer el seguimiento a uno o todos los archivos respectivamente:
```
git add nombre.tipo
git add .
```
Tomar la instantanea de los archivos en seguimiento:
```
git commit -m "Descripción"
```
Listar las instantaneas realizadas.
```
git log --oneline 
```
Hacer una restauracion del archivo:
```
git reset --hard c0d1g0
```
Actualizar los cambios de remoto a local:
```
git pull
```
Realizar un tag para el proyecto:
```
git tag 00-00-00v1 -m "Descripción"
```
Subir las tag al repositorio remoto:
```
git push --tags
```
Clonar un proyecto via https:
```
git clone https://github.com/...
```
Crear una nueva rama:
```
git branch nombre
```
Listar las ramas del proyecto y la rama en la que te encuentras:
```
git branch
```
Cambiar la rama en la que nos encontramos:
```
git checkout nombre-de-la-rama
```
Hacer un merge (El merge se debe hacer desde la rama master):
```
git merge nombre-de-la-rama-a-fucionar
```
Sube los cambios en la rama 'main' al repositorio remoto:
```
git push origin main
```
Eliminar la rama:
```
git branch -d nombre-rama
```
Es un nuevo commit que sobre escribe el ultimo commit que realizaste:
```
git commit --amend -m "Descripción"
```
Forzar el push al repositorio remoto:
```
git push origin main --force
```


