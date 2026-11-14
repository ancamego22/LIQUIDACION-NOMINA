# 🚀 ROADMAP - CalculaNomina
## Evolución de Liquidador a Plataforma Integral de Gestión Laboral

---

## 📊 VISIÓN DEL PROYECTO

**CalculaNomina** evolucionará de un simple liquidador de nómina a una **plataforma integral** que combina:
- 📅 **Calendario de Turnos** para personal de salud
- 💰 **Liquidación de Nómina** automática
- 📊 **Historial y Reportes**
- 👤 **Gestión de usuarios** (freemium model)

---

## 🎯 FASE ACTUAL: v1.0 - MVP Público (COMPLETADO)

### ✅ Funcionalidades Actuales:
- Liquidador de nómina quincenal
- Cálculo de recargos (nocturno, dominical, festivo)
- Calculadora de prima y vacaciones
- Registro de horas extras
- Normativa legal colombiana completa
- PWA instalable (funciona offline)
- Sin autenticación (acceso libre)

### 📂 Estado Actual:
```
NOMINA/
├── index.html          # Aplicación principal (v1.0)
├── manifest.json       # Configuración PWA
├── favicon.svg         # Logo/Ícono
├── README.md           # Documentación
└── ROADMAP.md         # Este archivo
```

---

## 📅 PLAN DE DESARROLLO - Próximos 12 Meses

### **FASE 2: v2.0 - Calendario de Turnos Inteligente**
**🗓️ Duración:** 2-3 meses  
**🎯 Objetivo:** Crear sistema de gestión de turnos visual e intuitivo

#### Funcionalidades:
1. **Módulo de Gestión de Turnos**
   - Vista mensual del calendario con turnos asignados
   - Crear/editar/eliminar turnos personalizados
   - Biblioteca de turnos predefinidos (salud, seguridad, etc.)
   - Códigos de colores por tipo de turno
   - Duplicar turnos de un mes a otro
   - Exportar calendario a PDF/imagen

2. **Integración con Liquidación**
   - Los turnos del calendario alimentan automáticamente el liquidador
   - Vista previa de valor a pagar por quincena
   - Indicador visual de ingresos estimados del mes

3. **Mejoras de UI/UX**
   - Diseño moderno con animaciones suaves
   - Modo oscuro
   - Navegación por tabs (Turnos / Liquidación / Configuración)

#### Arquitectura Técnica:
```
calculanomina/
├── v1/                     # Versión actual (backup)
│   └── index.html
├── v2/                     # Nueva versión
│   ├── index.html          # Entrada principal
│   ├── css/
│   │   ├── styles.css
│   │   └── themes.css
│   ├── js/
│   │   ├── app.js          # Inicialización
│   │   ├── turnos.js       # Gestión de turnos
│   │   ├── nomina.js       # Cálculos de nómina
│   │   ├── calendar.js     # Componente calendario
│   │   └── storage.js      # LocalStorage manager
│   └── components/
│       ├── header.html
│       ├── calendar.html
│       └── liquidador.html
├── assets/
│   ├── icons/
│   └── images/
└── docs/
    ├── ROADMAP.md
    ├── CHANGELOG.md
    └── API.md
```

---

### **FASE 3: v3.0 - Sistema de Usuarios y Backend**
**🗓️ Duración:** 3-4 meses  
**🎯 Objetivo:** Implementar autenticación, base de datos y modelo freemium

#### Funcionalidades:
1. **Sistema de Autenticación**
   - Registro de usuarios (email + contraseña)
   - Login con Google / Microsoft
   - Recuperación de contraseña
   - Verificación de email

2. **Base de Datos en la Nube**
   - Firebase / Supabase para backend
   - Sincronización en tiempo real
   - Backup automático de datos

3. **Gestión de Datos del Usuario**
   - Perfil de usuario (nombre, cargo, empresa)
   - Múltiples configuraciones de turnos
   - Historial de nóminas guardadas
   - Exportación de datos (JSON, Excel)

4. **Modelo Freemium**
   - **Gratis:**
     - Liquidación del mes actual
     - Calendario de turnos básico
     - Límite de 3 meses de historial
   
   - **Premium ($20,000/mes):**
     - Historial ilimitado
     - Múltiples perfiles (gestiona varios empleados)
     - Reportes avanzados en Excel/PDF
     - Soporte prioritario
     - Sin anuncios
     - Recordatorios de pago de nómina

