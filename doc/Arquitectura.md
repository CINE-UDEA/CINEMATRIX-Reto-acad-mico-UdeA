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
