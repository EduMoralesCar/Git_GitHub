
## Bajar cambios de otra rama a tu rama actual

Cuando trabajas en una rama y quieres traer los cambios de la rama principal (`main`) o de otra rama específica, puedes hacerlo de varias formas:

### 1. Usar git pull para traer cambios del remoto
Si tu rama principal es `main`:
```bash
git pull origin main
```
Esto trae los cambios de la rama `main` del repositorio remoto y los fusiona en tu rama actual.

### 2. Usar git fetch y luego merge
Primero descarga los cambios:
```bash
git fetch origin
```
Luego fusiona la rama deseada en tu rama actual:
```bash
git merge origin/main
```
O para otra rama:
```bash
git merge origin/otra-rama
```

### 3. Usar rebase para un historial más limpio
Puedes reescribir el historial de tu rama actual para que esté encima de los últimos cambios de la rama principal:
```bash
git fetch origin
git rebase origin/main
```

### Recomendación
Si hay conflictos, resuélvelos manualmente y luego continúa con el merge o rebase.
