# 📊 Guía de Configuración de Google Analytics para CalculaNomina

## ✅ Cambios Implementados

### 1. **Normativa Legal integrada en index.html**
- ✅ Ya NO es página separada
- ✅ Es una sección dentro de index.html con ID `#seccion-normativa`
- ✅ El botón "Normativa Legal" hace scroll suave hacia abajo
- ✅ No afecta la liquidación del usuario
- ✅ Botón "Volver arriba" para regresar

### 2. **Sistema de Analytics configurado**
- ✅ Google Analytics agregado al `<head>`
- ✅ Código listo para rastrear visitantes

---

## 🔧 Cómo Activar Google Analytics (Paso a Paso)

### Paso 1: Crear cuenta de Google Analytics

1. Ve a: https://analytics.google.com
2. Inicia sesión con tu cuenta de Google
3. Haz clic en **"Comenzar a medir"**
4. Ingresa:
   - **Nombre de la cuenta:** CalculaNomina
   - **Nombre de la propiedad:** CalculaNomina Web
   - **Zona horaria:** (GMT-05:00) Bogotá
   - **Moneda:** Peso colombiano (COP)
5. Selecciona:
   - Categoría: **Finanzas**
   - Tamaño de empresa: **Pequeña (1-10 empleados)**
6. Haz clic en **"Crear"** y acepta los términos

### Paso 2: Configurar flujo de datos

1. Selecciona **"Web"** como plataforma
2. Ingresa:
   - **URL del sitio web:** https://tuusuario.github.io/calculanomina
   - **Nombre del flujo:** CalculaNomina Web
3. Haz clic en **"Crear flujo"**

### Paso 3: Obtener tu ID de medición

Verás algo como: **G-XXXXXXXXXX** (ejemplo: G-1A2B3C4D5E)

### Paso 4: Reemplazar en index.html

Abre `index.html` y busca estas 2 líneas (están en el `<head>`):

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
```

```javascript
gtag('config', 'G-XXXXXXXXXX');
```

**Reemplaza `G-XXXXXXXXXX` con tu ID real en AMBAS líneas.**

Ejemplo:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-1A2B3C4D5E"></script>
```

```javascript
gtag('config', 'G-1A2B3C4D5E');
```

### Paso 5: Subir a GitHub

```bash
git add .
git commit -m "Agregado Google Analytics"
git push
```

### Paso 6: Verificar que funciona

1. Abre tu app: https://tuusuario.github.io/calculanomina
2. En otra pestaña, ve a Google Analytics
3. Ve a **Informes → Tiempo real**
4. Deberías ver **1 usuario activo** (tú mismo)

✅ Si apareces, ¡funciona correctamente!

---

## 📊 Qué Datos Podrás Ver

### Panel Principal (Informes → Resumen)
- **Usuarios activos:** Cuántas personas están usando la app AHORA
- **Nuevos usuarios:** Cuántos usuarios nuevos por día/semana/mes
- **Sesiones:** Cuántas veces abren la app
- **Duración promedio:** Cuánto tiempo pasan en la app

### Informes Detallados

#### 1. **Audiencia** (Quiénes son tus usuarios)
- **Datos demográficos:** Edad, género, ubicación
- **Dispositivos:** Móvil (Android/iOS), Desktop, Tablet
- **Navegadores:** Chrome, Safari, Edge, etc.
- **Ciudades:** Bogotá, Medellín, Cali, etc.

#### 2. **Comportamiento** (Qué hacen en la app)
- **Páginas más visitadas:** Inicio, Normativa Legal, etc.
- **Tiempo en cada página**
- **Tasa de rebote:** % que sale inmediatamente

#### 3. **Eventos Personalizados** (Opcional - Avanzado)
Puedes rastrear acciones específicas como:
- Clicks en "Descargar PNG"
- Clicks en "Imprimir PDF"
- Uso del calendario
- Registro de horas extras

---

## 🎯 Eventos Personalizados (Opcional pero Recomendado)

