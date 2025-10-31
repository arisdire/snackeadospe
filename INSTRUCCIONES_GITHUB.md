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

Para operaciones básicas de Git (push, pull, clone), necesitas crear un **Personal Access Token**:

#### Pasos para crear el token:

1. Ve a GitHub ? **Settings** ? **Developer settings** ? **Personal access tokens** ? **Tokens (classic)**
2. Haz clic en **"Generate new token"** ? **"Generate new token (classic)"**
3. Completa el formulario:
   - **Note**: Dale un nombre descriptivo (ej: "Token para snackeados proyecto")
   - **Expiration**: Elige la duración (30 días, 60 días, 90 días, o sin expiración)
   - **Scopes/Permisos**: Marca las siguientes opciones:
     - ? **`repo`** (Full control of private repositories) - **ES EL MÁS IMPORTANTE**
       - Esto incluye permisos para: clone, push, pull, y todas las operaciones de repositorio

4. Haz clic en **"Generate token"** al final de la página
5. **¡IMPORTANTE!** Copia el token inmediatamente, ya que GitHub solo lo mostrará una vez

#### Permisos mínimos necesarios:

Para uso básico de Git con GitHub, necesitas como mínimo:
- **`repo`**: Control completo de repositorios privados
  - Permite: `push`, `pull`, `clone`, `commit`, `create`, `delete`, y más

Si tu repositorio es **público**, algunos permisos adicionales opcionales:
- **`workflow`**: Si usas GitHub Actions (opcional)
- **`read:org`**: Si perteneces a una organización (opcional)

#### Cómo usar el token:

Cuando Git te pida autenticación:
- **Username**: Tu usuario de GitHub
- **Password**: Pega el **Personal Access Token** (NO tu contraseña de GitHub)

### Si hay conflictos al hacer pull:
```bash
# Primero guarda tus cambios localmente
git stash

# Descarga los cambios
git pull

# Aplica tus cambios guardados
git stash pop
```

