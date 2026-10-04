# Evaluación Bioinstrumental: Estabilidad Postural Unipodal Automática

## Descripción del Proyecto
Interfaz web interactiva para la evaluación biomecánica del control postural estático en apoyo unipodal (*Single Leg Stance Test*). La aplicación utiliza visión por computador mediante la cámara web para:
1. Calibrar y trazar automáticamente una **Línea Media Corporal de Referencia** ($X_0$).
2. Detectar de manera autónoma la **Señal Gestual de Inicio** (elevación de la palma de la mano derecha).
3. Reconocer cuál es el **Pie de Apoyo** (Derecho o Izquierdo) según la biomecánica del sujeto.
4. Medir en tiempo real el **Tiempo de Apoyo Unipodal** ($T$), el **Desplazamiento Mediolateral** ($\Delta X$) y la **Variabilidad RMS**.
5. Detener automáticamente la medición y el conteo al reconocer que el sujeto volvió a apoyar **ambos pies en el piso**.
6. Generar al finalizar una **Tabla Resumen y Gráfica Biomecánica** para el análisis kinesiológico.

## Requisitos y Dependencias
- Navegador web moderno (Google Chrome, Microsoft Edge, Mozilla Firefox o Safari).
- Cámara web funcional con resolución mínima recomendada de 720p.
- Conexión a internet para la carga de bibliotecas desde CDN:
  - **MediaPipe Pose** (Tracking biomecánico)
  - **Chart.js** (Renderizado de gráficos)
  - **Tailwind CSS** (Diseño de interfaz)

## Instrucciones de Uso
1. **Acceso:** Abra la página web pública y conceda los permisos para utilizar la cámara web.
2. **Calibración Bípeda:** Posiciónese erguido frente a la cámara en apoyo sobre ambos pies a una distancia de 1.5 a 2 metros. La interfaz fijará el eje vertical de referencia (Línea punteada azul).
3. **Señal Gestual:** Levante la mano derecha con la palma visible por sobre el nivel del hombro.
4. **Ejecución Unipodal:** Eleve un pie del suelo. La interfaz reconocerá automáticamente la extremidad de apoyo, iniciará el cronómetro y comenzará el gráfico de oscilaciones.
5. **Detención Automática:** Al finalizar o perder el equilibrio, vuelva a apoyar ambos pies en el suelo. La interfaz detectará el doble apoyo, detendrá la prueba y desplegará la tabla de resultados.

## Archivos Principales
- `index.html`: Código fuente integral que combina la interfaz gráfica, estilos, scripts de visión por computador y renderizado de gráficos/tablas.
- `README.md`: Documentación y manual de usuario para reproducción de la solución.
