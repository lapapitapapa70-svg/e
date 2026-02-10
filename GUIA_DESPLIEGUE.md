# 📖 GUÍA PASO A PASO: GitHub + Despliegue Gratis

## PASO 1: Subir el Proyecto a GitHub

### 1.1 Crear Repositorio en GitHub
1. Ve a https://github.com
2. Click en el botón **"+"** arriba a la derecha
3. Selecciona **"New repository"**
4. Nombre: `sistema-trolleo` (o el que quieras)
5. Descripción: "Sistema de trolleo con sonidos"
6. **Importante:** Marca como **"Public"** (o los servicios gratis no funcionarán)
7. Click en **"Create repository"**

### 1.2 Subir tus Archivos
Tienes dos opciones:

#### OPCIÓN A: Desde la Web (Más Fácil)
1. En tu nuevo repositorio, click en **"uploading an existing file"**
2. Arrastra todos estos archivos:
   - `server.js`
   - `package.json`
   - `README.md`
   - `.gitignore`
   - `render.yaml`
   - Carpeta `public/` completa (con index.html y sonidos/)
3. Click en **"Commit changes"**

#### OPCIÓN B: Desde la Terminal (Avanzado)
```bash
# En la carpeta de tu proyecto
git init
git add .
git commit -m "Primera versión del sistema de trolleo"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/sistema-trolleo.git
git push -u origin main
```

## PASO 2: Agregar los Archivos de Sonido

**⚠️ IMPORTANTE:** Antes de desplegar, debes agregar tus archivos MP3:

1. En GitHub, navega a `public/sonidos/`
2. Click en **"Add file"** → **"Upload files"**
3. Sube tus 5 archivos MP3 con estos nombres exactos:
   - `sonido1.mp3`
   - `sonido2.mp3`
   - `sonido3.mp3`
   - `sonido4.mp3`
   - `sonido5.mp3`
4. Click en **"Commit changes"**

### Donde conseguir sonidos gratis:
- https://freesound.org (requiere registro gratis)
- https://mixkit.co/free-sound-effects/
- https://www.zapsplat.com

## PASO 3: Desplegar en Render.com (GRATIS)

### 3.1 Crear Cuenta
1. Ve a https://render.com
2. Click en **"Get Started for Free"**
3. Regístrate con tu cuenta de GitHub (más fácil)

### 3.2 Conectar tu Repositorio
1. En el dashboard de Render, click en **"New +"**
2. Selecciona **"Web Service"**
3. Click en **"Connect" a repository"** (si es la primera vez)
4. Autoriza a Render para acceder a tus repositorios
5. Encuentra y selecciona **"sistema-trolleo"**

### 3.3 Configurar el Servicio
Render debería detectar automáticamente que es Node.js. Verifica:

- **Name:** sistema-trolleo (o cambia si quieres)
- **Region:** Frankfurt (o la más cercana)
- **Branch:** main
- **Build Command:** `npm install`
- **Start Command:** `npm start`
- **Plan:** **FREE** ⭐

### 3.4 Variables de Entorno (Opcional)
No necesitas configurar nada extra para este proyecto.

### 3.5 Desplegar
1. Click en **"Create Web Service"**
2. Espera 2-5 minutos mientras se despliega
3. Una vez que veas **"Live"** en verde, ¡está listo!

### 3.6 Obtener tu URL
Tu app estará disponible en:
```
https://sistema-trolleo.onrender.com
```
(o el nombre que hayas elegido)

## PASO 4: ¡USAR TU APP!

1. Abre la URL en tu navegador
2. Comparte la URL con amigos
3. Un dispositivo usa modo **COMANDOS** (código: 82900)
4. Otros dispositivos usan modo **TROLLEO**
5. ¡A trollear! 🎉

## ⚠️ NOTAS IMPORTANTES de Render.com FREE

- **Se duerme después de 15 minutos sin uso**
  - La primera visita tardará 30-60 segundos en despertar
  - Luego funciona normal
  
- **750 horas gratis al mes** (suficiente para uso personal)

- **Si se duerme mientras estás en modo TROLLEO:**
  - Simplemente recarga la página
  - Vuelve a entrar a modo TROLLEO

## 🔄 ACTUALIZAR TU APP

Cada vez que hagas cambios en GitHub:
1. Sube los cambios a tu repositorio
2. Render detectará los cambios automáticamente
3. Redesplegará tu app (toma 2-3 minutos)

## 🆘 PROBLEMAS COMUNES

### "Application failed to respond"
- Verifica que todos los archivos estén en GitHub
- Revisa que `package.json` esté correcto
- Mira los logs en Render para ver el error

### "Los sonidos no se reproducen"
- ¿Subiste los archivos MP3 a GitHub?
- ¿Los nombres son exactos? (sonido1.mp3, no Sonido1.mp3)
- ¿Los archivos están en `public/sonidos/`?

### "Cannot GET /"
- El servidor no está iniciando correctamente
- Revisa que `server.js` esté en la raíz del proyecto
- Mira los logs en Render

## 🎯 ALTERNATIVAS A RENDER

Si Render no te funciona, prueba:

### Railway.app
1. https://railway.app
2. "New Project" → "Deploy from GitHub"
3. Selecciona tu repo
4. ¡Deploy automático!

### Glitch.com
1. https://glitch.com
2. "New Project" → "Import from GitHub"
3. Pega tu URL de GitHub
4. ¡Listo!

---

## 📱 COMPARTIR CON AMIGOS

Una vez desplegado, comparte tu URL:
- Por WhatsApp
- Por Discord
- Por cualquier red social

¡Que se diviertan! 🎭
