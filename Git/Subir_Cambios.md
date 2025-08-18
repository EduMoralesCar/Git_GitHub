
## Subir un proyecto local a GitHub con Git

### 1. Crear un repositorio en GitHub

Ve a [github.com](https://github.com/) y crea un nuevo repositorio. No es necesario inicializarlo con README ni .gitignore.

### 2. Inicializar el repositorio local (si no lo has hecho)
```bash
git init
```

### 3. Agregar los archivos al área de preparación
```bash
git add archivo.txt   # Agrega un archivo específico
git add .             # Agrega todos los archivos
```

### 4. Realizar el primer commit
```bash
git commit -m "Primer commit"
```

### 5. Agregar el repositorio remoto
Reemplaza `URL-del-repositorio` por la URL que te da GitHub (HTTPS o SSH):
```bash
git remote add origin URL-del-repositorio
```

### 6. Subir los cambios al repositorio remoto
Para la primera subida, usa:
```bash
git push -u origin master
```
O si tu rama principal se llama `main`:
```bash
git push -u origin main
```

### 7. Subir cambios posteriores
Para subir nuevos commits:
```bash
git push
```
## 8. Ver historial de commits

```bash
git log
```

## 9. Ver diferencias entre archivos

```bash
git diff
```