5. **Panel de Administración**
   - Dashboard con estadísticas
   - Gráficos de ingresos mensuales
   - Comparativas año vs año

#### Stack Tecnológico Propuesto:
```
Frontend:
- React.js / Vue.js (framework moderno)
- Tailwind CSS (mantener consistencia)
- Chart.js (gráficos)

Backend:
- Firebase Authentication
- Firestore Database (NoSQL)
- Firebase Functions (lógica del servidor)
- Firebase Hosting

Pagos:
- Wompi (pasarela colombiana)
- Mercado Pago (alternativa)
```

---

### **FASE 4: v4.0 - Funcionalidades Avanzadas**
**🗓️ Duración:** 2-3 meses  
**🎯 Objetivo:** Diferenciación y valor agregado

#### Funcionalidades:
1. **Trabajo en Equipo**
   - Compartir calendario con compañeros
   - Vista de equipo (ver turnos de todos)
   - Chat interno básico

2. **Inteligencia Artificial**
   - Sugerencias de turnos basados en historial
   - Predicción de ingresos futuros
   - Alertas de inconsistencias en turnos

3. **Integraciones**
   - Exportar a Google Calendar
   - Sincronización con sistemas hospitalarios
   - API pública para terceros

4. **Módulo de Cesantías**
   - Cálculo automático de cesantías
   - Simulador de retiro de cesantías
   - Intereses sobre cesantías

5. **Notificaciones**
   - Push notifications (nuevos turnos, cambios)
   - Recordatorios de pago de nómina
   - Alertas de actualizaciones legales

---

### **FASE 5: v5.0 - Expansión y Escalabilidad**
**🗓️ Duración:** Continuo  
**🎯 Objetivo:** Crecimiento y monetización sostenible

#### Funcionalidades:
1. **Plan Empresarial**
   - Gestión de nómina para equipos completos
   - Administrador + Empleados
   - Reportes consolidados
   - Precio: $50,000 - $150,000/mes según número de empleados

2. **Marketplace de Plantillas**
   - Usuarios pueden vender/comprar configuraciones de turnos
   - Plantillas para diferentes sectores (salud, seguridad, retail)

3. **App Móvil Nativa**
   - iOS y Android
   - Notificaciones push nativas
   - Mejor rendimiento

4. **Cumplimiento Normativo Automático**
   - Actualización automática cuando cambien leyes
   - Alertas de nuevas regulaciones
   - Integración con MinTrabajo (APIs oficiales)

---

## 🗓️ CRONOGRAMA VISUAL

```
2026
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Ene-Feb  │ FASE 2: Desarrollo Calendario de Turnos
Mar      │ FASE 2: Testing y Lanzamiento v2.0
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Abr-Jun  │ FASE 3: Backend, Autenticación, Base de Datos
Jul      │ FASE 3: Implementación Modelo Freemium
Ago      │ FASE 3: Testing y Lanzamiento v3.0
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Sep-Oct  │ FASE 4: Funcionalidades Avanzadas
Nov      │ FASE 4: Lanzamiento v4.0
Dic      │ Evaluación y Planificación 2027
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

2027+    │ FASE 5: Expansión Continua
```

---

## 💰 MODELO DE MONETIZACIÓN

### Fase Inicial (v1.0 - v2.0)
- ✅ **100% Gratis** - Construcción de audiencia
- ✅ Sin anuncios
- ✅ Código abierto (opcional)

### Fase Intermedia (v3.0+)
**Plan Gratuito:**
- Liquidación mensual básica
- Calendario de turnos
- 3 meses de historial

**Plan Premium - $20,000/mes:**
- Todo lo del plan gratuito
- Historial ilimitado
- Múltiples perfiles
- Reportes en Excel/PDF
- Sin anuncios
- Soporte prioritario

**Plan Empresarial - $100,000+/mes:**
- Gestión de equipos completos
- API personalizada
- Soporte dedicado
- Capacitación incluida

