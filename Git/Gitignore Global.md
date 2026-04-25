El `.gitignore` global es un archivo en tu home (`~`) que Git aplica a **todos tus repositorios** automáticamente, sin necesidad de tocarlo en cada proyecto.

Se configura así:

bash

```bash
git config --global core.excludesfile ~/.gitignore_global
```

**Qué va ahí:** solo cosas generadas por **tu sistema o tus herramientas**, no por el proyecto en sí.

- `.DS_Store` — carpetas del Finder en macOS
- `Thumbs.db` — miniaturas de Windows
- `.idea/` — configuración de JetBrains (PyCharm, etc.)
- `.vscode/` — configuración local de VS Code
- `*.log` — archivos de log genéricos
- `__pycache__/` — caché de Python
- `*.pyc` — bytecode de Python
- `.env` — variables de entorno locales

**Qué NO va ahí:** dependencias, builds, o archivos específicos del proyecto (eso va en el `.gitignore` de cada repo, para que todos los colaboradores lo compartan).

```zsh
echo ".DS_Store" >> ~/.gitignore_global
```