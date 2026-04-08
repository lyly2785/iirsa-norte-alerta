# IIRSA Norte Alerta

<div align="center">

<img src="./logo.jfif" height="90" alt="IIRSA Norte — Concesión Vial" /><br/><br/>

<img src="https://img.shields.io/badge/IIRSA%20NORTE-Concesi%C3%B3n%20Vial-385E9D?style=for-the-badge&labelColor=385E9D&color=F1BE48"/>
<img src="https://img.shields.io/badge/Prototipo-v1.0-F1BE48?style=for-the-badge&labelColor=1e293b&color=F1BE48"/>
<img src="https://img.shields.io/badge/ISO%209001-2025-41B6E6?style=for-the-badge&labelColor=1e293b&color=41B6E6"/>
<img src="https://img.shields.io/badge/CCO%20%2B%20OSITRAN-Integrado-97D700?style=for-the-badge&labelColor=1e293b&color=97D700"/>

<br/><br/>

<p align="justify">
Aplicación móvil para el reporte ciudadano de incidencias viales, integrada con el <strong>Centro de Control de Operaciones (CCO)</strong> de IIRSA Norte y la plataforma regulatoria de <strong>OSITRAN</strong>. Desarrollada en el marco del piloto de Gemelo Digital BIM/GIS y el programa de modernización de supervisión del corredor vial más extenso del norte del Perú.
</p>

<p><em>Paita → Olmos → Jaén → Bagua → Tarapoto → Yurimaguas · 971 km · 5 regiones</em></p>

<br/>

