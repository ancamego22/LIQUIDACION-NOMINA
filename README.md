# 📱 Liquidador de Nómina y Turnos - Colombia 2026

Aplicación web para liquidación de nómina conforme a la normativa laboral colombiana vigente.

## ✨ Características

- ✅ Cálculo automático de recargos nocturnos (35%) - Ley 2466/2024
- ✅ Recargos dominicales y festivos (90% diurno, 125% nocturno)
- ✅ Calculadora de Prima de Servicios con fecha de ingreso
- ✅ Calculadora de Vacaciones (15 días hábiles)
- ✅ Deducciones de Seguridad Social (Salud 4%, Pensión 4%)
- ✅ Selector de quincena (15 o 30)
- ✅ Modal con normativa legal completa
- ✅ Diseño responsivo para móviles y tablets
- ✅ **Instalable como PWA (Progressive Web App)**
- ✅ Funciona offline una vez instalada

## 📲 Instalar como App en tu Móvil

### Android (Chrome/Edge)
1. Abre la aplicación en Chrome o Edge
2. Toca el menú (⋮) en la esquina superior derecha
3. Selecciona **"Agregar a pantalla de inicio"** o **"Instalar app"**
4. Confirma la instalación
5. ¡Listo! El ícono aparecerá en tu pantalla de inicio

### iOS (Safari)
1. Abre la aplicación en Safari
2. Toca el botón de compartir (🔗) en la barra inferior
3. Desplázate y selecciona **"Agregar a pantalla de inicio"**
4. Personaliza el nombre si deseas
5. Toca **"Agregar"**
6. ¡Listo! El ícono aparecerá en tu pantalla de inicio

### Escritorio (Chrome/Edge/Brave)
1. Abre la aplicación en tu navegador
2. Busca el ícono de instalación (➕) en la barra de direcciones
3. Haz clic en **"Instalar"**
4. La aplicación se abrirá en su propia ventana

## 🎨 Crear los Iconos para PWA

Para que la PWA funcione correctamente, necesitas crear dos iconos:

### Opción 1: Usar un generador online (Recomendado)
1. Ve a https://realfavicongenerator.net/
2. Sube un logo o diseño de 512x512px
3. Descarga los iconos generados
4. Renombra los archivos como `icon-192.png` y `icon-512.png`
5. Coloca los archivos en la carpeta raíz del proyecto

### Opción 2: Crear manualmente
Necesitas crear dos imágenes PNG:
- **icon-192.png**: 192x192 píxeles
- **icon-512.png**: 512x512 píxeles

**Diseño sugerido:**
- Fondo: Azul #1e3a8a (azul oscuro)
- Ícono central: Calculadora o símbolo de $ en blanco
- Bordes redondeados opcionales

**Herramientas recomendadas:**
- Canva (online, gratis)
- Figma (online, gratis)
- GIMP (desktop, gratis)
- Photoshop (desktop, pago)

### Opción 3: Icono temporal simple
Puedes usar un fondo de color sólido con texto:
```html
<!-- Genera esto en cualquier editor de imágenes -->
Fondo: #1e3a8a (azul)
Texto: "💰" o "📊" emoji grande centrado
Tamaño: 192x192 y 512x512
```

## 🚀 Subir a GitHub Pages

1. **Crear repositorio en GitHub:**
   - Ve a https://github.com/new
   - Nombre: `liquidador-nomina` (o el que prefieras)
   - Visibilidad: Público
   - Clic en "Create repository"

2. **Subir archivos:**
   ```bash
   cd C:\Users\kmiil\Downloads\NOMINA
   git init
   git add .
   git commit -m "Liquidador de nómina Colombia 2026"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/liquidador-nomina.git
   git push -u origin main
   ```

3. **Activar GitHub Pages:**
   - Ve a Settings → Pages
   - Source: Deploy from a branch
   - Branch: main → / (root) → Save
   - Espera 1-2 minutos

4. **Tu app estará en:**
   ```
   https://TU-USUARIO.github.io/liquidador-nomina/
   ```

## 📋 Archivos del Proyecto

```
NOMINA/
├── index.html          # Aplicación principal
├── manifest.json       # Configuración PWA
├── icon-192.png        # Ícono 192x192 (créalo)
├── icon-512.png        # Ícono 512x512 (créalo)
└── README.md           # Este archivo
```

## ⚖️ Base Legal

Toda la aplicación está fundamentada en:
- **Código Sustantivo del Trabajo (CST)**
- **Ley 2466 de 2024** (Recargo nocturno 7 PM - 6 AM)
- **Ley 100 de 1993** (Seguridad Social)
- **Artículo 306 CST** (Prima de Servicios)
- **Artículo 186 CST** (Vacaciones)

Ver el botón **"Normativa Legal"** en la app para más detalles.

## ⚠️ Disclaimer

Esta aplicación es una herramienta de apoyo para cálculos de nómina. Se recomienda validación por un Contador Público o profesional de RRHH para casos específicos.

Los valores de SMMLV y Auxilio de Transporte 2026 deben actualizarse cuando se publiquen oficialmente.

---

**Desarrollado por:** Andrés Medina
**Avalado por:** Contador Público (verificar antes de indicar)
**Año:** 2026
