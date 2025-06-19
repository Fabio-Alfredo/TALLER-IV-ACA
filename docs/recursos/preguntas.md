# ❓ Preguntas Frecuentes (FAQ)

Respuestas a las dudas más comunes sobre el uso de PupAPI.

---

## 🔐 ¿Cómo me autentico en la API?

Debes enviar tus credenciales al endpoint `/auth/login` y usar el token recibido en la cabecera `Authorization` con el formato:

```
Authorization: Bearer TU_TOKEN
```

Consulta más detalles en la sección [Autenticación](../guia/autenticacion.md).

---

## 🐶 ¿Cómo registro un nuevo perrito?

Utiliza el endpoint `POST /dogs` con un JSON que contenga los datos del perrito:

```json
{
  "name": "Luna",
  "breed": "Beagle",
  "age": 2,
  "vaccinated": true
}
```

---

## 💉 ¿Puedo actualizar la información de una vacuna?

Sí. Usa `PUT /vaccines/{id}` para modificar la información de una vacuna registrada.

---

## 📥 ¿Quién puede crear solicitudes de adopción?

Solo los usuarios autenticados. Debes contar con un token válido para poder hacer una solicitud con `POST /adoptions`.

---

## 📎 ¿Qué formato usan las respuestas?

Todas las respuestas están en formato **JSON**.

---

## ⚠️ ¿Qué hacer si pierdo mi token?

Solo vuelve a autenticarte con tu usuario y clave para obtener uno nuevo. Los tokens son temporales y expiran por seguridad.

---

## 🤔 ¿Puedo probar la API sin estar registrado?

Puedes registrarte con `POST /auth/register`. No hay sandbox público, pero puedes usar los datos de prueba en tu entorno local.

---

## 👨‍💻 ¿Puedo contribuir a este proyecto?

¡Claro que sí! Aunque es un proyecto ficticio, puedes proponer ideas o usarlo como base para tus propios desarrollos.

---

¿Tienes una pregunta que no aparece aquí?  
👉 Contáctanos por correo: **soporte@pupapi.com**
