# PhishGuard Labs

**PhishGuard Labs** es una aplicación de escritorio para portafolio creada con **Electron + React + Vite**. Simula un laboratorio básico de análisis SOC junior para detectar señales de phishing en correos, mensajes o URLs sospechosas.

La app funciona de manera local, sin API externa, y guarda el historial de casos en el equipo del usuario mediante Electron IPC.

---

## Funciones incluidas

- Analizador de phishing para correos, SMS, WhatsApp o URLs.
- Scoring de riesgo de 0 a 100.
- Clasificación: Bajo, Medio, Alto o Crítico.
- Detección de indicadores:
  - urgencia psicológica,
  - solicitud de credenciales,
  - enlaces HTTP,
  - acortadores,
  - dominios sospechosos,
  - adjuntos peligrosos,
  - posible suplantación de marca,
  - tono amenazante.
- Recomendaciones de respuesta ante incidentes.
- Historial local de casos tipo SOC.
- Dashboard con métricas de riesgo.
- Exportación de casos en JSON.
- Sección de presentación del proyecto para portafolio.

---

## Tecnologías

- Electron
- React
- Vite
- JavaScript
- HTML/CSS
- Persistencia local con JSON en `userData`

---

## Requisitos

Necesitás tener instalado:

- Node.js LTS, recomendado Node 20 o superior.
- npm.
- Visual Studio Code.

Para verificar:

```bash
node -v
npm -v
```

---

## Cómo ejecutar en VS Code

Abrí la carpeta del proyecto en VS Code y ejecutá:

```bash
npm install
npm run dev
```

Eso abre la app en modo desarrollo con Electron.

---

## Cómo detener la app

En la terminal donde está corriendo:

```bash
Control + C
```

En Mac también podés cerrar la ventana de Electron normalmente.

---

## Cómo generar instalador

Para crear una versión instalable:

```bash
npm run dist
```

El instalador aparecerá en la carpeta:

```txt
release/
```

En Mac genera `.dmg`, en Windows genera instalador `.exe` si lo corrés desde Windows, y en Linux genera `.AppImage`.

---

## Comando de revisión rápida

```bash
npm run lint:quick
```

Este comando verifica que los archivos principales existan.

---

## Estructura

```txt
phishguard-labs/
├── electron/
│   ├── main.cjs
│   └── preload.cjs
├── src/
│   ├── components/
│   │   ├── About.jsx
│   │   ├── Analyzer.jsx
│   │   ├── CasesTable.jsx
│   │   └── Dashboard.jsx
│   ├── lib/
│   │   └── analyzer.js
│   ├── App.jsx
│   ├── main.jsx
│   └── style.css
├── data/
│   └── demo_cases.json
├── scripts/
│   └── quick-check.cjs
├── index.html
├── package.json
└── README.md
```

---

## Texto para usar en LinkedIn o portafolio

**PhishGuard Labs** es una aplicación de escritorio de ciberseguridad desarrollada con Electron, React y Vite. Permite analizar correos, mensajes y enlaces sospechosos para detectar indicadores de phishing, calcular un score de riesgo y generar recomendaciones de respuesta. El proyecto simula una herramienta básica de apoyo para un analista SOC junior, incorporando dashboard, historial de casos y persistencia local.

---

## Posibles mejoras futuras

- Integrar una API de IA para explicación avanzada.
- Exportar reportes PDF por incidente.
- Agregar estado de tickets: abierto, investigando, cerrado.
- Añadir lista blanca y lista negra de dominios.
- Agregar modo educativo con ejercicios de phishing.
- Crear login admin para simular uso empresarial.
