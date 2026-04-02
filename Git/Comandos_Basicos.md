## Lista de Conflictos

git diff se usa para hacer una lista de conflictos.
Para poder ver conflictos con respecto al archivo base, usa:

```bash
git diff --base <file name>
```

El siguiente comando se usa para ver las diferencias que hay entre las ramas antes de fusionarlas:

```bash
git diff <source-branch> <target-branch>
```

Para ver una lista de todos los conflictos presentes usa:

```bash
git diff
```

## Historial del Repositorio

`git log` se usa para ver el historial de commits del repositorio.

Comando basico:

```bash
git log
```

Salida tipica (resumida):

```bash
commit a1b2c3d4e5f67890abc123def4567890abcdef12
Author: Nombre Apellido <correo@ejemplo.com>
Date:   Thu Apr 2 10:30:00 2026 -0500

	Mensaje del commit
```

Comandos utiles para revisar historial:

```bash
# Historial en una sola linea
git log --oneline

# Historial con grafo de ramas
git log --oneline --graph --all

# Ultimos 10 commits
git log -n 10

# Historial de un archivo especifico
git log -- <archivo>

# Ver cambios de cada commit
git log -p

# Buscar commits por autor
git log --author="Nombre"
```

### git reset

git reset sirve para restablecer el index y, segun la opcion, el directorio de trabajo al estado indicado.

```bash
git reset --hard HEAD
```

### git rm

git rm se puede usar para remover archivos del index y del directorio de trabajo.

```bash
git rm filename.txt
```

### git stash

git stash guardara momentaneamente los cambios que no estan listos para ser confirmados.
De esta manera, puedes volver al proyecto más tarde.

```bash
git stash
```

### git show

git show se usa para mostrar informacion sobre cualquier objeto git.

```bash
git show
```

### git fetch

Le permite al usuario buscar todos los objetos de un repositorio remoto que actualmente no se encuentran en el directorio de trabajo local.

```bash
git fetch origin
```

### git ls-tree

Te permite ver un objeto de árbol junto con el nombre y modo de cada item, y el valor blob de SHA-1.
Si quieres ver el HEAD, usa:

```bash
git ls-tree HEAD
```

### git cat-file

Se usa para ver la informacion de tipo y tamaño de un objeto de repositorio,
Usa la opcion -p junto con el valor SHA-1 del objeto para ver la informacion de un objeto especifico, por ejemplo:

```bash
git cat-file -p 321434
```

### git grep

Le permite al usuario buscar frases y palabras especificas en los arboles de confirmacion, el directorio de trabajo y en el area de preparacion. Para usar [https://www.hostinger.com](https://www.hostinger.com) en todos los archivos, usa:

```bash
git grep "www.hostinger.com"
```

### gitk

Muestra la interfaz grafica para un repositorio local.
Simplemente ejecuta:

```bash
gitk
```

### git instaweb

Te permite explorar tu repositorio local en la interfaz GitWeb.
Por ejemplo:

```bash
git instaweb --http=webrick
```

### git gc

Limpiara archivos innecesarios y optimizara el repositorio local.

```bash
git gc
```

### git archive

Le permite al usuario crear archivos zip y tar que contengan los constituyentes de un solo arbol de repositorio.
Por ejemplo:

```bash
git archive --format=tar master
```

### git prune

Elimina los objetos que no tengan ningun apuntador entrante.

```bash
git prune
```

### git fsck

Realiza una comprobación de integridad del sistema de archivos git e identificar cualquier objeto corrupto

```bash
git fsck
```

### git rebase

Se usa para aplicar ciertos cambios de una rama a otra.
Por ejemplo:

```bash
git rebase master
```