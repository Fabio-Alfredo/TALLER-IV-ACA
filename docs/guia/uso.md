# 🧪 Ejemplos de Uso

A continuación se muestran ejemplos de cómo interactuar con la API de PupAPI utilizando diferentes lenguajes y herramientas.

---

## 📡 Petición con `fetch` en JavaScript

```js
fetch('https://api.pupapi.com/v1/dogs', {
  method: 'GET',
  headers: {
    'Authorization': 'Bearer TU_TOKEN_AQUI'
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

---

## 🔐 Enviar credenciales con `curl`

```bash
curl -X POST https://api.pupapi.com/v1/auth/login \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "usuario=demo&clave=1234"
```

---

## 🐾 Crear un nuevo perrito con `axios`

```js
import axios from 'axios';

const nuevoPerrito = {
  name: 'Firulais',
  breed: 'Labrador',
  age: 4,
  vaccinated: true
};

axios.post('https://api.pupapi.com/v1/dogs', nuevoPerrito, {
  headers: {
    'Authorization': 'Bearer TU_TOKEN_AQUI'
  }
})
.then(response => console.log('Registrado:', response.data))
.catch(error => console.error('Error:', error));
```

---

## 🧪 Prueba rápida en Node.js

```js
console.log('🐶 Bienvenido a PupAPI');
```

---

> ✅ Todos los bloques de código aquí incluyen el botón de "copiar" automáticamente cuando se usa MkDocs con el tema Material.

