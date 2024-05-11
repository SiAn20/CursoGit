# **CURSO GIT**

# CONCEPTOS
## **Clase 1**
**Git:**
Sistema de control de versiones distribuido, cada desarrollador trabaja en una rama diferente. Posteriormente, estas ramas se fusionan de nuevo en la rama principal.

**repositorio:**
Almacen de versiones de los ficheros de un proyecto y sus históricos.

**Control de versiones:** 
Sistema que registra cada cambio que hacemos, permite tener un historico de los cambios, cuando se hicieron y quien los hizo. Importante por rendimiento y es flexible.

**CVS:**
(Concurrent Version System}, es el primer control de versiones.

**Estados de git:**
1. **Modified:** Archivos con cambios no confirmados.
2. **Staged:** Archivo marcado como preparado para ser confirmado.
3. **Commited:** Archivo grabado en el repositorio local (commit).

**Commit:** 
Registrar cambios del repositorio. Como una fotografía con autor, fecha y localización.

**Head:** 
Puntero que referencia el punto actual en el historial de cambios.
****
## **Clase 2**
**Rama de git:**
Es un snapshot, para bifurcaciones y desarrollo no lineal, colaborativo e independiente.

**Conflictos a fusionar 2 Ramas:**
Se da cuando Git no puede determinar que cambio es mas importante que otro.
****
## **Clase 3**

# COMANDOS
## git init
Comando para inicializar Git en un directorio. Existen 2 formas.
```bash
git init <nombre Proyecto>
cd <Proyecto>
```
```bash
cd <directorio de Proyecto>
git init
```
## git add
Indica a Git que quieres incluir actualizaciones en un archivo/directorio. Pasa de Modified a Staged.
```bash
git add <file>
```
## git status
Descripción del árbol de trabajo y ver el estado de los archivos.
```bash
git status
```
## git restore
Restaura un archivo al estado del último commit.
 ```bash
git restore <file>
```
Quitar un archivo del área de staged y restaurarlo al estado del último commit.
  ```bash
git restore --staged <file>
```
## git commit
Confirmar los cambios realizados en el repositorio.
  ```bash
git commit
git commit -m "<descripción>"
git commit -m "<Título>" -m "<descripción>"
```
Para sobreescribir la descripcion del ultimo commit, cambiando el ID y ocultando el commit cambiado:
  ```bash
git commit --ammend -m "<descripción>"
```
## git log
Ver el historial de commits en el repositorio Git.
  ```bash
git log
```
Ver solo descripcion de los commits:
  ```bash
git log --oneline
```
Ver los commits de forma grafica con conexiones:
  ```bash
git log --graph
```
```bash
git --graph --oneline
```
## git branch
Ver ramas disponibles:
```bash
git branch
```
Eliminar una rama:
  ```bash
git branch -d <nombre Rama>
git branch -D <nombre Rama>
```  
Crear una nueva rama:
```bash
git branch <nombre de nueva rama>
```
## git switch
Ingresar a una rama:
```bash 
git switch <nombre Rama>
```
Crear e ingresar a la nueva rama:'
```bash 
git switch -c <nombre Rama>
```
## git merge
Traer los cambios de una rama a la rama actual:
 ```bash 
git merge <nombre Rama>
```
Abrir el editor antes de hacer commit:
```bash 
git merge --edit
```
cancelar una operación de fusión que se encuentra en curso:
```bash 
git merge --abort
```
Evitar el commit automático:
 ```bash 
git merge --no-commit
```
Git creará un commit de fusión adicional:
 ```bash 
git merge <nombre Rama> --no--ff
```
