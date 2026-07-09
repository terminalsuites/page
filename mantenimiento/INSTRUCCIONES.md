# Reportes de Mantenimiento — Terminal Suites

## 📋 Cómo funciona

Esta carpeta contiene todos los reportes mensuales del plan de mantenimiento web.

**URL para compartir con la clienta:**
```
https://terminalsuites.com.ar/mantenimiento/
```

Ella accede a ese link y ve un listado profesional con todos los reportes disponibles.

---

## 📁 Estructura de archivos

```
mantenimiento/
├── index.html                          # Portada: listado de reportes
├── reporte-setup-julio2026.html         # Reporte del mes (setup inicial)
├── reporte-agosto2026.html              # Próximo reporte
├── propuesta-mantenimiento-dark.html    # Propuesta original (referencia)
└── INSTRUCCIONES.md                     # Este archivo
```

---

## 🔄 Cómo agregar un nuevo reporte cada mes

### **Paso 1: Crear el reporte HTML**

1. Usa `reporte-setup-julio2026.html` como plantilla
2. Crea un nuevo archivo: `reporte-MESAÑO.html`
   - Ejemplo: `reporte-agosto2026.html`
3. Actualiza:
   - El título: `<title>Reporte Agosto 2026 — Terminal Suites</title>`
   - El header: cambiar "Mes 0" por "Agosto 2026"
   - El período en `<div class="meta">`
   - El contenido: datos reales de GA4, cambios hechos, etc.

**Mantén:**
- El mismo diseño y estilos (CSS)
- El mismo footer con fecha dinámica
- La estructura de secciones

### **Paso 2: Actualizar el index.html**

Abre `index.html` y encuentra esta sección:

```javascript
const reports = [
  {
    id: 'setup-julio2026',
    title: 'Mes 0 — Configuración Inicial',
    date: 'julio 2026',
    desc: 'Instalación de herramientas de medición...',
    file: 'reporte-setup-julio2026.html',
    status: 'setup'
  },
  // Agrega AQUÍ el nuevo reporte
];
```

**Copia y pega, reemplazando los datos:**

```javascript
{
  id: 'agosto2026',
  title: 'Agosto 2026',
  date: 'agosto 2026',
  desc: 'Primer reporte completo con datos reales de visitas, fuentes de tráfico y conversiones.',
  file: 'reporte-agosto2026.html'
}
```

### **Paso 3: Versionar en Git**

```bash
cd "Terminal Suites"
git add mantenimiento/
git commit -m "Agregar reporte de agosto 2026"
git push
```

**Listo.** El reporte está online automáticamente en `terminalsuites.com.ar/mantenimiento/`

---

## 📝 Qué incluir en cada reporte

### Estructura recomendada:

1. **Header** — Mes/período y datos básicos (Para, De, Fecha)
2. **Resumen de lo hecho** — Cambios, actualizaciones, mantenimiento realizado
3. **Métricas** — Datos de GA4:
   - Visitas totales
   - Usuarios únicos
   - Fuentes de tráfico (Google, Instagram, directo)
   - Páginas más visitadas
   - Tasa de conversión (quién consulta/reserva)
4. **Recomendaciones** — Qué mejorar según los datos
5. **Próximos pasos** — Qué hacer el mes que viene
6. **Footer** — Contacto y fecha dinámica

---

## 🎯 Datos de GA4 para copiar cada mes

Accede a:
- **Google Analytics**: `analytics.google.com` → Terminal Suites
- **Período**: mes anterior completo
- **Métricas clave**:
  - Usuarios (Sessions → Users)
  - Fuentes de tráfico (Acquisition → Overview)
  - Páginas principales (Engagement → Pages and Screens)
  - Conversiones (Conversion → All events)

---

## 📧 Cómo compartir con la clienta

**Por WhatsApp o email:**
```
Hola Pau, acá está tu reporte de agosto:
https://terminalsuites.com.ar/mantenimiento/

Dentro encontrás todos los datos de visitas, de dónde llega la gente y cuántos consultaron.
```

---

## 🚀 Flujo mensual recomendado

```
Día 1-25 del mes:   Trabaja en cambios y mantenimiento
Día 25-30:          Recolecta datos de GA4
Día 30-1:           Arma el reporte del mes
Día 1-3 sig. mes:   Subes a GitHub y le mandas el link a la clienta
```

---

## 💡 Tips

- **Mantén el diseño consistente** — todos los reportes deben verse igual
- **Usa números reales** — más impacto que datos ficticios
- **Agrega recomendaciones** — no solo números, sino qué hacer con esa info
- **Fecha dinámica** — el footer se actualiza solo, no toques `<span id="currentDate">`
- **Imágenes opcionales** — si quieres agregar gráficos, pueden ser tablas HTML o capturas

---

## 📞 Contacto

Si hay dudas con GA4, estructura o datos, preguntale al desarrollador.

**Teo Cicciari**
- WhatsApp: +54 9 2944 81-2580
- Email: teocicciari@gmail.com
