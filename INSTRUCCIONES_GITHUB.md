# 📋 Instrucciones para Publicar en GitHub

## Paso 1: Crear el Repositorio en GitHub

1. Ve a https://github.com/new
2. Configura el repositorio:
   - **Repository name:** `apis_estaticas`
   - **Description:** API REST falsa para consultar clientes usando My JSON Server
   - **Visibility:** ✅ **Public** (IMPORTANTE: debe ser público para que My JSON Server funcione)
   - ❌ **NO** marques "Add a README file"
   - ❌ **NO** agregues .gitignore
   - ❌ **NO** agregues licencia
3. Haz clic en **"Create repository"**

## Paso 2: Conectar y Subir el Código

Copia y pega estos comandos en tu terminal (reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub):

```bash
git remote add origin https://github.com/TU_USUARIO/apis_estaticas.git
git branch -M main
git push -u origin main
```

### Ejemplo con usuario "juanperez":
```bash
git remote add origin https://github.com/juanperez/apis_estaticas.git
git branch -M main
git push -u origin main
```

## Paso 3: Verificar que Funciona

Después de hacer push, espera 1-2 minutos y prueba tu API:

### Probar en el navegador:
```
https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes
```

### Probar búsqueda por DNI:
```
https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes?dni=12345678
```

## Paso 4: Actualizar el Archivo HTML

1. Abre el archivo `ejemplo.html`
2. Busca la línea que dice:
   ```javascript
   const API_URL = 'https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas';
   ```
3. Reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub
4. Guarda el archivo
5. Haz commit y push de los cambios:
   ```bash
   git add ejemplo.html
   git commit -m "Actualizar URL de la API con usuario correcto"
   git push
   ```

## Paso 5: Probar la Aplicación

Abre el archivo `ejemplo.html` en tu navegador y prueba con estos DNIs:

- ✅ **12345678** - Juan Pérez García
- ✅ **87654321** - María López Torres
- ✅ **45678912** - Carlos Rodríguez Sánchez
- ❌ **99999999** - No existe (para probar el caso de error)

## 🎯 URLs Finales de tu API

Reemplaza `TU_USUARIO` con tu usuario de GitHub:

| Endpoint | URL |
|----------|-----|
| Todos los clientes | `https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes` |
| Cliente por DNI | `https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes?dni=12345678` |
| Cliente por ID | `https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes/1` |
| Buscar por nombre | `https://my-json-server.typicode.com/TU_USUARIO/apis_estaticas/clientes?nombre=Juan` |

## 🔧 Agregar Nuevos Clientes

Para agregar más clientes:

1. Edita el archivo `db.json`
2. Agrega un nuevo objeto en el array `clientes`:
   ```json
   {
     "id": 11,
     "dni": "11223344",
     "nombre": "Nuevo",
     "apellido": "Cliente",
     "email": "nuevo@example.com",
     "celular": "999888777",
     "direccion": "Nueva Dirección 123"
   }
   ```
3. Guarda y haz commit:
   ```bash
   git add db.json
   git commit -m "Agregar nuevo cliente"
   git push
   ```
4. Espera 1-2 minutos para que My JSON Server actualice

## ⚠️ Solución de Problemas

### Error: "remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/TU_USUARIO/apis_estaticas.git
```

### Error: "Permission denied"
Asegúrate de estar autenticado en GitHub. Puedes usar:
- GitHub CLI: `gh auth login`
- Personal Access Token
- SSH keys

### La API no responde
- Verifica que el repositorio sea **público**
- Espera 1-2 minutos después del push
- Verifica que el archivo se llame exactamente `db.json`
- Verifica que esté en la raíz del repositorio

### Error 404 en My JSON Server
- Confirma que tu usuario de GitHub sea correcto
- Confirma que el repositorio se llame `apis_estaticas`
- Verifica que el repositorio sea público

## 📚 Recursos Adicionales

- [My JSON Server](https://my-json-server.typicode.com/)
- [Documentación JSON Server](https://github.com/typicode/json-server)
- [GitHub Docs](https://docs.github.com/)

## ✅ Checklist Final

- [ ] Repositorio creado en GitHub (público)
- [ ] Código subido con `git push`
- [ ] API funcionando en My JSON Server
- [ ] Archivo `ejemplo.html` actualizado con tu usuario
- [ ] Probado al menos un DNI existente
- [ ] Probado un DNI que no existe

¡Listo! Tu API de clientes está funcionando. 🎉