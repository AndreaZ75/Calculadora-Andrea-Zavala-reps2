1. ¿Qué funcionó bien?
Arquitectura modular: Mantener aislada la lógica matemática (Calculador) de los componentes visuales (Calculadora) permitió que el desarrollo y las pruebas de la interfaz avanzaran sin interferir con la evaluación de expresiones.

Personalización de estilos: La lectura dinámica del archivo settings.json facilitó la adición de nuevos temas sin necesidad de modificar el código fuente de la GUI.

Comunicación y trabajo en equipo: Mantener una comunicación abierta nos permitió solventar dudas de diseño y asegurar la compatibilidad entre plataformas (Darwin/macOS).

2. ¿Qué no funcionó bien / Nos costó trabajo?
Gestión de eventos e ingreso de datos: Asegurar la validación adecuada de los operadores en el widget Entry (evitar duplicaciones de puntos o de caracteres inválidos consecutivamente) requirió más ajustes lógicos de los previstos.

Flujo de trabajo en Git/GitHub: Al ser de las primeras experiencias colaborativas con ramas y Pull Requests, la resolución de conflictos al fusionar cambios generó cierta incertidumbre al inicio.

Estimación inicial de tareas: La integración de la documentación, la generación de diagramas en formato Draw.io y el afinado de detalles visuales tomaron más tiempo del planeado cerca del cierre.

3. ¿Qué haríamos distinto la próxima vez?
Definir estándares de ramas desde el día 1: Establecer reglas estrictas sobre nombres de ramas y momentos de commit para evitar conflictos de fusión al integrar funciones de la interfaz.

Pruebas unitarias automáticas: Desarrollar scripts de prueba con unittest para comprobar la evaluación de cadenas aritméticas antes de vincularlas a los eventos de la interfaz gráfica.

Documentación en paralelo: Diseñar los diagramas de arquitectura e ir redactando el README.md conforme se agregan las historias de usuario en lugar de concentrarlo en la fase final.
