🎬 Manual de Usuario – Sistema Cine Cinematrix
📌 Descripción general

CINEMATRIX es un sistema desarrollado en Python que simula la gestión integral de un cine universitario. Permite el registro de usuarios, inicio de sesión, visualización de cartelera, reserva y cancelación de asientos, compra y cancelación de productos de confitería, así como la consulta de reportes administrativos.
El sistema opera mediante menús interactivos en consola y utiliza archivos JSON para la persistencia de la información.

🧩 Características principales
Registro de usuarios con validaciones automáticas.
Inicio de sesión con control de credenciales.
Visualización de cartelera de películas.
Reserva y cancelación de asientos.
Compra y cancelación de productos de confitería.
Consulta de reservas y compras realizadas.
Menú administrativo con reportes del sistema.
Persistencia de datos mediante archivos JSON.

🚀 Cómo ejecutar el sistema
Abrir el archivo CODIGO_CINEMATRIX.ipynb.

Ejecutar todas las celdas del notebook.

El sistema mostrará el menú principal en consola para iniciar la interacción.

✔️ 2. Estructura de carpetas recomendada
cinematrix/
 ├── CODIGO_CINEMATRIX.ipynb
 └── data/
       ├── usuarios.json
       ├── peliculas.json
       ├── reservas.json
       └── confiteria.json

👤 Registro e inicio de sesión
✔️ Registrar usuario

El sistema solicita:

Nombres

Apellidos

Documento de identidad

Correo institucional (@udea.edu.co)

Tipo de usuario

Contraseña

Validaciones:

Nombres y apellidos sin números.

Documento numérico.

Correo institucional obligatorio.

Contraseña válida definida por el sistema.

Inicio de sesión

El usuario debe ingresar correo y contraseña.
Si las credenciales son correctas, el sistema redirige al menú correspondiente.

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

Menú administrativo

Acceso mediante credenciales especiales.

Funciones disponibles:

Visualizar usuarios registrados.

Consultar reservas realizadas.

Ver ocupación de salas.

Consultar ingresos.

Ver ventas de confitería.

Generar reportes generales.

Credenciales:

Usuario: admin

Contraseña: cine123

🧪 Formato de los archivos JSON
✔️ usuarios.json
{
  "usuarios": [
    {
      "nombres": "Juan",
      "apellidos": "Pérez",
      "documento": "12345678",
      "correo": "juan.perez@udea.edu.co",
      "tipo_usuario": "estudiante",
      "password": "1234"
    }
  ]
}

✔️ películas.json
{
  "peliculas": [
    {
      "id": 1,
      "titulo": "Interestelar",
      "fecha": "2025-05-30",
      "hora": "18:00",
      "sala": 1
    }
  ]
}

✔️ reservas.json
{
  "reservas": [
    {
      "correo_usuario": "juan.perez@udea.edu.co",
      "pelicula": "Interestelar",
      "fecha": "2025-05-30",
      "hora": "18:00",
      "sala": 1,
      "asiento": "F6",
      "estado": "ACTIVA"
    }
  ]
}

✔️ confiteria.json
{
  "compras": [
    {
      "correo_usuario": "juan.perez@udea.edu.co",
      "producto": "Combo 1",
      "precio": 15000,
      "fecha": "2025-05-30",
      "estado": "ACTIVA"
    }
  ]
}

| Problema             | Posible causa                     | Solución                            |
| -------------------- | --------------------------------- | ----------------------------------- |
| No inicia el sistema | No se ejecutaron todas las celdas | Ejecutar todo el notebook           |
| Error en login       | Credenciales incorrectas          | Verificar correo y contraseña       |
| No guarda reservas   | Archivos JSON inexistentes        | Ejecutar el sistema para generarlos |
| Asiento ocupado      | Ya fue reservado                  | Seleccionar otro asiento            |

Screenshots
doc/screenshots/

Soporte

Proyecto académico: CINEMATRIX
Lenguaje: Python
Entorno: Google Colab

📄 doc/Instalacion.md
Instalación del Sistema CINEMATRIX

Requisitos
Python 3 o Google Colab
Archivo CODIGO_CINEMATRIX.ipynb
Consola habilitada
Instalación del sistema Cinematrix
Abrir Google Colab.
Cargar el archivo CODIGO_CINEMATRIX.ipynb.
Ejecutar todas las celdas.
El sistema creará los archivos JSON si no existen.

Estructura recomendada
cinematrix/
 ├── CODIGO_CINEMATRIX.ipynb
 └── data/

Notas
No modificar manualmente los archivos JSON.
Mantener la estructura de carpetas.
Usar siempre correos institucionales para registro.

📄 doc/Arquitectura.md
Arquitectura del Sistema CINEMATRIX

Tipo de arquitectura
El sistema utiliza una arquitectura monolítica modular, organizada mediante funciones que separan la lógica del sistema.

Módulos principales
Usuarios: registro, validación e inicio de sesión.
Cartelera: gestión de películas y funciones.
Reservas: control de asientos y facturación.
Confitería: compras y cancelaciones.
Administrador: reportes y estadísticas.

Estructura de datos
Los datos se almacenan en archivos JSON:
usuarios.json
peliculas.json
reservas.json
confiteria.json

Flujo del sistema
Inicio
 ├── Registro
 ├── Login
 │    ├── Menú Usuario
 │    └── Menú Administrador
 └── Salida

📄 doc/API.md
Documentación API – CINEMATRIX

Registro de usuario
Función encargada de validar y almacenar nuevos usuarios.

Inicio de sesión
Verifica credenciales y determina el tipo de usuario.

Gestión de cartelera
Permite visualizar películas, fechas, horarios y salas.

Reservas
Crear reservas.
Cancelar reservas.
Validar asientos disponibles.

Confitería
Comprar productos.
Cancelar compras.
Consultar historial.

Administración
Listar usuarios.
Consultar ventas.
Ver ocupación e ingresos.
