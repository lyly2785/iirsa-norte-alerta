🛣️ IIRSA Norte Alerta
<div align="center">
<!-- IIRSA Norte brand header -->
<img src="https://img.shields.io/badge/IIRSA%20NORTE-Concesi%C3%B3n%20Vial-385E9D?style=for-the-badge&labelColor=385E9D&color=F1BE48" alt="IIRSA Norte"/>
<img src="https://img.shields.io/badge/Estado-Prototipo%20v1.0-F1BE48?style=for-the-badge&labelColor=1e293b&color=F1BE48" alt="Estado"/>
<img src="https://img.shields.io/badge/ISO%209001-2025-385E9D?style=for-the-badge&labelColor=1e293b&color=41B6E6" alt="ISO 9001"/>
<img src="https://img.shields.io/badge/CCO%20%2B%20OSITRAN-Integrado-97D700?style=for-the-badge&labelColor=1e293b&color=97D700" alt="OSITRAN"/>
<br/><br/>
Aplicación móvil para el reporte ciudadano de incidencias viales, integrada con el Centro de Control de Operaciones (CCO) de IIRSA Norte y la plataforma regulatoria de OSITRAN.
Paita → Olmos → Jaén → Bagua → Tarapoto → Yurimaguas · 971 km · 5 regiones
<br/>
🗺️ Ver App Demo · 📊 Ver Flujograma · 📄 Procedimiento ISO 9001
</div>
---
📋 Descripción del Proyecto
IIRSA Norte Alerta es una iniciativa de transformación digital del corredor vial más extenso del norte del Perú, desarrollada en el marco del piloto de Gemelo Digital BIM/GIS de IIRSA Norte y el programa de modernización de supervisión de OSITRAN.
El sistema integra tres capas de gestión:
Capa	Descripción
📱 App Ciudadana	Reporte de incidencias por ciudadanos, PNP y personal de la concesionaria
🎛️ Panel CCO	Dashboard en tiempo real para el Centro de Control de Operaciones
📡 API OSITRAN	Integración automática REST + WebSocket con la plataforma regulatoria
---
🗺️ Demo Interactivo
> Abrir directamente en el navegador, sin instalación:
Recurso	Enlace	Descripción
📱 App Prototipo v1.0	Abrir demo	Mockup interactivo completo con 5 pantallas
📊 Flujograma PG-INP-001	Abrir flujograma	Swimlane interactivo ISO 9001:2025
📄 Procedimiento Word	Descargar .docx	Documento controlado — 10 secciones
---
✨ Funcionalidades
Versión 1.0 — Prototipo Funcional (en desarrollo)
[x] 🗺️ Mapa interactivo de la ruta IIRSA Norte (Paita–Yurimaguas)
[x] ⚠️ Reporte de incidencias con GPS automático, foto y video
[x] 👤 Perfiles diferenciados: Ciudadano · PNP/Comisaría · Concesionaria
[x] 🎛️ Panel CCO web con visualización de eventos en tiempo real
[x] 📡 Integración API OSITRAN (REST + WebSocket)
[x] 📊 Dashboard Power BI con KPIs de gestión
[x] 📄 Procedimiento de Gestión PG-INP-001 (ISO 9001:2025)
Versión 2.0 — Plataforma Inteligente (roadmap Q4 2026)
[ ] 🔔 Push Notifications geolocalizadas — Alertas proactivas a usuarios en radio de 20 km · Firebase Cloud Messaging
[ ] 🎤 Editor de Voz STT — Reporte por dictado de voz sin necesidad de escribir · Google Speech API + Whisper offline
[ ] ⛽ Directorio de servicios en ruta — Grifos, restaurantes, hoteles, talleres mecánicos
[ ] 🔗 Sync Gemelo Digital BIM/GIS — Eventos georeferenciados en modelo 3D del corredor
[ ] 🤖 IA predictiva de zonas de riesgo — Análisis histórico de incidencias recurrentes
[ ] 🌐 Portal de transparencia ciudadana — Estadísticas públicas de respuesta operativa
---
🏗️ Arquitectura del Sistema
```
┌─────────────────────────────────────────────────────────────┐
│  USUARIOS (Ciudadano · PNP · Concesionaria)                 │
│  App Móvil iOS + Android  ←→  GPS · Cámara · Voz (v2)      │
└──────────────────────┬──────────────────────────────────────┘
                       │ REST API + WebSocket
┌──────────────────────▼──────────────────────────────────────┐
│  BACKEND  (Node.js / FastAPI)                               │
│  PostgreSQL + PostGIS · Socket.io · S3 Storage              │
└──────────┬──────────────────────┬───────────────────────────┘
           │                      │
┌──────────▼──────────┐  ┌───────▼──────────────────────────┐
│  PANEL CCO (Web)    │  │  API OSITRAN                      │
│  React + MapLibre   │  │  POST /eventos · GET /via-estado  │
│  Dashboard en t.r.  │  │  WebSocket stream · GMAO Central  │
└─────────────────────┘  └───────────────────────────────────┘
                                   │
┌──────────────────────────────────▼───────────────────────────┐
│  GEMELO DIGITAL BIM/GIS  (v2.0)                              │
│  Modelo 3D corredor · GMAO · Dashboard Power BI · MTC        │
└──────────────────────────────────────────────────────────────┘
```
---
📐 Stack Tecnológico
Componente	Tecnología	Versión
App Móvil	React Native + Expo	v50+
Mapas	MapLibre GL JS	v4+
Backend API	FastAPI (Python)	v0.110+
Base de datos	PostgreSQL + PostGIS	v16
Tiempo real	Socket.io	v4+
Panel CCO	React + MapLibre	v18+
Almacenamiento	AWS S3 / Cloudflare R2	—
Autenticación	JWT + Bearer Token	—
Voz STT (v2)	Whisper (offline) + Google Speech	—
Push (v2)	Firebase Cloud Messaging (FCM)	—
Analytics	Power BI Embedded	—
---
🗂️ Estructura del Repositorio
```
iirsa-norte-alerta/
├── README.md
├── iirsa_norte_alerta_app.html          ← Demo prototipo app
├── Flujograma_PG-INP-001_IIRSA_Norte_Alerta.html  ← Flujograma ISO
├── PG-INP-001_Procedimiento_Gestion_Incidencias_IIRSA_Norte_Alerta.docx
├── /app/                                ← Código React Native (próximo)
├── /backend/                            ← API REST + WebSocket (próximo)
├── /cco-panel/                          ← Dashboard CCO web (próximo)
├── /powerbi/                            ← Archivos .pbix KPIs (próximo)
├── /docs/
│   ├── procedimientos/
│   └── flujogramas/
└── /infrastructure/                     ← Docker Compose / Terraform
```
---
📊 KPIs del Proceso (ISO 9001:2025)
Indicador	Meta	Frecuencia
Tiempo de Respuesta Promedio	< 18 min	Mensual
TR Eventos Graves	< 5 min	Mensual
Tasa de Notificación a OSITRAN	> 98%	Mensual
Disponibilidad del Sistema	> 99.5%	Mensual
Reportes Ciudadanos Válidos	> 70%	Mensual
---
🗓️ Roadmap
```
Q2 2026  ──────────────────────────────────────────  Q4 2026
   │                                                     │
   ▼  v1.0 — Prototipo Funcional                        ▼  v2.0 — Plataforma Inteligente
   • App iOS + Android                                   • Push Notifications (FCM)
   • GPS + Foto + Texto                                  • Voz STT (Whisper)
   • Perfiles: Ciudadano/PNP/Conc.                       • Directorio de servicios
   • Panel CCO web tiempo real                           • Gemelo Digital BIM/GIS sync
   • API OSITRAN (REST + WS)                             • IA predictiva zonas riesgo
   • Power BI básico                                     • Portal transparencia ciudadana
```
---
📎 Documentación Relacionada
📋 PG-INP-001 — Procedimiento de Gestión de Incidencias
🗺️ Flujograma Swimlane — ISO 9001:2025
🏗️ Presentación Gemelo Digital IIRSA Norte Rev. 4 (repositorio privado)
📡 Reunión Proinversión 31/03/2026 — Piloto GMAO Central (acceso restringido)
---
🤝 Contribuciones
Las contribuciones al prototipo son bienvenidas. Por favor:
Crea un fork del repositorio
Crea una rama `feature/nombre-de-la-funcionalidad`
Realiza tus cambios con commits descriptivos
Abre un Pull Request con descripción clara del cambio
> Para cambios en documentación ISO o procedimientos, contactar directamente a la coordinación del proyecto.
---
📞 Contacto del Proyecto
<div align="center">
	
Responsable	Liliana Bayona
Cargo	Coordinación de Gestión Documental — Ingeniería de Nuevos Proyectos
Organización	IIRSA Norte — Concesión Vial
Correo	lbayona@iirsanorte.com.pe
</div>
---
<div align="center">
<sub>
---
💊 Desarrollado con metodología y visión digital por
vitaminas_tecnológicas
Transformación digital · Gestión del conocimiento · Innovación en infraestructura vial
---
Proyecto enmarcado en el Plan Gemelo Digital BIM/GIS de IIRSA Norte · OSITRAN · ISO 9001:2025
© 2026 IIRSA Norte S.A. — Todos los derechos reservados
</sub>
</div>
