# GIT y GITHUB

## Introducción
**Git:** es un sistema de control de versiones que rastrea los cambios en los archivos de un proyecto.  
**GitHub:** es una plataforma en línea que utiliza Git para alojar y compartir proyectos de software, facilitando la colaboración entre desarrolladores.

---

## Instalación de GIT y Creación de cuenta en GITHUB
### Videos útiles:
- [Video 1](https://www.youtube.com/watch?v=lGfuztkRr4k)
- [Video 2](https://www.youtube.com/watch?v=WcYTcttEf50)

### Enlaces importantes:
- [Página para crear cuenta en GitHub](https://github.com/)
- [Página de descarga de Git](https://git-scm.com/downloads)

---

## Configuración Básica de GIT
```bash
git config --global user.name "your name" # Configurar el usuario
git config --global user.email "your email" # Configurar el Email
git config --list # Listado de configuraciones
git config --global --list # Lista todas las configuraciones del global
git config --global core.editor “code --wait” # Configura Visual Studio Code como editor
git config --global core.autocrlf=true # Configuración de salto de línea y retorno de carro
git config --local --list # Lista las configuraciones de nuestro repositorio local
```
## Para ver archivos ocultos: 

```bash 
ls -a
```
## Para eliminar el repositorio local:
```bash 
rm -m .git 
```
## Iniciando un repositorio
```bash 
git init # Iniciar GIT en la carpeta donde está el proyecto
git clone <url> # Clonar un repositorio de GitHub
```
## Git add
```bash 
git add . # Añadir todos los archivos a la preparación
git add *.txt # Añadir solo archivos .txt a la preparación
git add [archivo1] [archivo2] # Añadir archivos específicos
git add directorio/[archivo3] # Añadir archivos dentro de un directorio
git mv antiguo.txt nuevo.txt # Cambiar el nombre de un archivo
```
## Git commit
```bash 
git commit -m “Esto es mi primer commit” # Realizar un commit
git commit -a # Commit directo sin pasar por preparación
git checkout [file] # Recuperar un archivo del último commit
git restore [file] # Deshacer cambios del último archivo
```
## Visualización de logs:
```bash 
git log # Ver el identificador de los commits
git log --oneline # Ver lista de commits resumida
git log --oneline --all # Ver lista de commits en todas las ramas
git log --oneline --all --graph # Ver commits en forma gráfica
```

## Modificar el último commit:
```bash
git commit --amend
```
# Git reset
```bash
git reset --soft [hash] # Deshacer un commit y mover archivos al área de preparación
git reset --soft head~1 # Mover el head al commit anterior
git reset --hard [hash] # Mover el head al commit especificado
```
# Mostrar el contenido de un archivo:
```bash 
git show nombre.txt
```

## Git diff
```bash 
git diff Hash2 Hash1 # Comparar dos commits
git diff --staged # Comparar los archivos en preparación con el último commit
git diff –name-only [hash1] [hash2] # Comparar nombres de archivos entre commits
git diff --word-diff [hash1] [hash2] # Comparar las diferencias por palabras entre commits
```
## Git branch
```bash 
git branch # Lista de ramas
git branch [nombre] # Crear nueva rama
git checkout [nombre-rama] # Cambiar a una rama existente
git checkout -b [nombre-rama] # Crear y cambiar a nueva rama
git branch -d [nombre-rama] # Eliminar una rama
git branch -m [nombre-rama] [nuevo-nombre-rama] # Cambiar el nombre de una rama

```

## Git merge 
# Crear un nuevo repositorio:
```bash 
echo "# prueba2" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <url>
git push -u origin main
```
# Conectar a un repositorio existente:
```bash 
git remote add origin <url>
git branch -M main
git push -u origin main
```


## Alias en Git
```bash 
git config --global alias.mi-comando "log --oneline --all --graph"
```

## Git reflog
```bash 
git reflog # Lista todos los commits (historial)
```
## Comandos adicionales
```bash 
git clone # Clonar un repositorio
git push origin master # Subir cambios a la rama master
git pull origin master # Descargar cambios desde la rama master
git remote -v # Ver lista de remotos
```
# Eliminar configuraciones globales:
```bash 
git config --global --unset-all user.name
git config --global --unset-all user.email
```
# Eliminar credenciales:
```bash 
git credential-manager uninstall
```

