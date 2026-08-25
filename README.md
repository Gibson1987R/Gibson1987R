# Hola, soy Gibson Rosales 👋

**Desarrollador web junior.** Fui profesor de matemáticas durante años; hoy
construyo las herramientas que antes resolvía a mano. Enseñar me dejó dos
costumbres que uso a diario: descomponer un problema hasta que se vuelve
obvio, y explicar la solución en palabras que cualquiera entienda.

📄 **[Mi CV en la web](https://cv-gibson-rosales.netlify.app)** · ✉️ gibsonrosales@gmail.com · 📍 Medellín, Colombia — remoto o presencial

---

## Qué he hecho este año

En repos de clientes, así que no puedo enlazar el código. Enlazo el producto
como referencia y cuento lo que hice yo.

### 🍽️ Onboarding de [Directo IA](https://www.directoia.com/) · venta por WhatsApp con IA para restaurantes

**Construí el flujo de configuración inicial**, las pantallas donde el dueño de
un restaurante da de alta su agente —menú, precios, horarios, personalidad,
reglas de operación— sin nadie que lo acompañe. Si se pierde ahí, no hay
producto.

- **Rehice cada paso para que quepa en la pantalla**, en cualquier tamaño, en
  vez de obligar a hacer scroll dentro de un formulario largo: es el punto
  donde la gente abandona.
- **Llevé los errores al sitio donde ocurren.** Los dice el robot del producto,
  en ese paso, y desaparecen en cuanto tocas el campo. Al intentar avanzar, se
  resalta lo que falta.
- **Hice recuperable el onboarding a medias:** quien vuelve retoma donde iba,
  sin perder lo escrito ni recibir errores falsos.
- **Lo dejé navegable con teclado** y sin romperse con textos largos ni en móvil.

Next.js 16 · React 19 · TypeScript · Tailwind 4 · Supabase.

### ♟️ Internacionalización y acceso de [ChessLab](https://chesspwa.netlify.app) · cursos de ajedrez sin conexión

**Hice que la aplicación hablara otro idioma, incluido el contenido de los
cursos**, no solo los botones.

- **Traduje las lecciones en local** y resolví que las imágenes se perdieran al
  traducir el markdown: sin ellas, una lección de ajedrez no se entiende.
- **Añadí acceso con Supabase, opcional**, para que la app siga sirviendo a
  quien no quiere crear cuenta.
- **Arreglé un callejón sin salida:** al resolver el último ejercicio no había
  cómo volver, y el usuario quedaba atrapado.

PWA sin conexión · Supabase · Netlify.
*Requiere cuenta para entrar: el enlace es referencia del producto, no una demo abierta.*

### 💸 Mantengo en producción una automatización bancaria

**La opero y la arreglo; no la escribí, y prefiero decirlo.** Un Google Apps
Script lee las alertas de Bancolombia que llegan al correo y crea la
transacción ya categorizada en **[Lunch Money](https://lunchmoney.app)**, cada
5 minutos, sin que nadie la toque. No tiene web propia: corre dentro de la
cuenta de Google del cliente.

**Mi trabajo es que siga funcionando.** Cuando el banco cambia el formato de un
correo, el parser deja de reconocerlo y las transacciones se caen **en
silencio**: nadie recibe un error, simplemente dejan de aparecer. Encontrar ese
caso, reproducirlo y corregir la regla es lo que hago. Me enseñó que en
automatización lo difícil no es escribirla, es que siga viva el martes.

Google Apps Script · GmailApp · API de Lunch Money.

---

## Proyectos propios

### 🎯 [honest-english](https://github.com/Gibson1987R/honest-english) · [demo en vivo](https://gibson1987r.github.io/honest-english/)

**Las apps de idiomas te premian por abrirlas. Esta mide si de verdad puedes
hablar, y te lo dice sin adornos.** La construí para no engañarme sobre mi
propio inglés: te hace hablar al micrófono, puntúa palabra por palabra lo que
saliste diciendo, y muestra la brecha entre lo que entiendes y lo que puedes
producir.

JavaScript sin dependencias ni paso de build. Arquitectura **BYOK**: la clave de
OpenAI o Claude vive en el navegador del visitante y nunca pasa por un servidor
mío — porque no hay servidor. Estático en GitHub Pages, cero infraestructura.

### 🎂 fiestas-web · [demo en vivo](https://fiestas-app.vercel.app/demo)

**Tres semanas antes de un cumpleaños infantil solo importa una pregunta
—"¿cuántos vienen?"— y nadie la contesta.** Cada fiesta tiene su página: el
invitado confirma en menos de un minuto sin crear cuenta, y el contador de
confirmados se enciende en vivo en el teléfono de quien organiza.

React 18 · Vite · Firestore en tiempo real · Vercel. Cada fiesta tiene su
**propia colección** de Firestore con sus propias reglas, para que el
aislamiento entre clientes lo imponga el servidor y no un `where` que se me
pueda olvidar: son nombres de niños y teléfonos de sus padres.

### 🏥 [facturacion-scripts](https://github.com/Gibson1987R/facturacion-scripts)

**Automaticé mi propio trabajo.** En el hospital, las autorizaciones de salud
llegaban como un solo PDF con cuatro documentos mezclados dentro, y había que
separarlos a mano, página por página, tarde tras tarde. Este script en Python
los divide, prueba las repartos válidos según el número de páginas y deja cada
documento reconstruido y renombrado.

Sin datos de pacientes en el repositorio, y el NIT de la entidad se lee de una
variable de entorno. PyMuPDF, sin más dependencias.

### 💻 [cv-gibson](https://github.com/Gibson1987R/cv-gibson) · [demo en vivo](https://cv-gibson-rosales.netlify.app)

Mi currículum como página web bilingüe (es/en) con estética de editor de código
y paleta de comandos en <kbd>⌘K</kbd>. Cero dependencias en runtime, contraste
AA medido en ambos temas, navegable entero con teclado.

### 🍎 [calorie-smart](https://github.com/Gibson1987R/calorie-smart) · [demo en vivo](https://gibson1987r.github.io/calorie-smart/)

Contador de calorías con metas personalizadas: calcula el gasto energético con
Mifflin-St Jeor, lo ajusta por actividad y objetivo, y estima calorías de
alimentos escritos en lenguaje natural. React + Vite + Tailwind, Firebase Auth y
Supabase. **Funciona completo en modo demo sin configurar nada:** entra con
`admin@calorie.app` / `admin123` y estás dentro. Una demo que exige credenciales
no es una demo.

---

## Cómo trabajo

Construyo productos web dirigiendo agentes de IA: escribo la especificación,
reviso el código que sale, lo pruebo y lo publico. Reviso todo lo que firmo —
si no entiendo una línea, no la merge.

**Frontend** — JavaScript (ES6+) · React · TypeScript · HTML5 · CSS3 · Tailwind · Sass · Vite
**Backend y datos** — Node.js · Python · Supabase (PostgreSQL) · Firebase/Firestore · Google Apps Script
**Herramientas** — Git · GitHub Actions · Netlify · Vercel · n8n

## Aprendiendo ahora

- **Inglés técnico** — nivel A2 y subiendo. Construí `honest-english`
  precisamente para no engañarme sobre mi propio progreso.
- **Testing y CI** — que el código se defienda solo antes de que alguien lo lea.

---

<details>
<summary><b>In English</b></summary>

<br>

I'm a **junior web developer** based in Medellín, Colombia. After years teaching
mathematics, I now build the tools I used to run by hand.

**Client work lives in private repos, so I link the product and describe what
I did:**

- **I built the onboarding flow of [Directo IA](https://www.directoia.com/)**, a
  WhatsApp AI sales product for restaurants — the screens where an owner sets up
  their whole agent (menu, prices, hours, personality) with nobody helping them.
  I rebuilt every step to fit the viewport instead of scrolling inside a long
  form, moved validation to where the error happens, made an interrupted
  onboarding resumable, and made it keyboard-accessible.
  *Next.js 16 · React 19 · TypeScript · Tailwind 4 · Supabase.*
- **I made [ChessLab](https://chesspwa.netlify.app) speak another language** —
  including the course content, not just the buttons. I translated lessons
  locally and fixed the images being lost in the translated markdown (a chess
  lesson without them is unreadable), added optional Supabase sign-in, and fixed
  a dead end where the last puzzle had no way back. *Sign-in required — the link
  is a product reference, not an open demo.*
- **I keep a bank automation alive in production.** A Google Apps Script reads
  Bancolombia alert emails and posts categorized transactions to Lunch Money
  every 5 minutes. **I didn't write it — I operate and fix it**, and I'd rather
  say so. When the bank changes an email format, the parser silently stops
  matching: no error, transactions just stop appearing. Finding and fixing that
  is the job.

My own favorite project is
**[honest-english](https://gibson1987r.github.io/honest-english/)**: most
language apps reward showing up, not improving. This one makes you speak into
the mic, scores what actually came out, and shows the gap between what you
understand and what you can produce. Vanilla JS, BYOK architecture, no backend.

**Stack:** JavaScript · TypeScript · React · Node.js · Python · Tailwind CSS ·
Supabase · Firebase · Vite · Git

I'm actively looking for junior frontend or automation roles, and I'm
improving my English every week.

📄 [Resume](https://cv-gibson-rosales.netlify.app) · ✉️ gibsonrosales@gmail.com

</details>