### Proyección de Ingresos (Optimista)
```
Año 1 (2026):
- 1,000 usuarios gratuitos
- 50 usuarios premium ($1,000,000/mes)
- Total año: ~$12,000,000 COP

Año 2 (2027):
- 10,000 usuarios gratuitos
- 500 usuarios premium ($10,000,000/mes)
- 10 empresas ($1,000,000/mes)
- Total año: ~$132,000,000 COP

Año 3 (2028):
- 50,000 usuarios gratuitos
- 2,000 usuarios premium ($40,000,000/mes)
- 50 empresas ($5,000,000/mes)
- Total año: ~$540,000,000 COP
```

---

## 🎨 MEJORAS DE DISEÑO PLANIFICADAS

### UI/UX Moderna:
1. **Dashboard Principal**
   - Cards animadas con estadísticas
   - Gráficos interactivos (Chart.js / ApexCharts)
   - Microinteracciones (hover effects, loading states)

2. **Sistema de Diseño**
   - Paleta de colores ampliada
   - Componentes reutilizables
   - Animaciones con Framer Motion o GSAP

3. **Responsive Avanzado**
   - Optimización para tablets
   - Gestos táctiles (swipe, pinch)
   - Modo compacto para móviles pequeños

4. **Temas Personalizables**
   - Modo claro / oscuro
   - Colores de acento personalizables
   - Tamaños de fuente ajustables (accesibilidad)

### Referencias de Diseño:
- **Linear.app** - Diseño minimalista y rápido
- **Notion** - Flexibilidad y componentes
- **Stripe Dashboard** - Gráficos y reportes
- **Calendly** - Gestión de calendario

---

## 🔄 ACTUALIZACIONES NORMATIVAS

### Sistema de Actualización Automática:
1. **Monitoreo de Cambios Legales**
   - Suscripción a boletines de MinTrabajo
   - Alertas en DIAN y entidades oficiales
   - RSS feeds de noticias laborales

2. **Versionado de Normativa**
   - Cada cambio legal = nueva versión
   - Histórico de cambios visible
   - Changelog detallado

3. **Notificaciones a Usuarios**
   - Email cuando haya actualizaciones
   - Banner en la app
   - Explicación de cambios con ejemplos

### Fechas Clave 2026:
- **Enero:** Publicación SMLV y Aux. Transporte 2026
- **Febrero:** Actualización de la app v1.1
- **Junio:** Revisión pre-prima semestral
- **Diciembre:** Revisión anual completa

---

## 📂 ORGANIZACIÓN DEL PROYECTO

### Estructura de Carpetas Propuesta:

```
calculanomina-project/
│
├── 📁 production/              # Versión en producción (GitHub Pages)
│   ├── index.html
│   ├── manifest.json
│   └── assets/
│
├── 📁 development/             # Desarrollo activo
│   ├── v2-turnos/             # Fase 2 en desarrollo
│   ├── v3-backend/            # Fase 3 en desarrollo
│   └── components/            # Componentes reutilizables
│
├── 📁 docs/                    # Documentación
│   ├── ROADMAP.md             # Este archivo
│   ├── CHANGELOG.md           # Historial de cambios
│   ├── CONTRIBUTING.md        # Guía para colaboradores
│   ├── API.md                 # Documentación API (futuro)
│   └── LEGAL.md               # Bases legales y normativa
│
├── 📁 design/                  # Recursos de diseño
│   ├── mockups/               # Diseños en Figma
│   ├── logos/                 # Variaciones del logo
│   └── icons/                 # Íconos personalizados
│
├── 📁 tests/                   # Pruebas
│   ├── unit/                  # Pruebas unitarias
│   └── e2e/                   # Pruebas end-to-end
│
├── 📁 scripts/                 # Scripts útiles
│   ├── deploy.sh              # Script de despliegue
│   └── backup.sh              # Backup de datos
│
├── .gitignore
├── package.json               # Dependencias (cuando usemos Node.js)
└── README.md                  # Documentación principal
```

---

## 🛠️ TECNOLOGÍAS Y HERRAMIENTAS

### Stack Actual (v1.0):
- HTML5 / CSS3 (Tailwind CDN)
- JavaScript Vanilla
- LocalStorage
- PWA (Service Workers)

