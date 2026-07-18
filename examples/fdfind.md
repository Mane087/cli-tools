# Buscar por nombre
```bash
fdfind usuario
```

# Buscar por extensión
```bash
fdfind -e sql
```

# Buscar solamente archivos
```bash
fdfind config -t f
```

# Buscar solamente directorios
```bash
fdfind migrations -t d
```

# Incluir ocultos
```bash
fdfind -H '.env'
```

# Incluir ocultos e ignorados
```bash
fdfind -u archivo
```

# Excluir directorios
```bash
fdfind -e ts -E node_modules -E dist
```

# Buscar en toda la ruta
```bash
fdfind -p 'controllers/.*\.ex$'
```

# Ejecutar un comando por archivo
```bash
fdfind -e log -x gzip
```

# Ejecutar un comando con todos los archivos
```bash
fdfind -e ts -X code
```

# Buscar contenido dentro de archivos encontrados
```bash
fdfind -e sql -X rg 'IDLOTE'
```

# Archivos modificados recientemente
```bash
fdfind --changed-within 1d
```

# Archivos grandes
```bash
fdfind -t f --size +100m
```