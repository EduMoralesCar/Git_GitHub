## GitHub Actions

### ¿Qué es?
GitHub Actions permite automatizar tareas como pruebas, despliegues y más.

### ¿Cómo crear un workflow?
1. Ve a la pestaña "Actions" y selecciona un template.
2. Crea un archivo `.github/workflows/nombre.yml` con los pasos a seguir.

### Ejemplo básico
```yaml
name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Instalar dependencias
        run: npm install
      - name: Ejecutar pruebas
        run: npm test