### Stack Futuro (v3.0+):
**Frontend:**
- React 18+ / Vue 3
- TypeScript
- Tailwind CSS
- Vite (build tool)
- React Query (data fetching)
- Zustand (state management)

**Backend:**
- Firebase (Auth + Firestore + Functions + Hosting)
- Node.js 20+
- Express.js (API REST)

**Testing:**
- Jest (unit tests)
- Playwright (e2e tests)
- Vitest (testing framework)

**DevOps:**
- GitHub Actions (CI/CD)
- Vercel / Netlify (hosting alternativo)
- Sentry (error tracking)
- Google Analytics (métricas)

**Diseño:**
- Figma (UI/UX)
- Canva (marketing materials)
- Excalidraw (diagramas)

---

## 📊 KPIs Y MÉTRICAS

### Métricas de Éxito por Fase:

**FASE 2 (v2.0):**
- [ ] 100 usuarios activos mensuales
- [ ] 70% de retención a 30 días
- [ ] Promedio 3 sesiones/usuario/mes

**FASE 3 (v3.0):**
- [ ] 1,000 usuarios registrados
- [ ] 5% conversión a premium
- [ ] NPS Score > 40

**FASE 4 (v4.0):**
- [ ] 5,000 usuarios registrados
- [ ] 10% conversión a premium
- [ ] 50 empresas suscritas
- [ ] NPS Score > 50

---

## 🎯 PRÓXIMOS PASOS INMEDIATOS

### Enero 2026:
1. ✅ Lanzar v1.0 en GitHub Pages
2. ✅ Crear estructura de carpetas para v2.0
3. 🔲 Diseñar mockups de calendario en Figma
4. 🔲 Configurar repositorio Git organizado
5. 🔲 Crear CHANGELOG.md inicial

### Febrero 2026:
1. 🔲 Desarrollar módulo de gestión de turnos
2. 🔲 Implementar calendario visual mejorado
3. 🔲 Testing con usuarios beta (10-20 personas)
4. 🔲 Actualizar valores SMLV y Aux. Transporte 2026

### Marzo 2026:
1. 🔲 Lanzamiento oficial v2.0
2. 🔲 Campaña de difusión en redes sociales
3. 🔲 Recolección de feedback
4. 🔲 Planificación detallada de v3.0 (backend)

---

## 💡 RECOMENDACIONES FINALES

### Para Mantener el Proyecto Organizado:

1. **Usa Git desde Ya**
   ```bash
   git init
   git add .
   git commit -m "v1.0 - MVP Liquidador de Nómina"
   git branch development  # Para trabajo en progreso
   git branch main         # Solo versiones estables
   ```

2. **Crea Issues en GitHub**
   - Cada funcionalidad nueva = 1 issue
   - Labels: `enhancement`, `bug`, `documentation`
   - Milestones para cada fase

3. **Documenta TODO**
   - Comenta el código complejo
   - Actualiza CHANGELOG.md con cada cambio
   - Mantén README.md al día

4. **Testing Constante**
   - Prueba en diferentes dispositivos
   - Pide feedback a usuarios reales
   - Corrige bugs antes de agregar features

5. **Mantén el Scope Controlado**
   - No intentes hacer todo a la vez
   - Una fase a la vez, bien hecha
   - Mejor un feature completo que 10 incompletos

---

## 📞 CONTACTO Y COMUNIDAD (Futuro)

- **Website:** calculanomina.co (dominio a comprar)
- **GitHub:** github.com/tuusuario/calculanomina
- **Email:** soporte@calculanomina.co
- **Discord:** Comunidad de usuarios y desarrolladores
- **Twitter/X:** @CalculaNomina

---

## 📝 NOTAS IMPORTANTES

- Este roadmap es una **guía flexible**, no un contrato
- Las fechas pueden ajustarse según recursos y feedback
- El modelo freemium se implementa solo cuando haya suficientes usuarios
- La calidad siempre antes que la velocidad
- Escuchar a los usuarios es clave para priorizar features

---

**Última actualización:** Enero 2026  
**Versión actual:** v1.0  
**Próxima versión:** v2.0 (Q1 2026)

---

🚀 **¡Vamos a construir la mejor plataforma de gestión laboral de Colombia!**
