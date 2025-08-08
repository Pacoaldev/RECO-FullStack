# RECO - Gestión de Eventos

![RECO Logo](https://img.shields.io/badge/RECO-Event%20Manager-blue)
![React Native](https://img.shields.io/badge/React%20Native-0.72-61DAFB?logo=react)
![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?logo=mongodb)

## 📱 Descripción

RECO es una aplicación full-stack multiplataforma para la gestión integral de eventos. Combina un backend escalable con Node.js, una base de datos NoSQL en la nube y una interfaz móvil intuitiva desarrollada en React Native.

### ✨ Características principales
- 🔐 **Autenticación segura** con JWT
- 📅 **CRUD completo** de eventos
- 🌍 **Despliegue en la nube** con CI/CD
- 📱 **App móvil multiplataforma** (Android/iOS)
- 🔄 **Comunicación en tiempo real** con API REST

## 🚀 Demo

- **Backend API**: [https://reco-api.render.com](https://reco-api.render.com)
- **APK Android**: [Descargar última versión](https://github.com/tu-usuario/reco/releases)

## 🛠️ Stack Tecnológico

### Frontend (React Native)
```
React Native + Expo
├── React Navigation (navegación)
├── Axios (HTTP client)
├── AsyncStorage (persistencia local)
├── Formik + Yup (formularios)
└── EAS Build (distribución)
```

### Backend (Node.js)
```
Express.js API
├── Mongoose (MongoDB ODM)
├── JWT (autenticación)
├── Bcrypt (encriptación)
├── CORS (seguridad)
└── Render.com (hosting)
```

### Base de Datos
- **MongoDB Atlas** - Base de datos NoSQL en la nube

## 📋 Funcionalidades

### Autenticación
- [x] Registro de usuarios
- [x] Inicio de sesión
- [x] Tokens JWT persistentes
- [x] Middleware de autenticación

### Gestión de Eventos
- [x] **Crear** nuevos eventos
- [x] **Leer** lista de eventos del usuario
- [x] **Actualizar** detalles de eventos
- [x] **Eliminar** eventos
- [x] Validación de formularios
- [x] Manejo de errores

## 🏗️ Arquitectura

```
┌─────────────────┐    HTTP/REST    ┌──────────────────┐
│                 │ ──────────────> │                  │
│  React Native   │                 │   Express.js     │
│     Client      │ <────────────── │      API         │
│                 │                 │                  │
└─────────────────┘                 └──────────────────┘
                                              │
                                              │ Mongoose
                                              ▼
                                    ┌──────────────────┐
                                    │   MongoDB Atlas  │
                                    │   (Database)     │
                                    └──────────────────┘
```

## 🚀 Instalación y Uso

### Prerrequisitos
- Node.js 18+
- Expo CLI
- MongoDB Atlas cuenta
- Android Studio / Xcode (opcional)

### 1. Backend
```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/reco.git
cd reco/backend

# Instalar dependencias
npm install

# Configurar variables de entorno
cp .env.example .env
# Editar .env con tu MONGODB_URI y JWT_SECRET

# Ejecutar en desarrollo
npm run dev
```

### 2. Frontend
```bash
cd ../frontend

# Instalar dependencias
npm install

# Configurar API endpoint
# Editar config/api.js con tu URL del backend

# Ejecutar en desarrollo
npm start

# Construir APK
eas build --platform android
```

## 📁 Estructura del Proyecto

```
reco/
├── backend/
│   ├── controllers/     # Lógica de negocio
│   ├── models/         # Esquemas de MongoDB
│   ├── middleware/     # Autenticación y validación
│   ├── routes/         # Endpoints de la API
│   └── server.js       # Punto de entrada
├── frontend/
│   ├── components/     # Componentes reutilizables
│   ├── screens/        # Pantallas de la app
│   ├── navigation/     # Configuración de navegación
│   ├── services/       # Llamadas a la API
│   └── App.js          # Componente principal
└── README.md
```

## 🔧 Scripts Disponibles

### Backend
- `npm start` - Producción
- `npm run dev` - Desarrollo con nodemon
- `npm test` - Ejecutar tests

### Frontend
- `npm start` - Servidor de desarrollo Expo
- `eas build` - Construir para producción
- `eas submit` - Publicar en stores

## 🌐 API Endpoints

### Autenticación
```http
POST /api/auth/register    # Registro de usuario
POST /api/auth/login       # Inicio de sesión
GET  /api/auth/profile     # Perfil del usuario
```

### Eventos
```http
GET    /api/events         # Listar eventos del usuario
POST   /api/events         # Crear nuevo evento
PUT    /api/events/:id     # Actualizar evento
DELETE /api/events/:id     # Eliminar evento
```

## 🔒 Seguridad

- ✅ Passwords hasheadas con bcrypt
- ✅ Autenticación JWT
- ✅ Validación de datos de entrada
- ✅ CORS configurado
- ✅ Variables de entorno para secretos

## 🚀 Despliegue

### Backend (Render.com)
1. Conectar repositorio de GitHub
2. Configurar variables de entorno
3. Despliegue automático en push a main

### Frontend (EAS Build)
1. Configurar `eas.json`
2. `eas build --platform android`
3. Descargar APK generado

## 🎯 Próximas Funcionalidades

- [ ] Notificaciones push
- [ ] Compartir eventos
- [ ] Calendario integrado
- [ ] Modo offline
- [ ] Tests automatizados
- [ ] Versión web (React.js)

## 🤝 Contribuir

1. Fork del proyecto
2. Crear rama feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abrir Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**Paco López**
- GitHub: [@Fralopala2](https://github.com/Fralopala2)
- LinkedIn: [Perfil](www.linkedin.com/in/fmlalinked)
- Email: pacoaldevl@gmail.com

## 🙏 Agradecimientos

- [Expo](https://expo.dev/) por simplificar el desarrollo React Native
- [Render.com](https://render.com) por el hosting gratuito
- [MongoDB Atlas](https://mongodb.com/atlas) por la base de datos en la nube

---

⭐ **¡Si te gusta este proyecto, dale una estrella!** ⭐
