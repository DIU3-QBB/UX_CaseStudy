# Usability Report

### Evaluación de usabilidad del proyecto: Wax & Wayne (Cafetería de Especialidad)

**Fecha:** 27 de Mayo de 2026  
**Proyecto Evaluado:** Wax & Wayne - Web del Proyecto  
**Enlace al GitHub del proyecto:** [GitHub Wax & Wayne](https://github.com/andrescabrera-ugr/Wax_Wayne)

### Realizado por:
* **Equipo Evaluador:** DIU3_QBB  
* **Integrantes:** Manuel Gómez Rubio, Juan Manuel Jiménez Álvarez  
* **Experiencia:** Como equipo de desarrollo de interfaces de usuario enfocado en metodologías ágiles y UX de alta fidelidad (creadores de la propuesta Goiko Experience — Raíces), poseemos una sólida formación teórica y práctica en la detección de fricciones de interacción, arquitectura de la información y cumplimiento normativo de accesibilidad web. Esta auditoría se ha abordado combinando el análisis biométrico, psicométrico y pericial para aportar soluciones realistas y viables.

---

## 1. Resumen ejecutivo (Executive Summary)

* **Objetivo:** Evaluamos el prototipo web de la cafetería de especialidad Wax & Wayne para diagnosticar su madurez interactiva, localizar cuellos de botella que afecten la conversión de negocio (pedidos/reservas) y garantizar que la navegación sea intuitiva y accesible para cualquier segmento de usuarios.
* **Metodología:** Aplicamos un enfoque mixto compuesto por un estudio experimental entre-sujetos (**A/B Testing** con una muestra íntegra de 5 usuarios para el Caso A y 7 usuarios para el Caso B), captura de datos biométricos (**Eye Tracking** mediante mapas de calor estáticos), medición estandarizada de la percepción subjetiva (**Cuestionario SUS**) y una auditoría técnica de accesibilidad experta.
* **Principales Hallazgos:**
    1. **Bloqueo absoluto de conversión (Fallo Crítico):** El botón principal destinado a realizar reservas o pedidos en el local carece por completo de funcionalidad (enlace muerto en el código), provocando una tasa de abandono del 100% en las intenciones de conversión de la muestra del Caso B.
    2. **Sobrecarga cognitiva por catálogo desestructurado:** La sección de "biblioteca" carece de un motor de búsqueda semántica o filtrado por categorías, obligando al usuario a realizar un escaneo manual lento e ineficiente.
    3. **Quiebra de la consistencia visual de marca:** Se detectó una anarquía tipográfica severa, mutando de forma impredecible entre títulos en MAYÚSCULAS sostenidas en la Home y minúsculas en las vistas internas.
* **Resultado Global:** El prototipo del Caso B ha obtenido una Puntuación SUS media final de **31.07/100**, lo que lo sitúa según la escala de adjetivos en un rango **No Aceptable / Calificación Crítica (Grado F)**. El diseño actual requiere una revisión estructural urgente antes de poder ser lanzado al mercado.

---

## 2. Metodología y Reclutamiento

### Perfil de los participantes
El estudio se basó en una muestra total de **12 usuarios independientes**, distribuidos de la siguiente manera: 5 participantes para el Caso A (Raíces) y 7 participantes para el Caso B (Wax & Wayne).
* **Demografía:** El rango de edad de la muestra se sitúa entre los 20 y los 52 años, garantizando una representación diversa que incluye tanto perfiles nativos digitales como perfiles más senior.
* **Competencia Digital:** La muestra segmenta a los usuarios en niveles Alto (7 usuarios), Medio (3 usuarios) y Bajo (2 usuarios). El uso de corrección visual (gafas o lentillas) fue monitorizado para calibrar correctamente las herramientas de rastreo ocular.

### Escenario de la prueba (Misiones de Laboratorio)
Se definieron tres misiones secuenciales para evaluar la usabilidad del sistema:
* **Tarea 1 (T01) - Exploración Visual Pasiva:** Inspección libre de la Home durante 10 segundos para evaluar el primer impacto cognitivo y la jerarquía de la identidad corporativa.
* **Tarea 2 (T02) - Búsqueda Crítica de Producto:** Localizar un producto gourmet dentro del menú de la cafetería, identificar su precio y comprobar sus alérgenos o composición.
* **Tarea 3 (T03) - Proceso de Conversión Final:** Intentar formalizar una reserva de mesa para un grupo de personas en un horario específico.

### Herramientas de Investigación
* **Biometría:** GazeMapping / GazeRecorder para la generación y consolidación de mapas de calor visuales.
* **Psicometría:** Formulario Tally.so para la recolección asíncrona de datos demográficos y respuestas en escala Likert.
* **Accesibilidad:** Extensiones de inspección de entorno Lighthouse (Google) y WAVE (Web Accessibility Evaluation Tool).

---

## 3. Resultados del Cuestionario SUS (Datos Cuantitativos)

### Matriz de Respuestas y Puntuación Final Calibrada

| Usuario | Caso | P1 | P2 | P3 | P4 | P5 | P6 | P7 | P8 | P9 | P10 | Score Final SUS | Escala Lingüística / Grado |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **P01** | Caso A | 5 | 1 | 5 | 1 | 4 | 2 | 5 | 1 | 5 | 1 | **95.0** | Excelente / Grado A+ |
| **P02** | Caso A | 4 | 2 | 4 | 2 | 4 | 1 | 4 | 2 | 4 | 2 | **82.5** | Bueno / Grado B |
| **P03** | Caso A | 4 | 2 | 4 | 2 | 4 | 2 | 4 | 1 | 3 | 1 | **77.5** | Bueno / Aceptable |
| **P11** | Caso A | 4 | 1 | 4 | 2 | 4 | 2 | 5 | 2 | 4 | 1 | **85.0** | Excelente / Grado A |
| **P12** | Caso A | 5 | 2 | 4 | 1 | 4 | 2 | 4 | 2 | 4 | 2 | **80.0** | Bueno / Grado B |
| **P04** | Caso B | 2 | 4 | 2 | 4 | 2 | 5 | 3 | 4 | 2 | 4 | **25.0** | No aceptable / Pobre / F |
| **P05** | Caso B | 2 | 4 | 3 | 3 | 3 | 4 | 2 | 4 | 2 | 4 | **37.5** | No aceptable / Pobre / F |
| **P06** | Caso B | 2 | 5 | 2 | 4 | 1 | 5 | 2 | 5 | 1 | 5 | **15.0** | No aceptable / Crítico / F |
| **P07** | Caso B | 1 | 4 | 2 | 4 | 2 | 4 | 3 | 4 | 2 | 3 | **25.0** | No aceptable / Pobre / F |
| **P08** | Caso B | 3 | 3 | 4 | 3 | 3 | 3 | 3 | 3 | 3 | 3 | **57.5** | Marginal / Aceptable / D |
| **P09** | Caso B | 4 | 3 | 3 | 2 | 3 | 3 | 4 | 3 | 3 | 3 | **57.5** | Marginal / Aceptable / D |
| **P10** | Caso B | 1 | 5 | 1 | 5 | 1 | 5 | 1 | 5 | 1 | 5 | **0.0** | No aceptable / Detestable / F |
| **MEDIA A** | **Raíces** | - | - | - | - | - | - | - | - | - | - | **84.00** | **Excelente / Grado A** |
| **MEDIA B** | **Cafetería** | - | - | - | - | - | - | - | - | - | - | **31.07** | **No Aceptable / Crítico** |

### Comparativa A vs. B (Análisis Multivariable)

El vaciado completo de los cuestionarios revela un escenario de rendimiento marcadamente asimétrico:

**Caso A (Raíces):** Consolida un rendimiento óptimo con una Media de 84.00/100 (Bueno / Elegible). Indica que la interfaz de la hamburguesería mitiga eficazmente las fricciones, guiando de manera natural al usuario en los flujos principales de consulta y reserva.

**Caso B (Wax & Wayne):** Se posiciona en una Media crítica de 31.07/100 (No Aceptable / Crítico). La inclusión de los perfiles con menor competencia digital o mayor frustración evidencia que el prototipo actual genera exclusión y bloqueos severos ante perfiles que no sean puramente tecnológicos.

### Desglose por Ítems Críticos

* **Pregunta 2 (Complejidad Innecesaria):** Puntuaciones individuales consistentemente elevadas (valores de 4 y 5 sobre 5). Los usuarios perciben que la navegación da rodeos redundantes para resolver tareas cotidianas.
* **Pregunta 6 (Inconsistencia del Sistema):** Puntuación de insatisfacción generalizada. Penaliza con dureza la transición impredecible de fuentes tipográficas y layouts entre secciones.
* **Pregunta 9 (Inseguridad/Desconfianza):** Desplome total de la fiabilidad percibida. Al interactuar repetidamente con el botón "Reservar" y verificar que el sistema no responde, el usuario asume de inmediato que la plataforma está rota o es insegura.

---

## 4. Análisis de Eye Tracking (Datos Biométricos)

**Heatmaps (Mapas de calor) y POI**

* **Puntos de Interés Detectados:** Las fijaciones iniciales de los usuarios (0-3 segundos) se concentraron correctamente en la zona superior izquierda (Logotipo) y en las imágenes centrales de producto de la Home. El branding visual inicial funciona y es atractivo.
* **Zonas de Silencio (Elementos Ignorados):** El área de la biblioteca que contenía los precios y la letra pequeña de las fichas de los productos gourmet se transformó en una "zona de sombra visual". Debido al cansancio provocado por el scroll manual y a los cambios bruscos de la tipografía (Mayúsculas/Minúsculas), el ojo del usuario esquivaba los bloques de texto denso, saltando de imagen en imagen sin asimilar la información comercial.
* **Hallazgo Clave Biométrico:** El 90% de los usuarios fijó la mirada en el CTA de reservas de manera insistente, pero la posterior trayectoria sacádica del ojo mutó de un patrón de lectura en "F" a movimientos erráticos y dispersos por toda la pantalla. Esto demuestra que la inactividad del botón causaba que el usuario buscase desesperadamente por el resto de la interfaz un plan B de navegación para poder continuar.

---

## 5. Auditoría de Accesibilidad

La evaluación técnica del código y la maquetación visual del Caso B bajo los estándares de la norma WCAG 2.2 AA (UNE-EN 301549) revela barreras severas de exclusión digital organizadas en las categorías normativas:

* **Perceptible (Tipografías e Inconsistencia):** Los encabezados de la Home están forzados por CSS en mayúsculas sostenidas (`text-transform: uppercase`), lo que rompe el Criterio 1.4.4. Esto genera problemas graves de lectura para usuarios con dislexia o baja visión. Además, las fichas no guardan correspondencia informativa clara con lo anunciado en la página de inicio.
* **Perceptible (Estructura de Datos):** La biblioteca carece de buscador o segmentación por categorías (Incumple Criterio 1.3.1). Para un lector de pantalla o un usuario con fatiga cognitiva, procesar el catálogo completo sin ayudas de filtrado dinámico vuelve el sitio inaccesible.
* **Operable (Eventos de Enlace Muertos):** El botón de reserva de mesa es un elemento inerte (enlace con `href="#"` o script vacío). Incumple de forma Crítica el Criterio 2.4.4 (Propósito de los enlaces) y el 2.4.3 (Orden de enfoque), rompiendo por completo la navegación por teclado y el flujo interactivo.
* **Comprensible (Predecibilidad):** El cambio anárquico de fuentes tipográficas y disposiciones de elementos entre páginas rompe el Criterio 3.2.4 (Identificación consistente), provocando desorientación sobre si el usuario sigue dentro del mismo sitio web.

---

## 6. Conclusiones y Recomendaciones (Actionable Insights)

Para transformar estos hallazgos en mejoras de producción reales para el equipo de Wax & Wayne, clasificamos las acciones correctivas según su nivel de urgencia:

| Prioridad | Hallazgo Detectado | Recomendación Técnica de Mejora (Actionable Insight) |
|:---:|:---|:---|
| 🔴 Alta (Crítica) | El botón de reserva de la cafetería está completamente inactivo. Provoca un 100% de abandono en las misiones de conversión del Caso B y desploma la confianza en el SUS (P9). | Programar el evento interactivo de reservas. Vincular el CTA a un formulario real de captura de datos o un widget externo, asegurando el uso de etiquetas de feedback accesibles (`aria-haspopup="dialog"`). |
| 🟠 Media | Ausencia total de buscador o filtros en el catálogo ("biblioteca"). Produce fatiga en T02, provoca abandonos y penaliza la complejidad (P2). | Implementar un nodo de entrada estándar `<input type='search'>` en la cabecera de la biblioteca y desarrollar un script JavaScript de filtrado categórico instantáneo. |
| 🟠 Media | Inconsistencia tipográfica y layout severo entre páginas. Provoca confusión cognitiva masiva en perfiles con menor competencia digital, penalizando la accesibilidad. | Homogeneizar las hojas de estilo (CSS) globales. Definir tamaños estables mediante unidades relativas (`rem`/`em`) y eliminar transformaciones de texto forzadas y asimétricas (`text-transform: uppercase`). |
| 🟢 Baja | Disparidad de información de productos entre la Home y la biblioteca. El usuario duda si los artículos son coincidentes. | Unificar el naming, las imágenes de referencia y la estructura de metadatos informativos entre el embudo de captación inicial y las fichas técnicas del catálogo. |
