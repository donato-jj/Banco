# BioSci · Reconstrucción Académica en Biología y Ciencia Moderna

Aplicación web de reconstrucción académica que combina biología molecular, química y física en un sistema interactivo de capas con trazabilidad y distinción ciencia/metáfora.

## Modo de uso

Abre `index.html` directamente en el navegador. No requiere servidor, build ni dependencias externas.

## Capas de visualización

### 1. ADN / Biología (Consenso Científico - Simplificado)
- Doble hélice paramétrica con N pares de bases (10-120)
- Pares Watson-Crick: A-T (2 puentes H, verde/rojo), C-G (3 puentes H, azul/amarillo)
- Representación de surcos mayor/menor por offset visual (simplificado)
- **Slider de empaquetamiento (0-100%):**
  - 0%: Hélice libre (ADN B, ~2 nm)
  - ~30%: Nucleosomas (representación abstracta de histonas)
  - ~60%: Fibra de 30 nm (representación didáctica)
  - ~96%: Cromosoma condensado (representación abstracta)
- Hover/click sobre pares de bases -> tooltip con tipo, índice, puentes H
- **Modo Examen:** oculta labels, al hacer click pide identificar la base; registra puntuación
- **Mutaciones:** aplica sustituciones simples con historial antes/después
- Controles: radio, pitch, velocidad de rotación, toggle de labels, pausa
- Arrastrar para rotar en 3D; rueda del ratón para zoom

### 2. Química (Consenso Científico - Simplificado)
- Moléculas instanciadas (H2O, ATP, Na+, K+, Cl-, Glu) con físicas de atracción/repulsión
- Membrana celular semi-transparente pulsante
- 3 organelos abstractos (núcleo, mitocondria, RE)
- **NOTA:** Representación simplificada; no modela mecanismos reales, cinética ni estructuras atómicas

### 3. Física / Curvatura Espaciotemporal (Modelo Didáctico - NO exacto)
- Grilla de espaciotiempo con deformacion por masa central
- 8 geodésicas aproximadas con integración numérica simple
- Controles: masa, intensidad, escala
- **NOTA:** Modelo didáctico inspirado en Relatividad General (Einstein, 1915). NO es simulación de la métrica de Schwarzschild ni geodésicas reales. No atribuir resultados como fisica exacta.

### 4. Genoma del Vacío (Metáfora Artistica)
- Campo procedural FBM (Fractional Brownian Motion) en dos modos: campo de color y partículas
- Influencia visual del ADN (composición de bases -> matiz de color, sin causalidad científica)
- **NOTA:** Metáfora artística. No representa ningún fenómeno científico real.

## Funciónes del sistema

| Función | Descripción |
|---------|-------------|
| Presentación guiada | 8 pasos que recorren todas las capas con textos académicos |
| Glosario | 12 términos con definiciones rigorosas y referencias |
| Exportar reporte | Genera un archivo .txt con parámetros, secuencia, composición, mutaciones y notas metodológicas |
| Modo Examen | Quizz de identificación de bases con puntuación |

## Principio rector: Ciencia vs Metáfora

Cada capa esta claramente etiquetada en la UI:
- **Verde (Consenso Científico):** ADN, núcleosomas, empaquetamiento, química molecular
- **Amarillo (Modelo Didáctico):** Curvatura espaciotemporal (inspirada, no exacta)
- **Morado (Metáfora Artistica):** Genoma del Vacío (campo procedural FBM)

## Referencias

- Watson, J.D. & Crick, F.H.C. (1953). *Molecular structure of nucleic acids.* Nature 171:737-738.
- Luger, K. et al. (1997). *Crystal structure of the núcleosome core particle.* Nature 389:251-260.
- Chargaff, E. (1950). *Chemical specificity of nucleic acids.* Experientia 6:201-209.
- Einstein, A. (1915). *Die Feldgleichungen der Gravitation.* Preuss. Akad. Wiss. Berlin.
- NCBI Gene Database: https://www.ncbi.nlm.nih.gov/gene

## Stack técnico

- HTML5 + CSS3 + Canvas 2D API + JavaScript ES2020 (sin dependencias externas)
- Proyección 3D perspectiva manual (sin WebGL)
- Renderizado via requestAnimationFrame
- Ruido procedural FBM con hash determinístico
