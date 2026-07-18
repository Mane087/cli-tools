# Buscar una palabra en todo el proyecto
```bash
rg usuario
```

Podría mostrar:
```bash
lib/accounts/user.ex
42:  def get_usuario(id) do

priv/sql/usuarios.sql
18:CREATE TABLE USUARIOS (
```

# Buscar dentro de una ruta específica
```bash
rg IDLOTE ./priv/sql
```

# Buscar en un archivo concreto
```bash
rg IDLOTE ./priv/sql/lotes.sql
```

# Busca en varias rutas
```bash
rg IDLOTE ./lib ./priv/sql ./test
```

# Buscar una frase literal
```bash
rg -F 'user.id'
```

# Ignorar mayúsculas y minúsculas
```bash
rg -i usuario
```

# Forzar coincidencia sensible a mayúsculas
```bash
rg -s Usuario
```

# Buscar una palabra completa
```bash
rg -w status
```

# Buscar una línea completa
```bash
rg -x 'COMMIT;'
```

# Buscar varios patrones
```bash
rg -e ERROR -e WARNING -e FATAL
```

# Mostrar líneas que no coincidan
```bash
rg -v DEBUG app.log
```

# Buscar solo en una extensión
```bash
rg usuario -g '*.ex'
```

# Buscar en varias extensiones
```bash
rg usuario \
  -g '*.ex' \
  -g '*.exs'
```

# Excluir archivos por glob
```bash
rg usuario -g '!*.spec.ts'
```

# Excluir directorios
```bash
rg usuario \
  -g '!node_modules/**' \
  -g '!dist/**' \
  -g '!coverage/**'
```

# Incluir archivos ocultos
```bash
rg --hidden DATABASE_URL
```

# Ignorar .gitignore
```bash
rg -u usuario
```

# Incluir ocultos e ignorados
```bash
rg -uu usuario
```

# Mostrar líneas anteriores y posteriores
```bash
rg -C 2 'IDLOTE'
```

# Mostrar solo archivos con coincidencias
```bash
rg -l IDLOTE
```
