# 🔐 Autenticación

PupAPI utiliza **JSON Web Tokens (JWT)** para proteger sus endpoints. Antes de acceder a cualquier recurso privado, debes autenticarte y obtener un token de acceso.

## 🔑 Obtener un Token

Envía una solicitud `POST` con tus credenciales al endpoint `/auth/login`:

```bash
curl -X POST https://api.pupapi.com/v1/auth/login \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "usuario=demo&clave=1234"
```

Si las credenciales son correctas, recibirás una respuesta como esta:

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "expires_in": 3600
}
```

## 🔐 Usar el Token

Una vez recibido el token, debes incluirlo en la cabecera `Authorization` para todas las peticiones protegidas:

```bash
curl -X GET https://api.pupapi.com/v1/dogs \
     -H "Authorization: Bearer TU_TOKEN_AQUI"
```

!!! tip "Consejo"
    Puedes guardar el token en tu cliente HTTP favorito (como Postman) para facilitar pruebas.

!!! note "¿Cómo se crean los tokens?"
    Los tokens se generan utilizando una clave secreta y contienen la información del usuario, como su ID y rol. Esto permite validar su identidad sin almacenar sesiones en el servidor.

!!! warning "Advertencia"
    Nunca compartas tu token ni lo incluyas en repositorios públicos. Si crees que fue comprometido, solicita uno nuevo.

## 🚫 Token Expirado

Si recibes un error como este:

```json
{
  "error": "Token expirado o inválido"
}
```

Deberás volver a autenticarte para obtener un nuevo token válido.
