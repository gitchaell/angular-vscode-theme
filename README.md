<!--
Created: Sun Oct 31 2021 16:45:19 GMT-0400 (hora de Bolivia)
Modified: Wed Mar 16 2022 20:55:10 GMT-0400 (hora de Bolivia)
-->
<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=MichaellAlavedraMunayco.angular-theme">
    <img src="assets/logo.png" width="120px" />
  </a>
</p>

<h1 align="center">
  Angular VS Code Theme
</h1>

Como desarrollador de software, paso la mayor parte de mi día frente a un editor de código. A lo largo del tiempo, noté que la mayoría de los temas disponibles introducen una fatiga visual considerable debido al uso de negros puros o paletas de colores excesivamente saturadas. Al no encontrar una solución que se alineara con mis preferencias estéticas y necesidades de concentración, decidí crear mi propia herramienta.

Este documento detalla la creación de **Angular Dark Theme**, un tema para Visual Studio Code diseñado bajo los estándares de la guía de estilos de *Vercel UI* y *shadcn/ui*. Su propósito es ofrecer un entorno de lectura cómodo, reducir la fatiga ocular y mantener el enfoque mediante un diseño estructurado y sutil.

---

### El Problema de la Fatiga Visual en el Desarrollo

En el ecosistema actual de herramientas de desarrollo, es común encontrar entornos que dificultan la retención de la concentración:
*   **Contraste Extremo:** El uso extendido del negro puro (`#000000`) como fondo, junto con textos brillantes, genera un contraste agresivo que cansa la vista en sesiones prolongadas.
*   **Ruido Cromático:** Muchos temas utilizan acentos fuertes o colores llamativos (como azules saturados) en la interfaz de usuario, lo cual distrae de la tarea principal: comprender la semántica del código.

### La Solución: Diseño Sustractivo y Enfoque

**Angular Dark Theme** aborda estos problemas desde la simplicidad, estableciendo una base visual serena y coherente que prioriza la legibilidad.

[📸 **Insertar captura:** *Vista principal del editor mostrando un archivo de código complejo, destacando el fondo suave #09090B y el esquema de colores monocromático de la interfaz.*]

#### Beneficios Clave del Diseño:

*   **Ausencia de Negro Puro:** He descartado los fondos negros absolutos. En su lugar, el tema se asienta sobre un fondo oscuro suavizado (`#09090B`), proporcionando el nivel exacto de contraste necesario para no forzar la vista, ideal para jornadas largas o condiciones de poca luz.
*   **Interfaz Monocromática:** La paleta base de la interfaz de usuario (paneles, barras de actividad, menús) es estrictamente monocromática, basada en escalas de grises y tonos neutros (`#27272A`, `#52525B`, `#FAFAFA`). He evitado explícitamente el uso de acentos azules o tonos discordantes en los componentes primarios para garantizar un entorno de trabajo sobrio.
*   **Estética Inspirada en Vercel UI:** Las decisiones de color y la estructura visual toman como referencia directa la limpieza geométrica y el minimalismo de *Vercel UI* y *shadcn/ui*, aportando una sensación de orden y profesionalismo al editor.

[📸 **Insertar captura:** *Vista dividida (Split view). A la izquierda, un archivo de código; a la derecha, la terminal integrada y el árbol de archivos, demostrando la consistencia de la interfaz sin distracciones.*]

---

### ⚙️ Bajo el Capó: Arquitectura y Stack

A nivel técnico, esta solución está construida de manera directa sobre las capacidades nativas de tematización de Visual Studio Code, manteniendo el proyecto liviano y fácil de mantener.

*   **Configuración Centralizada:** El núcleo del proyecto es el archivo `themes/angular.dark.theme.json`. Aquí he definido de forma exhaustiva los valores hexadecimales para la interfaz de usuario de VS Code (en la propiedad `colors`), junto con las reglas específicas de resaltado de sintaxis (en `tokenColors`).
*   **Ecosistema de Empaquetado:** La extensión está gestionada mediante `npm` y empaquetada con `vsce` (la herramienta oficial de CLI para extensiones de VS Code). El archivo `package.json` maneja la configuración de publicación, dependencias y los metadatos del *Marketplace*.
*   **Soporte Multilenguaje Extendido:** Aunque el proyecto nació enfocado en el ecosistema Angular, he implementado soporte explícito mediante *TextMate tokens* para múltiples lenguajes y formatos de configuración. El tema incluye asignaciones de color específicas para:
    *   **Archivos de Entorno y Configuración:** `.env`, `json`, `yml`
    *   **Lenguajes de Programación:** `python`, `go`, `rust`, `java`, `kotlin`, `php`

Al analizar y definir tokens específicos para palabras clave (`keywords`) y funciones (`functions`) en estos lenguajes, aseguro que la legibilidad se mantenga constante sin importar el stack tecnológico en uso.

[📸 **Insertar captura:** *Mosaico de fragmentos de código en Go, Rust, Python y un archivo .env, ilustrando cómo el tema mantiene un resaltado sintáctico coherente en distintos lenguajes.*]

---

### Instalación y Uso

1. Visita la página de la extensión en el [VS Marketplace](https://marketplace.visualstudio.com/items?itemName=MichaellAlavedraMunayco.angular-theme).
2. Haz clic en **Install**.
3. En tu editor VS Code, selecciona **Angular Dark Theme** desde tu menú de temas de color.

*(Nota: Si deseas realizar ajustes específicos o añadir acentos personales, puedes sobrescribir colores individuales directamente en tu archivo `settings.json` local siguiendo la [documentación oficial de VS Code](https://code.visualstudio.com/api/extension-guides/color-theme)).*

---

### Conclusión

Un editor de código ordenado y visualmente equilibrado es fundamental para mantener la comodidad a largo plazo durante el desarrollo. Angular Dark Theme es mi respuesta a esta necesidad, aplicando principios de diseño minimalista para crear una herramienta que facilita el trabajo diario.

Si buscas un entorno de desarrollo más limpio, te invito a probar el tema. Además, si te interesa el desarrollo de herramientas para programadores, puedes explorar la configuración de la extensión en este repositorio.

*Puedes descargar el tema, revisar el código o contactarme para consultas a través de este repositorio.*