[📱 Ver App Demo](https://lyly2785.github.io/iirsa-norte-alerta/iirsa_norte_alerta_app.html) · [📊 Ver Flujograma](https://lyly2785.github.io/iirsa-norte-alerta/Flujograma_PG-INP-001_IIRSA_Norte_Alerta.html) · [🌐 Landing Page](https://lyly2785.github.io/iirsa-norte-alerta/) · [📄 Procedimiento](./PG-INP-001_Procedimiento_Gestion_Incidencias_IIRSA_Norte_Alerta.docx)

</div>

---

## 📋 Descripción del Proyecto

<p align="justify">
<strong>IIRSA Norte Alerta</strong> es una iniciativa de transformación digital del corredor vial más extenso del norte del Perú, desarrollada en el marco del piloto de <strong>Gemelo Digital BIM/GIS</strong> de IIRSA Norte y el programa de modernización de supervisión de OSITRAN. El sistema garantiza la trazabilidad completa de cada incidencia vial desde su detección hasta el cierre y notificación regulatoria, integrando tres capas de gestión.
</p>

| Capa | Descripción |
|------|-------------|
| 📱 **App Ciudadana** | Reporte de incidencias por ciudadanos, PNP y personal de la concesionaria |
| 🎛️ **Panel CCO** | Dashboard en tiempo real para el Centro de Control de Operaciones |
| 📡 **API OSITRAN** | Integración automática REST + WebSocket con la plataforma regulatoria |

---

## 🗺️ Demo Interactivo

> Todos los recursos se abren directamente en el navegador, sin instalación.

| Recurso | Enlace | Descripción |
|---------|--------|-------------|
| 📱 App Prototipo v1.0 | [Abrir demo](https://lyly2785.github.io/iirsa-norte-alerta/iirsa_norte_alerta_app.html) | Mockup interactivo con 5 pantallas navegables |
| 📊 Flujograma PG-INP-001 | [Abrir flujograma](https://lyly2785.github.io/iirsa-norte-alerta/Flujograma_PG-INP-001_IIRSA_Norte_Alerta.html) | Swimlane interactivo ISO 9001:2025 |
| 🌐 Landing Page | [Abrir página](https://lyly2785.github.io/iirsa-norte-alerta/) | Página de presentación del proyecto |
| 📄 Procedimiento Word | [Descargar .docx](./PG-INP-001_Procedimiento_Gestion_Incidencias_IIRSA_Norte_Alerta.docx) | Documento controlado — 10 secciones |

---

## ✨ Funcionalidades

### Versión 1.0 — Prototipo Funcional *(Q2 2026)*

- [x] 🗺️ Mapa interactivo de la ruta IIRSA Norte (Paita–Yurimaguas)
- [x] ⚠️ Reporte de incidencias con GPS automático, foto y video
- [x] 👤 Perfiles: Ciudadano · PNP/Comisaría · Concesionaria
- [x] 🎛️ Panel CCO web con visualización en tiempo real
- [x] 📡 Integración API OSITRAN (REST + WebSocket)
- [x] 📊 Dashboard Power BI con KPIs de gestión
- [x] 📄 Procedimiento PG-INP-001 (ISO 9001:2025)

### Versión 2.0 — Plataforma Inteligente *(Q4 2026)*

- [ ] 🔔 **Push Notifications geolocalizadas** — Radio 20 km · Firebase Cloud Messaging
- [ ] 🎤 **Editor de Voz STT** — Dictado sin escribir · Whisper offline + Google Speech API
- [ ] ⛽ **Directorio de servicios en ruta** — Grifos, restaurantes, hoteles, talleres
- [ ] 🔗 **Sync Gemelo Digital BIM/GIS** — Eventos en modelo 3D del corredor
- [ ] 🤖 **IA predictiva de zonas de riesgo**
- [ ] 🌐 **Portal de transparencia ciudadana**

---

## 🏗️ Arquitectura

```
USUARIOS (Ciudadano · PNP · Concesionaria)
         App Móvil iOS + Android
                  │ REST + WebSocket
         BACKEND (FastAPI · PostGIS)
         ┌────────┴────────┐
    Panel CCO          API OSITRAN
    React + Leaflet    POST/GET endpoints
                  │
         GEMELO DIGITAL BIM/GIS (v2)
         GMAO Central · Power BI · MTC
```

---

## 📊 KPIs — ISO 9001:2025

| Indicador | Meta | Frecuencia |
|-----------|------|------------|
| Tiempo de Respuesta Promedio | < 18 min | Mensual |
| TR Eventos Graves | < 5 min | Mensual |
| Tasa Notificación OSITRAN | > 98% | Mensual |
| Disponibilidad del Sistema | > 99.5% | Mensual |
| Reportes Ciudadanos Válidos | > 70% | Mensual |

---

## 🗓️ Roadmap

```
Q2 2026 ──────────────────────────── Q4 2026
v1.0 Prototipo Funcional    v2.0 Plataforma Inteligente
• App iOS + Android          • Push Notifications (FCM)
• GPS + Foto + Texto         • Voz STT (Whisper)
• Panel CCO + API OSITRAN    • Gemelo Digital BIM/GIS
• Power BI KPIs              • IA predictiva de riesgos
```

---

## 📞 Contacto

<div align="center">

<img src="./logo.jfif" height="60" alt="IIRSA Norte" /><br/><br/>

| Campo | Detalle |
|-------|---------|
| **Responsable** | Liliana Bayona |
| **Cargo** | Coordinación de Gestión Documental — Ingeniería de Nuevos Proyectos |
| **Organización** | IIRSA Norte — Concesión Vial |
| **Correo** | [lbayona@iirsanorte.com.pe](mailto:lbayona@iirsanorte.com.pe) |
| **GitHub** | [lyly2785/iirsa-norte-alerta](https://github.com/lyly2785/iirsa-norte-alerta) |

</div>

---

<div align="center">
<sub>

💊 Desarrollado con metodología y visión digital por **vitaminas_tecnológicas**

*Transformación digital · Gestión del conocimiento · Innovación en infraestructura vial*

© 2026 IIRSA Norte S.A. · ISO 9001:2025 · PG-INP-001 Rev.01

</sub>
</div>
