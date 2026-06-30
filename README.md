# 🪐 Slate — Spatial Research Canvas

Slate es una herramienta de investigación espacial y organización visual basada en un **lienzo infinito interactivo**. Diseñada para investigadores, estudiantes y desarrolladores, permite estructurar notas complejas, interconectar ideas y organizar recursos multimedia dentro de un entorno estético y de alto rendimiento.

El proyecto destaca por no depender de pesadas bases de datos tradicionales, implementando en su lugar un **motor de serialización estructurado propio (`.slate`)** que opera directamente sobre el almacenamiento local del navegador.

![Licencia](https://img.shields.io/badge/license-MIT-blue.svg)
![Frontend](https://img.shields.io/badge/frontend-HTML5%20%7C%20TailwindCSS%20%7C%20VanillaJS-orange)

---

## ✨ Características Principales

### 🧠 El Lienzo Infinito (`Lienzo`)
* **Navegación Fluida:** Paneado ultra-responsivo mediante arrastre dinámico y zoom milimétrico con la rueda del ratón.
* **Alineación Magnética (`Snap-to-Grid`):** Guías inteligentes visuales que facilitan la organización limpia y simétrica de los bloques de información.
* **Conexiones Dinámicas:** Generación automática de curvas de Bézier nativas en SVG para trazar relaciones lógicas e hilos conductores entre nodos.

### 🎛️ Modos de Trabajo
* **Estudio de Canvases:** Un centro de control (*Hub*) integrado para administrar, clonar, renombrar y previsualizar estadísticas avanzadas de múltiples espacios de trabajo simultáneos.
* **Modo Monolith (Escritura Pura):** Entorno inmersivo de pantalla completa optimizado para la concentración de flujo libre. Incluye contador de palabras en tiempo real y guardado automático instantáneo.

### 🎨 Estética de Vanguardia
* La interfaz implementa un enfoque de **Playful Minimalism** y **Neo-Brutalismo sofisticado**, utilizando efectos de desenfoque de cristal (*iOS-like glassmorphism*), paletas de acento monocromáticas y un fondo oscuro con gradientes ambientales sutiles para reducir la fatiga visual.

---

## 🛠️ Arquitectura Técnica e Ingeniería

### Motor de Serialización Físico Nativo (`.slate`)
En lugar de depender de formatos genéricos de transferencia de datos desestructurados, Slate introduce un protocolo de estructura física personalizado para empaquetar de forma segura texto enriquecido, coordenadas geográficas en pantalla y recursos binarios. 

Un archivo plano `.slate` parseado nativamente por la aplicación sigue la siguiente especificación:

```text
### SLATE PHYSICAL STRUCTURE PROTOCOL v2.0 ###
METADATA::NAME::[Base64_Project_Name]
METADATA::EXPORT_DATE::[ISO_Timestamp]
METADATA::ENGINE_HASH::[Unique_Hex_Hash]

### START ENTITY LAYERS (BLOCKS) ###
BLOCK_ID::b_1719770000000
  TYPE::text
  COLOR::color-blue
  COORD_X::320
  COORD_Y::150
  METATAG::W0lERUFd
  HEADLINE::VGl0dWxvIGRlIGxhIElkZWE=
  MARKDOWN_BODY::Q29udGVuaWRvIGVuIG1hcmtkb3du...
  BINARY_RESOURCE::NULL_RESOURCE
END_BLOCK
### END ENTITY LAYERS ###

### START LOGICAL MAPPINGS (CONNECTIONS) ###
MAP_EDGE::b_1719770000000==>>b_1719770888888
### END LOGICAL MAPPINGS ###
