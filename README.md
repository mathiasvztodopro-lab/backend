# backend

TAREA_SENATI

## Despliegue de la aplicación

### 1. Alojar el frontend

El frontend suele estar compuesto por archivos estáticos como HTML, CSS y JavaScript y se ejecuta en el navegador del usuario.

Opciones recomendadas:

- Gratis: Netlify o Render.
- De pago: Hostinger, si necesitas un dominio personalizado y un panel de control tradicional.

### 2. Alojar el backend

El backend procesa la lógica de negocio, gestiona la base de datos y se ejecuta en un servidor remoto.

Opciones recomendadas:

- Gratis o barato: Render.
- Alternativas: Railway.app y Fly.io para desplegar APIs hechas con Node.js, Python o Java.

### 3. Conectar frontend y backend

Al desplegar ambas partes, el frontend no debe apuntar a `localhost`, sino a la URL pública del backend.

Recomendaciones:

- Cambia la variable de entorno o constante de conexión, por ejemplo `API_URL`.
- Usa la URL de producción del backend en lugar de una dirección local.
- Configura CORS en el backend para permitir peticiones desde el dominio del frontend.

### 4. Configurar la base de datos

Si el backend usa una base de datos, tienes dos opciones:

- Base de datos en la nube: MongoDB Atlas o Supabase.
- Base de datos propia: PostgreSQL o MySQL instalados en tu servidor, asegurando que el firewall permita conexiones remotas y que las variables de conexión estén actualizadas.

## Resumen rápido

1. Sube el frontend a un hosting estático.
2. Despliega el backend en un servidor público.
3. Actualiza la URL de la API en el frontend.
4. Habilita CORS en el backend.
5. Conecta la base de datos correcta para producción.
