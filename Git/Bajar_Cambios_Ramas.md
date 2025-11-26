# 📘 Guía: Sobrescribir mi rama con otra en Git

Este documento explica cómo hacer que tu rama actual quede **idéntica** a otra rama remota, sobrescribiendo todo el contenido.  
Ejemplo: dejar `morales-dev` igual que `matos-dev`.

---

## 🔹 Paso a paso

1. **Cambiar a tu rama actual**

```bash
git checkout morales-dev
```

2. **Actualizar referencias remotas

```bash
git fetch origin
```

3. **Reset duro contra la rama remota que quieres copiar

```bash
git reset --hard origin/matos-dev
```

4. Subir los cambios a remoto (si quieres que tu rama remota también quede igual)

```bash
git push origin morales-dev --force
```

---

# ⚠️ Advertencias

- El reset --hard y el push --force eliminan tu historial local y lo reemplazan por el de la otra rama.

- Si tienes cambios importantes en tu rama, guárdalos antes con:

```bash
git stash
```
o crea una copia en otra rama:
```bash
git checkout -b backup-morales
```

---

# 🔹 Reutilizar con otras ramas
Si más adelante quieres que morales-dev quede igual que otra rama (ej. macedo-dev), solo cambia el nombre en el paso 3:
```bash
git reset --hard origin/macedo-dev
git push origin morales-dev --force
```
