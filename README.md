# 💝 30 Días Contigo

Una página web romántica para celebrar un mes de amor. Este proyecto es un regalo digital interactivo que muestra 30 días de recuerdos especiales con fotos y mensajes personalizados.

## ✨ Características

- 🎨 **Diseño romántico** con gradientes rosa, púrpura y efectos visuales
- 💖 **Animaciones suaves** con corazones flotantes y destellos de luz
- 📸 **Carrusel de fotos** estilo Polaroid con 30 imágenes
- 💌 **Mensajes personalizados** para cada día
- 🎯 **Interfaz interactiva** - toca/haz clic para avanzar
- 📱 **Responsive** - se ve perfecto en móvil y escritorio
- ⚡ **Sin costos** - 100% gratis en Firebase

## 🚀 Cómo usar este proyecto

### Prerequisitos

- Node.js instalado (versión 16 o superior)
- Una cuenta de Firebase (gratuita)
- Tus fotos subidas a Google Drive

### Instalación

1. **Clona o descarga este repositorio**

```bash
git clone <tu-repositorio>
cd mi-regalo
```

2. **Instala las dependencias**

```bash
npm install
```

3. **Configura Firebase**

   - Ve a [Firebase Console](https://console.firebase.google.com/)
   - Crea un nuevo proyecto (si no lo has hecho)
   - Ve a "Project Settings" > "General" > "Your apps"
   - Copia la configuración de Firebase

4. **Personaliza el contenido**

   Edita el archivo `src/App.jsx`:

   - **Líneas 7-13**: Pega tu configuración de Firebase
   - **Líneas 23-53**: Agrega tus 30 fotos y mensajes

### 📸 Cómo subir fotos a Google Drive

1. Sube tus fotos a Google Drive
2. Haz clic derecho en cada foto → "Obtener enlace"
3. Cambia los permisos a "Cualquiera con el enlace"
4. El enlace será algo como: `https://drive.google.com/file/d/ID_DE_LA_FOTO/view`
5. Conviértelo a este formato: `https://lh3.googleusercontent.com/d/ID_DE_LA_FOTO`

**Ejemplo:**
```javascript
{
  id: 1,
  url: "https://lh3.googleusercontent.com/d/1LalNg8jI3mjPvDjR3MwxGcg3B2dhLAv2",
  mensaje: "Día 1: Nuestra primera mirada."
}
```

### 🎨 Personalizar mensajes

En el array `HISTORIA_30_DIAS`, cada objeto tiene:
- `id`: Número del día (1-30)
- `url`: URL de la foto
- `mensaje`: Tu mensaje romántico personalizado

```javascript
const HISTORIA_30_DIAS = [
  { id: 1, url: "TU_URL_AQUI", mensaje: "Tu mensaje aquí" },
  { id: 2, url: "TU_URL_AQUI", mensaje: "Tu mensaje aquí" },
  // ... hasta 30
];
```

### 🖥️ Desarrollo local

Para ver tu proyecto en desarrollo:

```bash
npm run dev
```

Abre tu navegador en `http://localhost:5173` (o el puerto que te indique)

### 📦 Build para producción

```bash
npm run build
```

Los archivos listos para producción estarán en la carpeta `dist/`

## 🌐 Desplegar a Firebase Hosting

### 1. Instala Firebase CLI

```bash
npm install -g firebase-tools
```

### 2. Inicia sesión en Firebase

```bash
firebase login
```

### 3. Inicializa Firebase en tu proyecto

```bash
firebase init hosting
```

Selecciona:
- ✅ Use an existing project → Selecciona tu proyecto
- ✅ Public directory: `dist`
- ✅ Configure as single-page app: `Yes`
- ✅ Set up automatic builds: `No`

### 4. Construye y despliega

```bash
npm run build
firebase deploy
```

¡Tu página estará en vivo en: `https://TU-PROYECTO.web.app`! 🎉

## 💰 Costos

**¡Este proyecto es 100% GRATIS!**

- ✅ Firebase Authentication (anónima): Gratis ilimitado
- ✅ Firebase Hosting: 10GB/mes gratis (más que suficiente)
- ✅ No usa base de datos
- ✅ Fotos en Google Drive (gratis)

**Plan recomendado:** Spark (Gratuito)

## 🛠️ Tecnologías utilizadas

- **React 19** - Framework de UI
- **Vite** - Build tool ultra rápido
- **Tailwind CSS 3** - Estilos y diseño
- **Firebase** - Autenticación y hosting
- **Lucide React** - Iconos bonitos
- **Google Drive** - Almacenamiento de imágenes

## 📁 Estructura del proyecto

```
mi-regalo/
├── src/
│   ├── App.jsx          # Componente principal (¡edita aquí!)
│   ├── main.jsx         # Entry point
│   ├── index.css        # Estilos Tailwind
│   └── App.css          # Estilos adicionales
├── public/              # Archivos públicos
├── dist/               # Build de producción
├── package.json        # Dependencias
├── tailwind.config.js  # Configuración Tailwind
├── postcss.config.js   # Configuración PostCSS
└── README.md          # Este archivo

```

## 🎨 Personalización avanzada

### Cambiar colores

En `src/App.jsx`, busca las clases de Tailwind:
- `rose-*` - Colores rosa
- `pink-*` - Colores rosa claro
- `purple-*` - Colores púrpura

### Modificar animaciones

Las animaciones están en las clases:
- `animate-pulse` - Pulso suave
- `animate-bounce` - Rebote
- `animate-ping` - Expansión

### Cambiar el título

Edita `index.html` línea 7:
```html
<title>30 Días Contigo</title>
```

## 🐛 Solución de problemas

### Los estilos no se cargan

```bash
npm install -D tailwindcss@3.4.1 postcss autoprefixer
```

### Firebase no se conecta

Verifica que tu configuración de Firebase en `src/App.jsx` esté correcta.

### Las fotos no cargan

Asegúrate de que:
1. Las fotos tengan permisos públicos en Google Drive
2. El URL tenga el formato correcto: `https://lh3.googleusercontent.com/d/ID`

## 📝 Licencia

Este proyecto es de uso personal. Siéntete libre de usarlo y modificarlo para tu propio regalo romántico. 💕

## 🙏 Créditos

Hecho con ❤️ para alguien muy especial.

---

**¿Dudas?** Revisa la documentación de:
- [Firebase](https://firebase.google.com/docs)
- [React](https://react.dev)
- [Tailwind CSS](https://tailwindcss.com)

¡Que disfrutes regalando amor! 💝✨
