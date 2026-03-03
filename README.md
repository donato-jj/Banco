# BioSci · Reconstruccion Academica en Biologia y Ciencia Moderna

Aplicacion web de reconstruccion academica que combina biologia molecular, quimica y fisica en un sistema interactivo de capas con trazabilidad y distincion ciencia/metafora.

## Modo de uso

Abre `index.html` directamente en el navegador. No requiere servidor, build ni dependencias externas.

## Capas de visualizacion

### 1. ADN / Biologia (Consenso Cientifico - Simplificado)
- Doble helice parametrica con N pares de bases (10-120)
- Pares Watson-Crick: A-T (2 puentes H, verde/rojo), C-G (3 puentes H, azul/amarillo)
- Representacion de surcos mayor/menor por offset visual (simplificado)
- **Slider de empaquetamiento (0-100%):**
  - 0%: Helice libre (ADN B, ~2 nm)
  - ~30%: Nucleosomas (representacion abstracta de histonas)
  - ~60%: Fibra de 30 nm (representacion didactica)
  - ~96%: Cromosoma condensado (representacion abstracta)
- Hover/click sobre pares de bases -> tooltip con tipo, indice, puentes H
- **Modo Examen:** oculta labels, al hacer click pide identificar la base; registra puntuacion
- **Mutaciones:** aplica sustituciones simples con historial antes/despues
- Controles: radio, pitch, velocidad de rotacion, toggle de labels, pausa
- Arrastrar para rotar en 3D; rueda del raton para zoom

### 2. Quimica (Consenso Cientifico - Simplificado)
- Moleculas instanciadas (H2O, ATP, Na+, K+, Cl-, Glu) con fisicas de atraccion/repulsion
- Membrana celular semi-transparente pulsante
- 3 organelos abstractos (nucleo, mitocondria, RE)
- **NOTA:** Representacion simplificada; no modela mecanismos reales, cinetica ni estructuras atomicas

### 3. Fisica / Curvatura Espaciotemporal (Modelo Didactico - NO exacto)
- Grilla de espaciotiempo con deformacion por masa central
- 8 geodesicas aproximadas con integracion numerica simple
- Controles: masa, intensidad, escala
- **NOTA:** Modelo didactico inspirado en Relatividad General (Einstein, 1915). NO es simulacion de la metrica de Schwarzschild ni geodesicas reales. No atribuir resultados como fisica exacta.

### 4. Genoma del Vacio (Metafora Artistica)
- Campo procedural FBM (Fractional Brownian Motion) en dos modos: campo de color y particulas
- Influencia visual del ADN (composicion de bases -> matiz de color, sin causalidad cientifica)
- **NOTA:** Metafora artistica. No representa ningun fenomeno cientifico real.

## Funciones del sistema

| Funcion | Descripcion |
|---------|-------------|
| Presentacion guiada | 8 pasos que recorren todas las capas con textos academicos |
| Glosario | 12 terminos con definiciones rigorosas y referencias |
| Exportar reporte | Genera un archivo .txt con parametros, secuencia, composicion, mutaciones y notas metodologicas |
| Modo Examen | Quizz de identificacion de bases con puntuacion |

## Principio rector: Ciencia vs Metafora

Cada capa esta claramente etiquetada en la UI:
- **Verde (Consenso Cientifico):** ADN, nucleosomas, empaquetamiento, quimica molecular
- **Amarillo (Modelo Didactico):** Curvatura espaciotemporal (inspirada, no exacta)
- **Morado (Metafora Artistica):** Genoma del Vacio (campo procedural FBM)

## Referencias

- Watson, J.D. & Crick, F.H.C. (1953). *Molecular structure of nucleic acids.* Nature 171:737-738.
- Luger, K. et al. (1997). *Crystal structure of the nucleosome core particle.* Nature 389:251-260.
- Chargaff, E. (1950). *Chemical specificity of nucleic acids.* Experientia 6:201-209.
- Einstein, A. (1915). *Die Feldgleichungen der Gravitation.* Preuss. Akad. Wiss. Berlin.
- NCBI Gene Database: https://www.ncbi.nlm.nih.gov/gene

## Stack tecnico

- HTML5 + CSS3 + Canvas 2D API + JavaScript ES2020 (sin dependencias externas)
- Proyeccion 3D perspectiva manual (sin WebGL)
- Renderizado via requestAnimationFrame
- Ruido procedural FBM con hash deterministico
