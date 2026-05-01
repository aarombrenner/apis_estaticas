# 🌐 Configuración de GitHub Pages

## ✅ Archivos Creados

Se han creado los siguientes archivos para GitHub Pages:

1. **`index.html`** - Página principal con Swagger UI interactivo
2. **`swagger.yaml`** - Especificación OpenAPI 3.0 de la API
3. **`_config.yml`** - Configuración de GitHub Pages

## 📋 Pasos para Activar GitHub Pages

### 1. Subir los Archivos a GitHub

Primero, haz commit y push de los nuevos archivos:

```bash
git add .
git commit -m "Agregar documentación Swagger y configurar GitHub Pages"
git push
```

### 2. Activar GitHub Pages en tu Repositorio

1. Ve a tu repositorio: https://github.com/aarombrenner/apis_estaticas
2. Haz clic en **Settings** (Configuración)
3. En el menú lateral izquierdo, busca **Pages**
4. En la sección **Source** (Fuente):
   - Selecciona **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**
5. Haz clic en **Save**

### 3. Esperar el Despliegue

GitHub Pages tardará 1-3 minutos en construir y desplegar tu sitio.

Verás un mensaje como:
```
✅ Your site is live at https://aarombrenner.github.io/apis_estaticas/
```

## 🎯 URLs Resultantes

Una vez activado GitHub Pages, tendrás acceso a:

### Documentación Interactiva (Swagger UI)
```
https://aarombrenner.github.io/apis_estaticas/
```

### Archivo OpenAPI para BAW
```
https://aarombrenner.github.io/apis_estaticas/swagger.yaml
```

### Demo de Validación de Clientes
```
https://aarombrenner.github.io/apis_estaticas/ejemplo.html
```

## 🔧 Usar en BAW (IBM Business Automation Workflow)

### Opción 1: Importar desde URL

En BAW, cuando te pida la URL del servicio OpenAPI, usa:

```
https://aarombrenner.github.io/apis_estaticas/swagger.yaml
```

**Ventajas:**
- ✅ Certificado SSL válido (GitHub)
- ✅ No requiere configuración de truststore
- ✅ Actualización automática cuando cambies el swagger.yaml

### Opción 2: Descargar e Importar Manualmente

1. Descarga el archivo: https://aarombrenner.github.io/apis_estaticas/swagger.yaml
2. En BAW, importa el archivo directamente

## 📊 Verificar que Funciona

### Probar el Swagger UI

1. Abre: https://aarombrenner.github.io/apis_estaticas/
2. Deberías ver la documentación interactiva de tu API
3. Puedes probar los endpoints directamente desde la interfaz

### Probar el Archivo YAML

1. Abre: https://aarombrenner.github.io/apis_estaticas/swagger.yaml
2. Deberías ver el contenido del archivo OpenAPI en formato YAML

### Probar en BAW

1. En BAW, agrega un nuevo servicio externo
2. Usa la URL: `https://aarombrenner.github.io/apis_estaticas/swagger.yaml`
3. BAW debería importar correctamente la especificación OpenAPI

## 🔄 Actualizar la Documentación

Cuando necesites actualizar el Swagger:

1. Edita el archivo `swagger.yaml`
2. Haz commit y push:
   ```bash
   git add swagger.yaml
   git commit -m "Actualizar documentación API"
   git push
   ```
3. GitHub Pages se actualizará automáticamente en 1-3 minutos

## ⚠️ Solución de Problemas

### GitHub Pages no se activa

- Verifica que el repositorio sea **público**
- Asegúrate de haber hecho push de todos los archivos
- Espera 5 minutos y refresca la página

### Error 404 en las URLs

- Verifica que GitHub Pages esté activado
- Confirma que los archivos estén en la rama `main`
- Espera unos minutos después de activar Pages

### BAW no puede leer el archivo

- Verifica que la URL sea exactamente: `https://aarombrenner.github.io/apis_estaticas/swagger.yaml`
- Prueba abrir la URL en tu navegador primero
- Asegúrate de que GitHub Pages esté completamente desplegado

### Cambios no se reflejan

- GitHub Pages puede tardar hasta 5 minutos en actualizar
- Limpia la caché de tu navegador (Ctrl+F5 o Cmd+Shift+R)
- Verifica que hayas hecho push de los cambios

## 📚 Recursos

- [Documentación GitHub Pages](https://docs.github.com/en/pages)
- [OpenAPI Specification](https://swagger.io/specification/)
- [Swagger UI](https://swagger.io/tools/swagger-ui/)

## ✅ Checklist

- [ ] Archivos subidos a GitHub (`git push`)
- [ ] GitHub Pages activado en Settings
- [ ] Sitio desplegado (verificar URL)
- [ ] Swagger UI funciona correctamente
- [ ] Archivo swagger.yaml accesible
- [ ] URL probada en BAW
- [ ] Servicio importado exitosamente en BAW

¡Tu documentación API está lista para usar! 🎉