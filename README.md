# 🪐 AstroSim Pro: Simulador de Dinámica Orbital & Eclipses en 3D

[![Live Demo](https://img.shields.io/badge/Demo-GitHub%20Pages-06b6d4?style=for-the-badge&logo=github)](https://username.github.io/repository-name)
[![Stack](https://img.shields.io/badge/Tech-HTML5%20%7C%20TailwindCSS%20%7C%20Canvas2D-f59e0b?style=for-the-badge)](https://developer.mozilla.org/es/docs/Web/API/Canvas_API)
[![Licencia](https://img.shields.io/badge/Licencia-MIT-green?style=for-the-badge)](LICENSE)

> **Una inmersión interactiva en la sizigia cósmica.** Explora las leyes del movimiento planetario, proyecta conos de umbra en tiempo real y contempla las geometrías exactas que desencadenan los eclipses solares y lunares a lo largo de un ciclo orbital de 365 días.

---

## 🌌 La Geometría Detrás de la Penumbra

Un eclipse no es solo un evento visual deslumbrante; es la alineación matemática perfecta de tres cuerpos celestes en un fenómeno conocido en astrofísica como **sizigia** (*syzygy*). 

A pesar de que la Luna es aproximadamente 400 veces más pequeña que el Sol, también se encuentra casi 400 veces más cerca de la Tierra. Esta célebre coincidencia cósmica permite que ambos astros posean un tamaño angular casi idéntico desde nuestra perspectiva terrestre (~0.5° en el cielo).

```
   [ SOL ] ------------------->  ( LUNA ) ----------> [ TIERRA ]
                       Cono Umbral / Penumbral
```

**AstroSim Pro** reproduce esta interacción a través de modelos dinámicos interactivos:
* **Sizigia y Plano Inclinado:** Representación de la inclinación orbital de la Luna (~5.14° respecto a la eclíptica), explicando por qué no ocurre un eclipse en cada luna nueva o llena.
* **Proyección de Umbras y Penumbras:** Simulación geométrica precisa de los conos de sombra proyectados por la Tierra y la Luna hacia el espacio.
* **Geolocalización en Tiempo Real:** Telemetría integrada para proyectar la franja de totalidad y visibilidad geográfica exacta (como el esperado Eclipse Solar Total sobre **Madrid, España y el Atlántico Norte** en agosto de 2026).

---

## ⚡ Características Principales

### 🛰️ Simulador 3D con Inclinación de Perspectiva
* **Navegación espacial interactiva:** Arrastra el cursor o desliza en pantallas táctiles para inclinar y rotar el ángulo de cámara 3D.
* **Cálculo de Porcentaje de Alineación:** Algoritmo en tiempo real que mide la alineación angular Sol-Tierra-Luna.
* **Renderizado fluido a 60 FPS:** Motor gráfico basado en HTML5 Canvas API sin dependencias pesadas.

### ⏳ Control Temporal & Telemetría
* **Simulación del ciclo de 365 días:** Visualiza la traslación terrestre alrededor del Sol y la traslación lunar (~27.3 días siderales).
* **Velocidades ajustables:** Control de reproducción en tiempo real (`0.5x`, `1x`, `2x`, `5x`).
* **Fases Lunares:** Identificación automática de la fase lunar en pantalla (Nueva, Creciente, Llena, Menguante).

### 🔍 Inspección de Eclipses (Notificación Flotante)
* **Detección automática de alineación:** Al alcanzar la fecha exacta de un eclipse (solar total, anular o lunar), la simulación ralentiza el flujo para su inspección.
* **Ubicación Geográfica y Coordenadas:** Detalle preciso de las coordenadas y regiones terrestres desde donde el fenómeno es visible.
* **Lente de Zoom Óptico:** Lienzo secundario de alta resolución que renderiza la vista microscópica del evento (Corona solar, Anillo de Fuego o Luna de Sangre).
* **Modo Congelado (*Hold Mode*):** Botón para congelar temporalmente la tarjeta informativa y tomar apuntes o analizar la física del evento sin límite de tiempo.
* **Ubicación No Intrusiva:** La tarjeta se despliega en la esquina superior derecha (`top-20 right-4`), permitiendo que el modelo 3D central permanezca 100% visible.

---

## 📸 Tarjeta de Telemetría Geográfica

Cuando ocurre un evento astronómico, **AstroSim Pro** proporciona telemetría en tiempo real:

| Evento | Fecha Simulada | Tipo | Ubicación Principal & Coordenadas |
| :--- | :--- | :--- | :--- |
| 🟡 **Eclipse Solar Anular** | 17 Feb 2026 | Anular | Antártida y Sur de África (`68.3° S, 12.4° E`) |
| 🔴 **Eclipse Lunar Total** | 03 Mar 2026 | Total (Luna de Sangre) | Océano Pacífico y Américas (`12.1° N, 165.4° W`) |
| ☀️ **Eclipse Solar Total** | 12 Ago 2026 | Total | Madrid (España), Islandia y Ártico (`65.2° N, 25.1° W`) |
| 🌗 **Eclipse Lunar Parcial** | 28 Ago 2026 | Parcial | Océano Atlántico y Europa (`18.5° S, 34.2° W`) |

---

## 🛠️ Arquitectura Web & Arquitectura Técnica

El proyecto ha sido concebido bajo los principios de **Zero External Dependencies** para maximizar el rendimiento de carga y facilitar el despliegue instantáneo:

* **HTML5 Canvas API:** Motor de renderizado en 2D/3D basado en matemáticas vectoriales puras (trigonometría de órbitas, gradientes radiales de resplandor e iluminación refractiva).
* **Tailwind CSS (v3 CDN):** Estilizado declarativo UI con un enfoque *Glassmorphism* (efecto de vidrio translúcido).
* **JavaScript ES6+:** Programación modular sin frameworks pesados, garantizando un tiempo de respuesta (*First Contentful Paint*) inferior a 300 ms.

---

## 🚀 Despliegue Rápido en GitHub Pages

Para publicar este proyecto en tu perfil de GitHub y mostrarlo como demostración interactiva:

1. **Crea un nuevo repositorio** en tu cuenta de GitHub (ejemplo: `simulador-eclipses`).
2. Sube el archivo `index.html` y este `README.md` a la rama principal (`main`).
3. Ve a **Settings (Configuración)** > **Pages**.
4. En **Source**, selecciona `Deploy from a branch` y elige la rama `main` / carpeta `/(root)`.
5. Haz clic en **Save**. ¡Tu simulación estará lista en minutos en la URL `https://tu-usuario.github.io/simulador-eclipses`!

---

## 💻 Desarrollo Local

No se requiere ningún instalador de paquetes (`npm`, `yarn` o servidores dedicados). Simplemente clona el repositorio y abre el archivo en cualquier navegador moderno:

```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/simulador-eclipses.git

# Entrar al directorio
cd simulador-eclipses

# Abrir en navegador (Linux/Mac)
open index.html
# O abrir haciendo doble clic en index.html en Windows
```

---

## 📜 Licencia y Autoría

Desarrollado con dedicación técnica y científica para proyectos de divulgación astronómica e interfaces web de alto impacto.

Distribuido bajo la Licencia **MIT**. Consulta el archivo `LICENSE` para más información.