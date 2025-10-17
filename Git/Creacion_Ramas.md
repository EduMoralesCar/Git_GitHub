# 🌿 Ramas en Git
Las ramas permiten trabajar en diferentes versiones del proyecto de forma independiente.

# Ver ramas existentes
Muestra todas las ramas locales. Para ver también las remotas:

```bash
git branch              # Muestra ramas locales
git branch -a           # Muestra ramas locales y remotas
git branch -r           # Muestra solo ramas remotas
```
# Crear una nueva rama
```
git branch nombre-rama  # Crea una rama local llamada 'nombre-rama'
```
# Cambiar de rama
```
git switch nombre-rama          # Cambia a una rama local
git checkout nombre-rama        # Alternativa clásica para cambiar de rama
```

# Cambiar a una rama remota que aún no existe localmente
```
git fetch origin
git switch -c nombre-rama origin/nombre-rama
```

# Fusionar ramas
```
git merge nombre-rama   # Fusiona 'nombre-rama' en la rama actual
```

# Eliminar ramas
```
git branch -d nombre-rama              # Elimina una rama local
git push origin --delete nombre-rama   # Elimina una rama remota
```

# 🌐 Repositorio remoto
```
git remote -v       # Ver remotos configurados
git clone URL       # Clonar repositorio desde GitHub
git push            # Subir cambios al remoto
git pull            # Descargar y fusionar cambios del remoto
```

# 🆘 Ayuda de comandos
```
git help            # Acceder a la documentación de Git
```
