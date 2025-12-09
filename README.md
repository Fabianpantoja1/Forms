# Formulario de Registro - María Irma Noreña

## 🚀 Pasos para Desplegar en Vercel

### 1. Configurar la URL del Script

Antes de desplegar, debes editar el archivo `index.html` y reemplazar la URL del Google Apps Script:

1. Abre el archivo `index.html`
2. Busca la línea 189:
   ```javascript
   const SCRIPT_URL = 'TU_URL_DE_GOOGLE_APPS_SCRIPT_AQUI';
   ```
3. Reemplaza `TU_URL_DE_GOOGLE_APPS_SCRIPT_AQUI` con la URL que copiaste de Google Apps Script
4. Debe quedar así:
   ```javascript
   const SCRIPT_URL = 'https://script.google.com/macros/s/AKfycby.../exec';
   ```

### 2. Subir a GitHub (Opción A - Recomendada)

1. Crea un nuevo repositorio en GitHub
2. Sube estos archivos:
   - `index.html`
   - `vercel.json`
3. Ve a [vercel.com](https://vercel.com)
4. Clic en "Import Project"
5. Conecta tu repositorio de GitHub
6. Clic en "Deploy"

### 3. Desplegar directamente con Vercel CLI (Opción B)

1. Instala Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. En la carpeta del proyecto, ejecuta:
   ```bash
   vercel
   ```

3. Sigue las instrucciones en pantalla

### 4. Desplegar arrastrando archivos (Opción C - Más Fácil)

1. Ve a [vercel.com/new](https://vercel.com/new)
2. Arrastra la carpeta con los archivos
3. Clic en "Deploy"

## 📋 Campos del Formulario

El formulario captura estos datos (deben coincidir con tu Google Sheet):

1. **Fecha Registro** (automática)
2. **Nombre** (obligatorio)
3. **Cédula** (obligatorio)
4. **Teléfono** (obligatorio)
5. **Ocupación** (opcional)
6. **Dirección** (opcional)
7. **Barrio** (opcional)
8. **Ciudad** (obligatorio)

## ✅ Verificación

Para verificar que todo funciona:

1. Abre tu formulario desplegado
2. Llena los datos de prueba
3. Envía el formulario
4. Revisa que aparezca en la pestaña "Contactos" de tu Google Sheet

## 🎨 Personalización

Puedes cambiar:
- Colores en el CSS (línea 15-20)
- Logo o encabezado (línea 165-168)
- Textos y placeholder

## 🔒 Seguridad

- Los datos se envían directamente a Google Sheets
- No hay backend intermedio
- Todos los datos son confidenciales
- Solo tú tienes acceso a la hoja de cálculo

## 📱 Responsive

El formulario está optimizado para:
- ✅ Computadoras
- ✅ Tablets
- ✅ Celulares

## 🆘 Solución de Problemas

**Si no se guardan los datos:**
1. Verifica que la URL del script esté correcta
2. Verifica que la hoja se llame exactamente "Contactos"
3. Revisa los permisos del Google Apps Script

**Si aparece error CORS:**
- Es normal en pruebas locales
- Despliega en Vercel y funcionará correctamente

---

**Desarrollado para la campaña de María Irma Noreña**
Senado - Valle del Cauca
