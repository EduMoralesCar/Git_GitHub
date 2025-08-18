
## Inicializar un repositorio local

```bash
git init
```

## Configuración de usuario en Git

Antes de empezar a trabajar con Git, es importante configurar tu nombre y correo electrónico. Estos datos se asocian a cada commit que realices.

```bash
git config --global user.name "Tu Nombre"      # Configura tu nombre globalmente
git config --global user.email "tu@email.com"  # Configura tu email globalmente
```

Si quieres configurar el usuario solo para un repositorio específico (no global), omite la opción `--global`:

```bash
git config user.name "Tu Nombre"
git config user.email "tu@email.com"
```

Para verificar la configuración actual:

```bash
git config --list
```

Puedes cambiar otros parámetros, como el editor por defecto:

```bash
git config --global core.editor "code --wait"  # Usa VS Code como editor
```