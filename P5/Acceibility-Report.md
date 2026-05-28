# Accessibility Report

<img src="https://img.uxcel.com/cdn-cgi/image/format=auto/practices/wcag-principles-overview-1742315821212/a-1742315821212-2x.jpg" alt="usability Download png" style="height:200px" />

## 1. Ficha Técnica del Informe

- **Nombre del proyecto:** Wax & Wayne - Web del Proyecto (Caso B)
- **Normativa de referencia:** WCAG 2.2 (Nivel AA) / Estándar legal UNE-EN 301549
- **Herramientas utilizadas:** WAVE (Web Accessibility Evaluation Tool), Lighthouse Accessibility Engine y validación pericial por teclado.
- **Fecha de la auditoría:** 28 de Mayo de 2026

---

## 2. Puntuaciones Globales (Métricas Automáticas)

* **Lighthouse Accessibility Score:** 62 / 100
* **WAVE Summary:** * **Errores Críticos:** 3 (Eventos de acción huérfanos, enlaces muertos estructurales y ausencias de etiquetado semántico).
  * **Alertas:** 4 (Estructura de encabezados forzada por CSS y saltos de layout desestructurados).
  * **Errores de Contraste:** 0 (La paleta cromática es aceptable, pero la legibilidad quiebra por deformación de fuentes).

---

## 3. Análisis por Principios (POUR)

<img src="https://cdn.sanity.io/images/r115idoc/production/e745ae232e5e6760c1392354021aed4eecc4627d-1920x1080.png" alt="usability Download png" style="height:200px" />

### A. Perceptible

* **Error detectado:** Inconsistencia tipográfica severa. Los títulos principales de la Home están forzados mediante CSS en letras MAYÚSCULAS sostenidas (`text-transform: uppercase`), mientras que en las secciones internas de la biblioteca cambian radicalmente a minúsculas ordinarias sin justificación jerárquica.
* **Criterio WCAG incumplido:** Criterio 1.4.4 (Cambio de tamaño de texto) y Pauta 3.2 (Consistencia).
* **Impacto:** Los usuarios con baja agudeza visual, dislexia o dificultades de procesamiento cognitivo experimentan fatiga, estrés y desorientación espacial debido a la falta de regularidad de los pesos y las formas visuales de las fuentes.
* **Recomendación de mejora:** Homogeneizar las hojas de estilo del sitio. Definir clases CSS globales estables para los encabezados (`h1`, `h2`) y eliminar la alteración forzada mediante propiedades tipográficas de forma anárquica.

---

### B. Operable

* **Error detectado:** El botón principal para realizar reservas de mesa en la cafetería carece por completo de funcionalidad interactiva o hipervínculo activo (es un elemento muerto en el código con un puntero inerte o un enlace apuntando exclusivamente a `href="#"`).
* **Criterio WCAG incumplido:** Criterio 2.4.3 (Orden de enfoque) y Criterio 2.4.4 (Propósito de los enlaces).
* **Impacto:** Produce una sensación de bloqueo técnico absoluto. Los usuarios de tecnologías asistivas o navegación exclusiva por teclado ejecutan la acción principal de negocio sin recibir ningún tipo de respuesta, feedback o cambio de estado del sistema.
* **Recomendación de mejora:** Programar un modal de captura de datos interactivo con validación estricta de accesibilidad o redirigir de forma efectiva al usuario al widget de reservas externo utilizando etiquetas de feedback claras como `aria-haspopup="dialog"`.

---

### C. Comprensible

* **Error detectado:** El catálogo completo de productos gourmet alojado en la sección "biblioteca" carece por completo de un componente de buscador de texto o de un filtro dinámico por categorías, tipos de grano o alérgenos.
* **Criterio WCAG incumplido:** Criterio 1.3.1 (Información y Relaciones / Estructura de Datos).
* **Impacto:** Obliga a los usuarios con discapacidades motoras, fatiga cognitiva o que dependan de lectores de pantalla a realizar un scroll manual infinito y ciego para localizar un artículo elemental, destruyendo la predictibilidad de la navegación.
* **Recomendación de mejora:** Implementar un nodo estándar de búsqueda `<input type='search'>` en la parte superior con etiquetas WAI-ARIA descriptivas y desarrollar un script JavaScript de filtrado dinámico en tiempo real para segmentar los productos.

---

### D. Robusto

* **Error detectado:** Ruptura de la trazabilidad e identificación informativa. Los elementos estéticos y los nombres promocionados en el inicio de la web (Home) no se corresponden ni guardan relación directa con las fichas técnicas o etiquetas nominales de la biblioteca de productos.
* **Criterio WCAG incumplido:** Criterio 3.2.4 (Identificación consistente).
* **Impacto:** Genera una sobrecarga cognitiva severa y quiebra la compatibilidad interpretativa del sistema. El usuario no logra descifrar si el café o postre gourmet publicitado en la Landing Page es el mismo que está visualizando bajo otra disposición en el catálogo.
* **Recomendación de mejora:** Unificar el naming, las imágenes de referencia y la estructura de metadatos informativos entre el embudo de captación inicial y las fichas técnicas finales de la biblioteca.

---

## 4. Tabla de Hallazgos y Prioridades

| ID | Prioridad | Criterio WCAG | Error detectado | Recomendación Técnica |
| :--- | :--- | :--- | :--- | :--- |
| **ACC-01** | 🔴 **Crítica** | 2.4.4 Propósito de enlaces | El botón principal de reserva de mesa es un elemento inerte en el código (`href="#"`). | Programar el evento interactivo de reservas vinculándolo a un formulario real o widget con atributos `aria-haspopup`. |
| **ACC-02** | 🟠 **Alta** | 1.3.1 Info y relaciones | Catálogo de productos sin barra de búsqueda o filtros de accesibilidad. | Implementar un nodo estándar `<input type='search'>` y aplicar filtros por script de interacción directa. |
| **ACC-03** | 🟠 **Media** | 1.4.4 Tamaño del texto | Títulos forzados por CSS en mayúsculas sostenidas en Home y minúsculas en internas. | Homogeneizar las CSS globales, definir tamaños estables con unidades relativas (`rem`) y retirar el `text-transform`. |
| **ACC-04** | 🟢 **Baja** | 3.2.4 Identif. consistente | Desconexión informativa de nombres e imágenes entre la Home y la Biblioteca. | Unificar el naming y la estructura de metadatos comerciales de los productos en todas las vistas de la aplicación. |

---

## 5. Conclusiones y Declaración de Conformidad

- **¿Es el sitio accesible?** El prototipo actual **NO cumple con los estándares mínimos de accesibilidad del nivel AA**. Presenta barreras críticas de exclusión digital, destacando la imposibilidad absoluta de completar el flujo de conversión (reserva) para usuarios dependientes de navegación por teclado o lectores de pantalla, además de provocar una alta fatiga cognitiva debido a su desestructuración e inconsistencia tipográfica.
- **Próximos pasos:**
  1. **Acción Urgente:** Activar el código del CTA de reservas dotándolo de un comportamiento interactivo real y accesible.
  2. **Acción de Navegabilidad:** Insertar el motor de filtrado y búsqueda semántica en la biblioteca para mitigar el scroll manual infinito.
  3. **Acción de Consistencia:** Unificar las hojas de estilo (CSS) para que las tipografías, layouts y nombres de producto mantengan un patrón predecible en todo el sitio web.
