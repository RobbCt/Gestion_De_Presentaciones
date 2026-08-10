\# Especificación de Requisitos - GP (Incremento 1 / MVP)



\## 1. Función Principal

Secuenciación, ejecución y control de una cola ordenada de presentaciones (carrusel).



\---



\## 2. Límites del Sistema

\* \*\*Punto de Entrada (Inicio):\*\* El operador presiona el botón \*\*"Iniciar Carrusel"\*\* en la ventana de herramientas.

\* \*\*Puntos de Salida (Fin):\*\* 

&#x20; \* Cierre automático al finalizar la última diapositiva del último archivo de la cola.

&#x20; \* Cierre manual e inmediato mediante los botones de salida desde cualquier ventana.

\---



\##  3. Alcance Funcional del Incremento 1 (MVP)



\### A. Dashboard Principal (Ventana 1)

\* \*\*Línea de Tiempo Horizontal:\*\* Interfaz organizada horizontalmente para gestionar el orden visual de la cola de reproducción.

\* \*\*Tarjetas con Vista Previa:\*\* Cada tarjeta exhibirá una miniatura (cuadrado con la primera diapositiva) del archivo cargado (`.odp`, `.ppt`, `.pptx`) y su nombre.



\* \*\*Agregar Presentacion:\*\* Cuadro de diálogo para abrir \&rarr; explorar \&rarr; agregar presentaciones al carrusel.



\* \*\*Gestión de Lista:\*\* Botones para eliminar o reordenar elementos (Agregar/Eliminar).

\* \*\*Disparador:\*\* Botón "Iniciar Carrusel" que lanza la presentación en el proyector y la siguiente ventana.



\### B. Modo Presentador (Ventana 2)

\* \*\*Visualizador en Vivo:\*\* Muestra la vista previa de la diapositiva en pantalla (proyector) y la diapositiva siguiente para anticipación.

\* \*\*Navegación Dinámica:\*\* Controles manuales rápidos (Anterior, Siguiente, Saltar Presentación, Agregar Presentacon Siguiente, Salida Forzada)



\### C. Integración Externa

\* Adaptador para comunicación bidireccional con \*\*LibreOffice Impress\*\* (envío de comandos de navegación, lectura del estado de diapositivas y extracción/generación de miniatura inicial).



\---



\##  4. Funciones no incluidas

\* \*\*Guardado de proyectos en disco:\*\* La aplicación iniciará con la lista vacía en cada ejecución.

\* \*\*Edición de contenido:\*\* No se modificarán diapositivas dentro de GP, sino en software de presentación externo (LibreOffice, PowerPoint, Etc).

\* \*\*Integración con Microsoft PowerPoint:\*\* Postergada para versiones futuras.

