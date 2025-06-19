# 📚 Endpoints de PupAPI

A continuación se detallan los principales endpoints disponibles en la API.

---

## 🐶 Perritos

| Método | Endpoint        | Descripción                          | Autenticación |
|--------|------------------|--------------------------------------|----------------|
| GET    | `/dogs`          | Lista todos los perritos             | ✅             |
| GET    | `/dogs/{id}`     | Obtiene un perrito por su ID         | ✅             |
| POST   | `/dogs`          | Crea un nuevo perrito                | ✅             |
| PUT    | `/dogs/{id}`     | Actualiza los datos de un perrito    | ✅             |
| DELETE | `/dogs/{id}`     | Elimina un perrito                   | ✅             |

---

## ❤️ Adopciones

| Método | Endpoint            | Descripción                                 | Autenticación |
|--------|----------------------|---------------------------------------------|----------------|
| GET    | `/adoptions`         | Lista todas las solicitudes de adopción     | ✅             |
| POST   | `/adoptions`         | Crea una nueva solicitud de adopción        | ✅             |

---

## 💉 Vacunas

| Método | Endpoint           | Descripción                         | Autenticación |
|--------|---------------------|-------------------------------------|----------------|
| GET    | `/vaccines`         | Lista todas las vacunas registradas | ✅             |
| POST   | `/vaccines`         | Registra una nueva vacuna           | ✅             |
| PUT    | `/vaccines/{id}`    | Actualiza los datos de una vacuna   | ✅             |

---

## 👤 Usuarios

| Método | Endpoint         | Descripción                           | Autenticación |
|--------|-------------------|---------------------------------------|----------------|
| POST   | `/auth/register`  | Registro de un nuevo usuario          | ❌             |
| POST   | `/auth/login`     | Inicio de sesión y generación de JWT  | ❌             |

---

✅: Requiere token JWT en la cabecera `Authorization: Bearer <token>`.  
❌: No requiere autenticación.

