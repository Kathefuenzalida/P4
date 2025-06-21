# 📚 Proyecto 4: API de Reservas Hoteleras

Este proyecto consiste en el desarrollo de una API RESTful utilizando Node.js y Express para la gestión de reservas en hoteles. La API permite realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar), además de varios filtros para buscar reservas por distintos criterios.


# Tecnologías utilizadas

- Node.js  
- Express  
- Nodemon (para desarrollo)  
- JavaScript

# 📁 Estructura del proyecto

reservas-api/
│
├── controllers/
│ └── reservasController.js // Lógica de negocio para las reservas
├── routes/
│ └── reservasRoutes.js // Definición de las rutas de la API
├── server.js // Punto de entrada de la aplicación
├── .env // Variables de entorno (puerto, etc.)
├── .gitignore // Ignorar node_modules, .env, etc.
├── package.json
└── README.md

## 🔌 Instalación y ejecución

1. Clonar el repositorio  
En bash:
git clone https://github.com/tu-usuario/reservas-api.git
Instalar dependencias

bash
Copiar código
npm install
Ejecutar el servidor

bash
Copiar código
npm run start
Por defecto, la API se ejecuta en:
📍 http://localhost:3000

📬 Endpoints disponibles
📍 Crear reserva
POST /api/reservas

Body (JSON):

json
Copiar código
{
  "hotel": "Hotel Paraíso",
  "tipo_habitacion": "doble",
  "num_huespedes": 2,
  "fecha": "2023-05-20",
  "estado": "confirmada"
}
📍 Obtener todas las reservas
GET /api/reservas

📍 Obtener una reserva por ID
GET /api/reservas/:id

📍 Actualizar una reserva
PUT /api/reservas/:id

Body (JSON):

json
Copiar código
{
  "estado": "pendiente"
}
📍 Eliminar una reserva
DELETE /api/reservas/:id

🔍 Filtros disponibles (todos por GET en /api/reservas)
?hotel=Hotel Paraíso

?estado=pendiente

?tipo_habitacion=doble

?num_huespedes=3

?fecha_inicio=2023-05-01&fecha_fin=2023-05-31

🧪 Herramientas para probar
Puedes usar herramientas como Postman, Insomnia o Thunder Client (VS Code) para realizar peticiones a la API.

✍️ Autora
Proyecto realizado por Katherine Fuenzalida como parte del Bootcamp Fullstack 2025.
👩‍💻 Ingeniera Civil Industrial y Product Owner.

📝 Notas
Los datos se almacenan en memoria, por lo que se reinician al apagar el servidor.

Este proyecto puede escalar fácilmente conectándolo a una base de datos como MongoDB.