🎬 Manual de Usuario – Sistema Cine Cinematrix
📌 Descripción general

El sistema Cinematrix es una aplicación desarrollada en Python y Google Colab para la gestión básica de un cine: registro de usuarios, inicio de sesión, cartelera de películas, compra de entradas y consulta de historial.
El programa guarda datos en archivos JSON para mantener persistencia.

🧩 Características principales

Registro de usuarios

Inicio de sesión

Gestión de cartelera

Compra de entradas

Historial de compras

Manejo de datos en JSON

Validaciones automáticas

Menús interactivos

🚀 Cómo ejecutar el sistema
✔️ 1. Desde Google Colab

Abrir el archivo main.ipynb.

Ejecutar todas las celdas con Runtime → Run all.

El sistema creará carpetas y archivos si no existen.
✔️ 2. Estructura de carpetas recomendada
cinematrix/
 ├── data/
 │     ├── usuarios.json
 │     ├── peliculas.json
 │     ├── funciones.json
 │     └── ventas.json
 ├── utils/
 │     ├── manejo_archivos.py
 │     ├── validaciones.py
 │     └── menus.py
 └── main.ipynb
👤 Registro e inicio de sesión
✔️ Registrar usuario

El sistema solicitará:

Nombre

Correo

Contraseña

Edad (opcional)

Los usuarios se guardan en usuarios.json.

✔️ Iniciar sesión

Ingrese:

Correo

Contraseña

Si coinciden, accede al menú principal.

🎥 Menú principal del usuario

El menú incluye:

1. Ver Cartelera

Muestra título, duración, clasificación y funciones disponibles.

2. Comprar Entradas

Permite:

Seleccionar película

Seleccionar horario

Elegir cantidad de boletos

Confirmar compra

La venta se guarda en ventas.json.

3. Mi Historial

Lista todas las entradas compradas anteriormente.

4. Cerrar Sesión
🛠️ Menú administrativo

Agregar películas

Editar películas

Eliminar películas

Crear funciones

Revisar ventas

🧪 Formato de los archivos JSON
✔️ usuarios.json
{
  "usuarios": [
    {
      "id": 1,
      "nombre": "Ejemplo",
      "correo": "ejemplo@mail.com",
      "password": "123"
    }
  ]
}
✔️ peliculas.json
{
  "peliculas": [
    {
      "id": 1,
      "titulo": "Avatar",
      "duracion": 160,
      "clasificacion": "+7"
    }
  ]
}
✔️ ventas.json
{
  "ventas": [
    {
      "usuario_id": 1,
      "pelicula": "Avatar",
      "cantidad": 2,
      "fecha": "2025-05-20"
    }
  ]
}
| Problema              | Solución                      |
| --------------------- | ----------------------------- |
| No carga JSON         | Revisar que estén en `/data/` |
| Error de rutas        | Usar `os.path.join` en Colab  |
| No encuentra usuario  | Revisar correo y contraseña   |
| No se guardan cambios | Ejecutar celda de archivos    |
