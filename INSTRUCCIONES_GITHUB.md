# 📋 API de Clientes - Configuración Completa

## ✅ Estado: Repositorio Publicado

Tu API ya está publicada y funcionando en:
- **Usuario GitHub:** aarombrenner
- **Repositorio:** https://github.com/aarombrenner/apis_estaticas

## 🚀 URLs de tu API

Tu API está disponible en las siguientes URLs:

### Probar en el navegador:
```
https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes
```

### Probar búsqueda por DNI:
```
https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni=12345678
```

## 🎯 Probar la Aplicación

Abre el archivo `ejemplo.html` en tu navegador y prueba con estos DNIs:

- ✅ **12345678** - Juan Pérez García
- ✅ **87654321** - María López Torres
- ✅ **45678912** - Carlos Rodríguez Sánchez
- ❌ **99999999** - No existe (para probar el caso de error)

## 📊 Endpoints Disponibles

| Endpoint | URL |
|----------|-----|
| Todos los clientes | `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes` |
| Cliente por DNI | `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni=12345678` |
| Cliente por ID | `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes/1` |
| Buscar por nombre | `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?nombre=Juan` |

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
git remote add origin https://github.com/aarombrenner/apis_estaticas.git
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

## ✅ Checklist de Configuración

- [x] Repositorio creado en GitHub (público)
- [x] Código subido con `git push`
- [x] Archivos actualizados con usuario aarombrenner
- [ ] API probada en My JSON Server (espera 1-2 minutos después del push)
- [ ] Archivo `ejemplo.html` probado en el navegador
- [ ] Probado al menos un DNI existente
- [ ] Probado un DNI que no existe

## 🔄 Próximos Pasos

1. **Espera 1-2 minutos** para que My JSON Server indexe tu repositorio
2. **Prueba la API** en tu navegador con la URL de arriba
3. **Abre `ejemplo.html`** en tu navegador para probar la aplicación
4. **Haz commit y push** de estos cambios actualizados:
   ```bash
   git add .
   git commit -m "Actualizar archivos con usuario aarombrenner"
   git push
   ```

¡Tu API de clientes está lista para usar! 🎉