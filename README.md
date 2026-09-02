# Calculadora Tk - Aplicación de Escritorio en Python

## Descripción y Justificación del Proyecto

### Descripción
**Calculadora Tk** es una aplicación de escritorio desarrollada en Python utilizando la librería nativa `tkinter` para la interfaz gráfica[cite: 3]. Permite realizar operaciones aritméticas fundamentales y avanzadas (potenciación con `^` y radicación con `√` mediante exponentes fraccionarios `**(1/2)`, más el manejo de jerarquía con paréntesis), incorporando gestión de errores en tiempo real, notación científica automática para resultados extensos y personalización dinámica de temas visuales mediante archivos de configuración JSON (`settings.json`).

### Justificación Formal

El proyecto se seleccionó tomando como referencia la implementación base del repositorio [matheusfelipeog/calculadora-tk](https://github.com/matheusfelipeog/calculadora-tk)[cite: 3] con el objetivo de analizar, refactorizar y documentar un motor de cálculo modular y visualmente adaptable. Esta elección representó un alcance técnicamente adecuado dentro del marco temporal de la práctica, permitiendo aplicar la separación de responsabilidades entre la interfaz visual (`Calculadora`) y la lógica interna de evaluación (`Calculador`), validando de punta a punta las 5 fases del ciclo de vida del software (Comunicación, Planeación, Modelado, Construcción y Cierre).
Esto puede brindar una herramienta personal al alcance, si el usuario desea se realicen mas operaciones o solo ciertas funciones añadidas, creando una calculadora personal.
Con esta se toma como una buena base a iniciar.

---

## Historias de Usuario

* **US1 (Base):** Como usuario, quiero disponer de un teclado numérico (0 al 9) y de operadores básicos (`+`, `-`, `*`, `/`) dispuestos en rejilla para construir expresiones matemáticas intuitivamente.
* **US2 (Base):** Como usuario, quiero agrupar operaciones mediante paréntesis `(` y `)` para definir prioridades de cálculo complejas.
* **US3 (Base):** Como usuario, quiero presionar el botón `=` para evaluar la expresión actual mediante el motor de cálculo y obtener el resultado en pantalla.
* **US4 (Base):** Como usuario, quiero que la interfaz muestre el mensaje `'Erro'` ante fallas matemáticas (como división entre cero, errores de sintaxis o valores no válidos) sin bloquear la aplicación.
* **US5 (Base - Notación Científica):** Como usuario, quiero que los resultados que excedan los 15 caracteres se formateen en notación científica (`{:5.5E}`) para preservar la presentación visual en pantalla.
* **US6 (Bonus - Gestión de Temas):** Como usuario, quiero cambiar la apariencia visual de la calculadora mediante la barra de menú (`Configuração > Tema`) y guardar mi preferencia persistentemente en un archivo `settings.json`.
* **US7 (Base - Compatibilidad Multiplataforma):** Como usuario en entornos macOS (`Darwin`), quiero que el sistema detecte la plataforma y seleccione automáticamente un tema nativo compatible (`Default Theme For MacOS`) para evitar inconsistencias de renderizado.

---

### Metodología Elegida
**Enfoque Ágil con Kanban Ligero.**

Dirigiendo hacia un enfoque ágil guiado por un tablero Kanban; la organización en columnas permitiendo asignar un issue a cada historia de usuario, priorizar la construcción de los botones y la evaluación sintáctica antes de implementar la persistencia de temas visuales en JSON, manteniendo una visibilidad constante sobre los avances realizados.

---

## Estructura del Proyecto y Tecnologías

### Tecnologías Utilizadas
* **Lenguaje:** Python 3 (`tkinter`, `functools`, `json`, `platform`, `copy`, `os`, `sys`).
* **Control de Versiones y CASE:** Git, GitHub (Repositorio, Issues y GitHub Projects).
* **Modelado y Diagramas:** Matplotlib / Draw.io.

### Estructura de Archivos

```text
Calculadora-repositorio2-/
│
├── app/
│   ├── settings/
│   │   └── settings.json                     # Configuración de temas visuales
│   ├── view/
│   │   └── calculadora.py                    # Interfaz gráfica de usuario (Tkinter)
│   └── calculador.py                         # Motor y lógica matemática de la calculadora
├── diagrams/
│   ├── diagrama_flujo_calculador_class.png     # Diagrama de flujo de la clase Calculador
│   └── diagrama_flujo_calculadora_gui.png      # Diagrama de arquitectura y eventos GUI
├── main.py                                   # Punto de entrada principal
├── README.md                                 # Documentación técnica del proyecto
└── RETROSPECTIVA.md                          # Informe de cierre y retrospectiva del equipo

```


### Arquitectura de Interfaz y Eventos GUI (Clase Calculadora)
![Diagrama Calculadora](<DIAGRAMA DE FLUJO/calculadora.jpeg>)