Para rastrear acciones específicas, agrega esto en las funciones de JavaScript:

### Ejemplo 1: Rastrear descarga de PNG

Busca la función `descargarImagen()` y agrega:

```javascript
function descargarImagen() {
    // Rastrear evento en Google Analytics
    gtag('event', 'descargar_desprendible', {
        'event_category': 'engagement',
        'event_label': 'PNG'
    });
    
    // Resto del código existente...
    const elemento = document.getElementById('desprendiblePago');
    html2canvas(elemento, { scale: 2 }).then(canvas => {
        let enlace = document.createElement('a');
        enlace.download = 'desprendible-nomina.png';
        enlace.href = canvas.toDataURL('image/png');
        enlace.click();
    });
}
```

### Ejemplo 2: Rastrear clicks en Normativa Legal

```javascript
// Agregar al final del <script>
document.querySelector('a[href="#seccion-normativa"]').addEventListener('click', function() {
    gtag('event', 'ver_normativa', {
        'event_category': 'contenido',
        'event_label': 'Normativa Legal'
    });
});
```

---

## 🚀 Próximos Pasos Recomendados

### Corto Plazo (Esta Semana)
1. ✅ Configurar Google Analytics
2. ✅ Verificar que funciona
3. ✅ Compartir con tus 40+ beta testers
4. ✅ Monitorear usuarios activos diariamente

### Mediano Plazo (Próximas 2 Semanas)
1. Analizar qué dispositivos usan más (móvil vs desktop)
2. Ver qué ciudades tienen más usuarios
3. Identificar funciones más usadas
4. Recolectar feedback de usuarios

### Largo Plazo (Próximo Mes)
1. Implementar eventos personalizados (clicks, descargas)
2. Configurar objetivos (ej: "completar liquidación")
3. Analizar flujo de usuarios (qué hacen primero/después)
4. Crear reportes semanales automáticos

---

## 📈 Métricas Clave a Monitorear

### Semana 1-2 (Validación)
- **Objetivo:** 40+ usuarios únicos
- **Métrica clave:** Tiempo promedio en sitio (> 3 minutos = buena señal)
- **Acción:** Si < 1 minuto, hay problemas de UX

### Mes 1 (Crecimiento)
- **Objetivo:** 100+ usuarios únicos
- **Métrica clave:** Tasa de retorno (usuarios que vuelven)
- **Acción:** Si < 20% retornan, mejorar funcionalidades

### Mes 2-3 (Optimización)
- **Objetivo:** 500+ usuarios únicos
- **Métrica clave:** Conversión a premium (cuando lo lances)
- **Acción:** A/B testing de precios

---

## 🔒 Privacidad y GDPR

**Importante:** Google Analytics es legal en Colombia, pero considera:

1. **Agregar Política de Privacidad** (obligatorio si creces)
2. **Banner de Cookies** (opcional por ahora, obligatorio si llegas a Europa)
3. **Anonimización de IP** (ya incluida por defecto en GA4)

---

## 🆘 Solución de Problemas

### No aparecen datos en Analytics
- Espera 24-48 horas (a veces tarda)
- Verifica que el ID esté en AMBAS líneas
- Abre en modo incógnito y prueba
- Desactiva AdBlockers en tu navegador

### Aparecen pocos usuarios
- Normal al inicio
- Comparte más el link
- Google Analytics solo rastrea visitas web (no cuenta instalaciones PWA como app separada)

### Quiero más métricas
- Considera agregar **Microsoft Clarity** (gratis, muestra grabaciones de sesiones)
- O **Hotjar** (mapas de calor, ver dónde hacen click)

---

## 📞 Recursos Útiles

- **Google Analytics Academy:** https://analytics.google.com/analytics/academy/
- **Dashboard de Analytics:** https://analytics.google.com
- **Documentación GA4:** https://support.google.com/analytics

---

**¿Necesitas ayuda configurando?** Avísame y te guío paso a paso.

**Última actualización:** Enero 2026
