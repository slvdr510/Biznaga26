# Biznaga26@FYCMA

---

## Construyendo features en vivo: SDD y técnicas para guiar a la IA

*Al habla, Fernando Herrera.*
	
Construir software con agentes de IA sin método produce código impredecible y decisiones de arquitectura que nadie tomó.

Haré una demo en vivo construiremos varios features de cero poniendo el foco en Spec-Driven Design y otras técnicas de desarrollo guiado para crear los artefactos (specs), contexto y reglas, que dirigen al agente hacia el resultado correcto, evitando que se descarrile, pierda o simplemente cree resultados que no nos sirven para nada.

**Resumen**: 

- Crear specs para describir el feature, su estado actual, requisitos y dependencias.  

- Usar comandos de opencode que sirvan para hacer trabajo repetitivo con la IA, agilizando el input de la información para dicho proceso, ya sea con selectores de opciones por parte de la IA, o marcando paso a paso los datos que el desarrollador tiene que introducir para generar cualquier cosa.

**Extra**:

Le pregunté a Fernando qué proveedor de hosting usa para poder vender cursos en `cursos.devtalles.com`. Me comentó que usa  [thinkific.com](https://www.thinkific.com/). Tienen modalidad de pago único (1000$ anuales) y el resto de beneficio generado por las ventas de los cursos va para el creador.

---

## Construyendo la Web Agéntica: Introducción, Utilidades y Retos de Web-MCP

*Al habla, Raúl Tovar.*

La inteligencia artificial ha cambiado la forma en que interactuamos con el software, pero la web sigue estando diseñada exclusivamente para humanos. ¿Qué pasaría si nuestras páginas web pudieran exponer directamente sus herramientas y utilidades a los agentes autónomos de forma nativa?

En esta sesión técnica exploraremos a fondo Web-MCP (Web Model Context Protocol), el nuevo y revolucionario estándar impulsado por el W3C Community Group. A diferencia del MCP tradicional de backend, Web-MCP transforma el propio navegador web en un orquestador semántico. A través de la nueva API navigator.modelContext, descubriremos cómo los desarrolladores frontend pueden publicar las funcionalidades de sus aplicaciones como herramientas estrictamente tipadas y listas para ser usadas por cualquier IA local o en la nube.

Durante la charla daremos a conocer las principales utilidades prácticas del protocolo: desde la API Declarativa para modernizar formularios HTML en segundos, hasta la API Imperativa para integrar lógicas complejas en aplicaciones React o Vue. Pero también hablaremos desde las trincheras, abordando los retos arquitectónicos reales: la obligatoria refactorización para desacoplar componentes, la gestión de costes y abusos, y la limitación del ciclo de vida en la pestaña del usuario. Finalmente, miraremos hacia el futuro debatiendo cómo Web-MCP sentará las bases del AEO (Agent Engine Optimization). Ven a descubrir cómo preparar tus proyectos frontend para la era de los motores agénticos.

**Contenido**:

1. Spec y documentación

	1.1. WebMCP - [https://webmachinelearning.github.io/webmcp](https://webmachinelearning.github.io/webmcp)

	1.2. Explainer e issues - [https://github.com/webmachinelearning/webmcp](https://github.com/webmachinelearning/webmcp)

	1.3. Chrome - [https://developer.chrome.com/docs/ai/webmcp](https://developer.chrome.com/docs/ai/webmcp)

	1.4. MCP - [https://modelcontextprotocol.io/specification/2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28)

	1.5. Angular - [https://angular.dev/ai/webmcp](https://angular.dev/ai/webmcp)

	1.6. Cloudflare - [blog.cloudflare.com/webmcp](blog.cloudflare.com/webmcp)

2. Herramientas

	2.1. knot.kz - [https://www.knot.kz](https://www.knot.kz)

	2.2. chrome-debug - [https://github.com/raultov/chrome-debug-mcp](https://github.com/raultov/chrome-debug-mcp)

	2.3. chrome-devtools-mcp - [https://github.com/ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp)

	2.4. Playwright MCP - [https://github.com/microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)

	2.5. media-transcriber - [https://github.com/raultov/media-transcriber-mcp](https://github.com/raultov/media-transcriber-mcp)

**Resumen**:

La IA no sabe qué hace realmente el botón de una web. Necesita hacer capturas, probar el botón, etc.

Para ello se está creando un nuevo estándar para las páginas, WebMCP. Este no es lo mismo que MCP. WebMCP necesita que tengas la web abierta en tu navegador, `Brave Browser` creo que dijo, tiene un compañero IA. Este se puede conectar a dicha web abierta en el navegador y ver el contenido accesible.

La reflexión fue, desacoplar las funcionalidades de los botones para poder dárselas también al WebMCP, para que la IA pueda usar las funcionalidades del sitio web, sin tener que visualizar y analizar la interfaz web del sitio en ningún momento.

Todo esto implica una nueva serie de permisos y restricciones para dicha IA que usará la web, y una nueva superficie de ataque tanto para la web como para el agente que ejecuta algo proporcionado por WebMCP.

---

## Agentic DevOps no es lo que tú creías

*Al habla, Gisela Torres.*

Nos han vendido Agentic DevOps como “agentes haciendo cosas”: que si crean código, que si abren PRs, que si ejecutan workflows… pero la parte interesante viene justo después: ¿y ahora quién revisa esto?, ¿con qué permisos corre?, ¿qué pasa si se viene arriba?, ¿y si hace merge porque “todo estaba en verde”?

En esta charla veremos Agentic DevOps desde otro ángulo: no como magia con IA, sino como una nueva forma de colaborar donde los agentes también necesitan contexto, límites, trazabilidad y supervisión.

Spoiler: el futuro no va solo de tener agentes más listos, sino de tener mejores guardrails.

**Resumen**:

Usar IA en github, haciendo un flujo de trabajo para gestionar qué PRs se pueden mergear directamente sin revisión humana. Además, que una IA lea dicho PR y que tenga un prompt template para generar algo nuevo gracias al ticket.

---

## Gestionando datos a gran escala

*Al habla, Javi Santana.*

Las empresas que trabajan con gran cantidad de datos necesitan trabajar de formas poco habituales, hacer algunas cosas muy concretas a nivel técnico, tener en cuenta detalles que a poca escala son insignificantes, costes, performance... la mayoría de gente no tiene la oportunidad de saber como funcionan las tripas de esos sistemas, pero para eso está esta charla.

En esta charla cuento qué retos técnicos tienen empresas como Vercel, Canva, Harness, Inditex y otras similares donde las cargas de datos se miden en petabytes diarios. Obviamente hablaré de como hemos diseñado los sistemas para sostener esas cargas.

No es una charla teoríca donde vaya a explicar la arquitectura ideal que ya la conocéis todos, es una charla práctica con ejemplos de arquitecturas de datos que han evolucionado durante años.

**Contenido**:

[Shared content](https://lbrl.engineering/biznagafest)

[Slides](content/biznaga_Datos_a_escala_petabyte.pdf)

---

## Building AI apps from scratch with the Google ecosystem

*Al mando del taller, Rosário Fernandes.*

The way we build software has changed. Today, the most successful developers aren't just writing code, they are orchestrating AI tools and agents to build better and faster.

This hands-on session is a deep dive into this modern "Builder Stack”, where you will learn how to build with a variety of tools in the Google ecosystem.

Come to this session if you want to spend less time configuring and more time creating. We’ll guide you through a complete development lifecycle, from prototyping an idea, to generating a beautiful UI, building AI features, and integrating a secure, scalable backend.


**Contenido**:

[OG site](https://codelabs.developers.google.com/building-ai-apps-google-ecosystem#0)

[slvdr510.dev post](https://slvdr510.dev/blog/0002-build-ai-apps-with-the-google-ecosystem/)

---

## Harness Engineering: Construyendo el entorno para que tu Agente de IA escriba código rápido y óptimo

*Al habla, Joan León y Carlos Villuendas*

Delegar la escritura de código a agentes de IA es el nuevo estándar, pero ¿cómo nos aseguramos de que el código generado no destroza el rendimiento de nuestra aplicación? La IA es excelente iterando, pero es ciega al impacto en tiempo de ejecución a menos que le demos los ojos adecuados. Aquí es donde entra la Ingeniería de Arneses.

En esta charla exploraremos cómo diseñar y programar arneses de rendimiento específicos para agentes de IA. Veremos cómo definir herramientas (tools) deterministas basadas en scripts de navegador y APIs nativas para que un agente pueda ejecutar su propio código, medir el estrés del hilo principal y analizar métricas clave de forma autónoma antes de dar por buena una tarea. Descubre cómo pasar de hacer prompt engineering a construir la infraestructura que guiará a las IA del futuro hacia un desarrollo web eficiente y de alto rendimiento.

[Slides OG](https://harness-eng.surge.sh)

[Slides en el repositorio](content/Harness_Engineering.html)

---