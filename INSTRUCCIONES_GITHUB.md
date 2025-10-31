# Instrucciones para Subir el Proyecto a GitHub

## Pasos a Seguir:

### 1. Crear un Repositorio en GitHub

1. Ve a [GitHub.com](https://github.com) e inicia sesi�n
2. Haz clic en el bot�n **"+"** en la esquina superior derecha
3. Selecciona **"New repository"**
4. Completa los siguientes campos:
   - **Repository name**: `snackeadospe` (o el nombre que prefieras)
   - **Description**: "Tienda online de bebidas y snacks - SNACKEADOS Per�"
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

# Sube tu c�digo a GitHub
git push -u origin main
```

### 3. Verificar la Conexi�n

Si todo sali� bien, deber�as poder ver tus archivos en el repositorio de GitHub.

## Comandos �tiles para el Futuro:

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
git commit -m "Descripci�n de los cambios"
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

- **Nunca subas archivos sensibles** como contrase�as, claves API, etc.
- El archivo `.gitignore` ya est� configurado para ignorar archivos temporales y del sistema
- Realiza commits frecuentes con mensajes descriptivos
- Antes de hacer push, aseg�rate de que tus cambios funcionan correctamente

## Soluci�n de Problemas:

### Si GitHub te pide autenticaci�n:

Para operaciones b�sicas de Git (push, pull, clone), necesitas crear un **Personal Access Token**:

#### Pasos para crear el token:

1. Ve a GitHub ? **Settings** ? **Developer settings** ? **Personal access tokens** ? **Tokens (classic)**
2. Haz clic en **"Generate new token"** ? **"Generate new token (classic)"**
3. Completa el formulario:
   - **Note**: Dale un nombre descriptivo (ej: "Token para snackeados proyecto")
   - **Expiration**: Elige la duraci�n (30 d�as, 60 d�as, 90 d�as, o sin expiraci�n)
   - **Scopes/Permisos**: Marca las siguientes opciones:
     - ? **`repo`** (Full control of private repositories) - **ES EL M�S IMPORTANTE**
       - Esto incluye permisos para: clone, push, pull, y todas las operaciones de repositorio

4. Haz clic en **"Generate token"** al final de la p�gina
5. **�IMPORTANTE!** Copia el token inmediatamente, ya que GitHub solo lo mostrar� una vez

#### Permisos m�nimos necesarios:

Para uso b�sico de Git con GitHub, necesitas como m�nimo:
- **`repo`**: Control completo de repositorios privados
  - Permite: `push`, `pull`, `clone`, `commit`, `create`, `delete`, y m�s

Si tu repositorio es **p�blico**, algunos permisos adicionales opcionales:
- **`workflow`**: Si usas GitHub Actions (opcional)
- **`read:org`**: Si perteneces a una organizaci�n (opcional)

#### C�mo usar el token:

Cuando Git te pida autenticaci�n:
- **Username**: Tu usuario de GitHub
- **Password**: Pega el **Personal Access Token** (NO tu contrase�a de GitHub)

### Si hay conflictos al hacer pull:
```bash
# Primero guarda tus cambios localmente
git stash

# Descarga los cambios
git pull

# Aplica tus cambios guardados
git stash pop
```

