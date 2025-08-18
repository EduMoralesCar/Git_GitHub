
## Tags en Git

Los tags (etiquetas) en Git se usan para marcar puntos importantes en el historial, como versiones o lanzamientos.

### Tipos de tags
- **Ligero (lightweight):** Solo referencia un commit.
- **Anotado (annotated):** Incluye información extra como mensaje, autor y fecha.

### Crear un tag ligero
```bash
git tag v1.0
```

### Crear un tag anotado
```bash
git tag -a v1.0 -m "Versión 1.0"
```

### Listar todos los tags
```bash
git tag
```

### Ver información de un tag anotado
```bash
git show v1.0
```

### Eliminar un tag
```bash
git tag -d v1.0
```

### Subir los tags al repositorio remoto
```bash
git push origin --tags
```

### Ejemplo práctico
Supón que acabas de terminar una versión estable y quieres marcarla:
```bash
git tag -a v2.0 -m "Versión estable 2.0"
git push origin --tags
```
