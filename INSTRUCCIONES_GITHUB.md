# Instrucciones para Subir el Proyecto a GitHub

## Pasos a Seguir:

### 1. Crear un Repositorio en GitHub

1. Ve a [GitHub.com](https://github.com) e inicia sesión
2. Haz clic en el botón **"+"** en la esquina superior derecha
3. Selecciona **"New repository"**
4. Completa los siguientes campos:
   - **Repository name**: `snackeadospe` (o el nombre que prefieras)
   - **Description**: "Tienda online de bebidas y snacks - SNACKEADOS Perú"
   - **Visibilidad**: Elige **Public** o **Private**
   - ?? **NO marques** las opciones "Initialize this repository with a README", "Add .gitignore", o "Choose a license"
5. Haz clic en **"Create repository"**

### 2. Conectar tu Repositorio Local con GitHub

Una vez creado el repositorio en GitHub, ejecuta estos comandos en la terminal:

```bash
# Agrega el repositorio remoto (reemplaza TU_USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/snackeados.git

# Cambia la rama principal a 'main' (si no lo has hecho)
git branch -M main

# Sube tu código a GitHub
git push -u origin main
```

### 3. Verificar la Conexión

Si todo salió bien, deberías poder ver tus archivos en el repositorio de GitHub.

## Comandos Útiles para el Futuro:

### Ver el estado de tus archivos:
```bash
git status
```

### Agregar cambios:
```bash
git add .
```

### Crear un commit:
```bash
git commit -m "Descripción de los cambios"
```

### Subir cambios a GitHub:
```bash
git push
```

### Ver el historial de commits:
```bash
git log
```

### Descargar cambios desde GitHub:
```bash
git pull
```

## Notas Importantes:

- **Nunca subas archivos sensibles** como contraseñas, claves API, etc.
- El archivo `.gitignore` ya está configurado para ignorar archivos temporales y del sistema
- Realiza commits frecuentes con mensajes descriptivos
- Antes de hacer push, asegúrate de que tus cambios funcionan correctamente

## Solución de Problemas:

### Si GitHub te pide autenticación:
- Usa un **Personal Access Token** en lugar de tu contraseña
- Ve a GitHub ? Settings ? Developer settings ? Personal access tokens ? Generate new token
- Usa ese token como contraseña cuando Git te lo pida

### Si hay conflictos al hacer pull:
```bash
# Primero guarda tus cambios localmente
git stash

# Descarga los cambios
git pull

# Aplica tus cambios guardados
git stash pop
```

