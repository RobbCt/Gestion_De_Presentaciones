\#  Planificación del Proyecto - GP (Incremento 1 / MVP)



\##  1. Sprints y Tareas



\###  Sprint 1: Estructura Visual e Interfaz de Usuario

\* \*\*Objetivo:\*\* Maquetar la interfaz gráfica en WPF sin lógica detallada de fondo.

\* \*\*Tareas:\*\*

&#x20; \* Crear la Solución Multi-Proyecto en Visual Studio (`GP.UI.WPF`, `GP.Core`, `GP.PresentationEngine`, `GP.Adapters.LibreOffice`).

&#x20; \* Diseñar ventana de Inicio para la seleccion de la herramienta (Carrusel)

&#x20; \* Diseñar la ventana Dashboard principal con la \*\*Línea de Tiempo Horizontal\*\* para previsualizaciones y botones para agregar/eliminar presentación .

&#x20; \* Maquetar la ventana emergente \*\*Modo Presentador\*\* (panel con vista previa en vivo y botones de control).

&#x20; \* Crear el cuadro de diálogo para selección de archivos (`.odp`, `.ppt`, `.pptx`) con el flujo de pantallas: Agregar archivo \&rarr; Explorar presentación  \&rarr; Agregar a carrusel



\---



\### Sprint 2: Logica (GP.Core)

\* \*\*Objetivo:\*\* Crear lógica que administra la cola, siendo independiente de la interfaz.

\* \*\*Tareas:\*\*

&#x20; \* Crear el modelo de dato para los elementos del carrusel (`CarouselItem`).

&#x20; \* Programar la lógica de la cola: agregar, eliminar y avanzar/retroceder.

&#x20; \* Implementar eventos para notificar cambios en la lista a la interfaz visual.



\---



\###  Sprint 3: Adaptador de Presentación (GP.Engine + LibreOffice)

\* \*\*Objetivo:\*\* Establecer la comunicación con el software de presentaciones externo.

\* \*\*Tareas:\*\*

&#x20; \* Definir la interfaz universal `IPresentationController` en `GP.PresentationEngine`.

&#x20; \* Desarrollar conector con LibreOffice Impress (`GP.Adapters.LibreOffice`) para abrir/cerrar archivos y avanzar diapositivas.

&#x20; \* Implementar la generación/extracción de miniaturas para las previsualizaciones horizontales.



\---



\###  Sprint 4: Integración Total y Pruebas del MVP

\* \*\*Objetivo:\*\* Unir todos los módulos y realizar pruebas.

\* \*\*Tareas:\*\*

&#x20; \* Conectar el Dashboard y el Modo Presentador con `GP.Core` y `GP.Adapters.LibreOffice`.

&#x20; \* Probar el flujo completo: Seleccionar herramienta \&rarr; Cargar canciones \&rarr; Iniciar Carrusel \&rarr; Proyección en pantalla completa \&rarr; Avance automático/manual entre presentaciones \&rarr; Salida Forzada.

&#x20; \* Ajustes finales de estabilidad y rendimiento(?.



\---



\## 2. Gestión de Riesgos Esperados



| Riesgo  | Plan  |

| :--- | :--- |

| La extracción de la miniatura puede demorar al cargar el archivo. | Generar las imágenes de forma asíncrona en segundo plano y mostrar un icono temporal (\*placeholder\*). |

| Falla o cierre inesperado de LibreOffice en medio de una presentación en vivo.  | Incluir en el Modo Presentador un botón de emergencia "Salida Forzada". |

| Bloqueo de la interfaz al cambiar entre presentaciones. | Ejecutar los comandos hacia el motor externo en hilos secundarios para no congelar la pantalla del operador. |

