# API de Clientes - My JSON Server

Este proyecto contiene una API REST falsa para consultar información de clientes usando My JSON Server.

## 🚀 URL de la API

Una vez que subas este repositorio a GitHub, tu API estará disponible en:

```
https://my-json-server.typicode.com/aarombrenner/apis_estaticas
```

## 📋 Endpoints Disponibles

### 1. Obtener todos los clientes
```
GET https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes
```

### 2. Buscar cliente por DNI
```
GET https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni=12345678
```

### 3. Obtener cliente por ID
```
GET https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes/1
```

### 4. Buscar por nombre
```
GET https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?nombre=Juan
```

### 5. Buscar por apellido
```
GET https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?apellido=Pérez
```

## 🔍 Ejemplos de Uso

### JavaScript / Fetch API

```javascript
// Validar si un DNI existe
async function validarCliente(dni) {
  const response = await fetch(
    `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni=${dni}`
  );
  const clientes = await response.json();
  
  if (clientes.length > 0) {
    console.log('✅ Cliente encontrado:', clientes[0]);
    return clientes[0];
  } else {
    console.log('❌ Cliente no registrado');
    return null;
  }
}

// Uso
validarCliente('12345678');
```

### cURL

```bash
# Buscar por DNI
curl "https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni=12345678"

# Obtener todos los clientes
curl "https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes"
```

### Python

```python
import requests

def validar_cliente(dni):
    url = f"https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes?dni={dni}"
    response = requests.get(url)
    clientes = response.json()
    
    if len(clientes) > 0:
        print(f"✅ Cliente encontrado: {clientes[0]}")
        return clientes[0]
    else:
        print("❌ Cliente no registrado")
        return None

# Uso
validar_cliente('12345678')
```

## 📊 Estructura de Datos

Cada cliente tiene los siguientes campos:

```json
{
  "id": 1,
  "dni": "12345678",
  "nombre": "Juan",
  "apellido": "Pérez García",
  "email": "juan.perez@example.com",
  "celular": "987654321",
  "direccion": "Av. Arequipa 1234, Lima"
}
```

## 🎯 Clientes de Prueba

El archivo `db.json` incluye 10 clientes de ejemplo con los siguientes DNIs:

- 12345678 - Juan Pérez García
- 87654321 - María López Torres
- 45678912 - Carlos Rodríguez Sánchez
- 78912345 - Ana Martínez Flores
- 32165498 - Luis Fernández Díaz
- 65498732 - Patricia Gómez Ruiz
- 98765432 - Roberto Silva Vargas
- 15975348 - Carmen Ramos Castro
- 75315928 - Jorge Mendoza Quispe
- 35795124 - Rosa Huamán Pérez

## 📝 Pasos para Publicar en GitHub

1. **Inicializar Git** (si no lo has hecho):
   ```bash
   git init
   ```

2. **Agregar archivos**:
   ```bash
   git add .
   git commit -m "Initial commit: API de clientes"
   ```

3. **Crear repositorio en GitHub**:
   - Ve a https://github.com/new
   - Nombre del repositorio: `apis_estaticas`
   - Hazlo público
   - No inicialices con README (ya lo tienes)

4. **Conectar y subir**:
   ```bash
   git remote add origin https://github.com/aarombrenner/apis_estaticas.git
   git branch -M main
   git push -u origin main
   ```

5. **Probar tu API**:
   - Espera 1-2 minutos
   - Accede a: `https://my-json-server.typicode.com/aarombrenner/apis_estaticas/clientes`

## ⚙️ Características de My JSON Server

✅ **Filtrado**: Buscar por cualquier campo  
✅ **Paginación**: `?_limit=5&_page=2`  
✅ **Ordenamiento**: `?_sort=nombre&_order=asc`  
✅ **Búsqueda**: `?q=juan` (busca en todos los campos)  

## ⚠️ Limitaciones

- Solo operaciones de **lectura (GET)**
- No soporta POST, PUT, DELETE
- Los datos son estáticos (no se pueden modificar vía API)
- Para agregar/modificar clientes, edita `db.json` y haz push a GitHub

## 🔄 Agregar Nuevos Clientes

Para agregar nuevos clientes:

1. Edita el archivo `db.json`
2. Agrega un nuevo objeto en el array `clientes`
3. Asegúrate de que el `id` sea único
4. Haz commit y push a GitHub
5. Los cambios estarán disponibles en 1-2 minutos

Ejemplo:
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

## 📚 Recursos

- [My JSON Server](https://my-json-server.typicode.com/)
- [Documentación JSON Server](https://github.com/typicode/json-server)

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la licencia MIT.