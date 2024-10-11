# Git Comandos

Este proyecto es un repositorio de prueba para aprender y practicar los comandos básicos y avanzados de Git.

## Descripción

El proyecto **Git Comandos** tiene como objetivo crear un entorno para explorar diversas funcionalidades de Git, como la creación de ramas, 
fusión de cambios, cherry-picking, resolución de conflictos y más. A lo largo del proyecto se realizan commits en 
diferentes ramas y se aplican correcciones mediante hotfixes.

## Estructura del Proyecto

- `feature`: Rama en la que se añaden los cambios iniciales y posteriores mejoras.
- `master`: Rama principal que mantiene el código final.
- `hotfix`: Rama para solucionar problemas urgentes.

## Comandos Usados

- `git init`: Inicializar un nuevo repositorio.
- `git config --global user.name "nombre"`: Configurar el nombre del usuario globalmente.
- `git config --global user.email "correo"`: Configurar el correo del usuario globalmente.
- `git checkout -b <rama>`: Crear y cambiar a una nueva rama.
- `git add <archivo>`: Añadir archivos al área de preparación.
- `git commit -m "mensaje"`: Hacer un commit con un mensaje descriptivo.
- `git merge <rama>`: Fusionar los cambios de una rama en la rama actual.
- `git cherry-pick <commit>`: Aplicar un commit específico en la rama actual.
- `git rebase <rama>`: Reaplicar los cambios de una rama encima de otra.

## Ejemplo de Uso

1. Creamos la carpeta del proyecto:
    git init nombre-del-proyecto

2. Abrimos la carpeta que creamos:
    cd git-comandos

3. Ingresamos los datos requeridos para inicializar nuestro proyecto:
    git config --global user.name "Nombre-estudiante"
    git config --global user.email "email@estudiante.com"

4. Creacion de ramas:
    git checkout -b feature
    Tambien debemos de crear la rama master

5. Crear un archivo y realizar el primer commit:
   echo "Texto inicial" > archivo.txt
   git add archivo.txt
   git commit -m "Commit inicial"

Tambien debemos de crear la rama master

6. Cambiamos a la rama master:
    git checkout master

7. Realizamos una fusion :
    git merge feature

8. Revertir el merge:
    git reset --hard HEAD~1

9. Hacer rebase con feature:
    git rebase feature

10. Crear una rama hotfix:
   git checkout -b hotfix 

11. Agregamos un cambio critico:
    echo "Corrección urgente" >> archivo.txt
    git commit -am "Hotfix"

12. Hacer cherry-pick de este cambio en la rama master:
    git checkout master
    git cherry-pick hotfix

13. Revisar el historial:
    git reflog

14. Cambia a la rama feature y haz un cambio en el archivo:
    git checkout feature
    echo "Cambio en feature" > conflicto.txt
    git commit -am "Cambio en feature"


14. cambia a la rama master y realiza un cambio en el archivo:
    git checkout master
    echo "Cambio en master" > conflicto.txt
    git commit -am "Cambio en master"

15. Fusionar las ramas :
    git merge feature

