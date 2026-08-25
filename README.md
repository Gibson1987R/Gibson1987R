# Hola, soy Gibson Rosales 👋

**Desarrollador web junior.** Fui profesor de matemáticas durante años; hoy
construyo las herramientas que antes resolvía a mano. Enseñar me dejó dos
costumbres que uso a diario: descomponer un problema hasta que se vuelve
obvio, y explicar la solución en palabras que cualquiera entienda.

📄 **[Mi CV en la web](https://cv-gibson-rosales.netlify.app)** · ✉️ gibsonrosales@gmail.com · 📍 Medellín, Colombia — remoto o presencial

---

## Trabajo real, en repos privados

Lo que más he construido este año está en repos de clientes, así que no puedo
enlazar el código. Lo cuento aquí con lo que sí es verificable: el producto en
vivo, lo que hice yo, y con quién.

### 🍽️ Directo IA — flujo de onboarding · [producto en vivo](https://www.directoia.com/)

Un restaurante vende por WhatsApp con un agente de IA y opera lo vendido desde
un dashboard. El problema que me tocó: **el dueño del restaurante tiene que
configurar su agente —menú, precios, horarios, personalidad, reglas de
operación— sin que nadie lo acompañe.** Si se pierde en ese formulario, no hay
producto.

Soy responsable del flujo de onboarding: **41 commits, PRs #10 al #39** (julio
2026). Lo que resolví ahí:

- **Que quepa en una pantalla, en cualquier pantalla.** Cada paso del flujo se
  adapta al alto disponible en vez de obligar a hacer scroll dentro de un
  formulario largo — el momento donde la gente abandona.
- **Validación que se explica sola.** Los errores los dice el robot del producto,
  en el paso donde ocurren, y se apagan en cuanto el usuario toca el campo. Las
  secciones incompletas se resaltan al intentar avanzar.
- **Recuperar a quien vuelve a medias.** Retomar el onboarding desde un estado
  incompleto valida bien y no pierde lo ya escrito.
- **Accesible con teclado** y sin romperse con textos largos ni en móvil.

**Stack:** Next.js 16 (App Router) · React 19 · TypeScript · Tailwind 4 ·
Supabase (Postgres, Auth, Realtime) · n8n · WhatsApp vía GoHighLevel · Vercel.

### ♟️ ChessLab — PWA de cursos de ajedrez · [app en vivo](https://chesspwa.netlify.app)

Una aplicación instalable que convierte un curso de ajedrez en lecciones y
ejercicios que **funcionan sin conexión**. Mi parte, en **37 commits**
(julio–agosto 2026): la **internacionalización completa** —incluida la
traducción local del contenido del curso, preservando las imágenes de cada
lección—, la **autenticación opcional con Supabase** (PR #29) y la navegación
entre ejercicios, que dejaba al usuario en un callejón sin salida al llegar
al último.

**Stack:** PWA offline · Supabase · Netlify.

> Requiere cuenta para entrar: el enlace es la referencia del producto, no una
> demo abierta.

### 💸 Bancolombia → Lunch Money — automatización en producción

Bancolombia no está soportado por Plaid ni Belvo para personas naturales, así
que las transacciones se registran a mano o no se registran. La solución: un
**Google Apps Script que corre dentro de la cuenta de Google del cliente**, lee
las alertas del banco que llegan al correo, las parsea y crea la transacción ya
categorizada en **[Lunch Money](https://lunchmoney.app)**. Cada 5 minutos, sin
que nadie lo toque. **No tiene dirección web propia:** es un script que corre
dentro de la cuenta de Google del cliente, sin interfaz.

**Soy honesto con mi papel aquí: el sistema lo escribió su autor; yo lo opero y
lo mantengo** para el cliente que lo usa a diario. Cuando el banco cambia el
formato de un correo, el parser deja de reconocerlo y las transacciones se caen
en silencio — encontrar ese caso, reproducirlo y arreglar la regla es mi trabajo.
Es el proyecto que me enseñó que en automatización lo difícil no es escribirla:
es que siga funcionando el martes.

**Stack:** Google Apps Script · GmailApp · API de Lunch Money · clasp.

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

**Client work lives in private repos, so here is what's verifiable:**

- **[Directo IA](https://www.directoia.com/)** — a WhatsApp AI sales product
  for restaurants. I own the **onboarding flow**: 41 commits, PRs #10–#39. The
  restaurant owner has to configure their whole agent — menu, prices, hours,
  personality — with nobody helping them; if they get lost in that form, there
  is no product. I made every step fit the viewport, moved validation to where
  the error happens, made an interrupted onboarding resumable, and made it
  keyboard-accessible. *Next.js 16 · React 19 · TypeScript · Tailwind 4 ·
  Supabase · n8n · Vercel.*
- **[ChessLab](https://chesspwa.netlify.app)** — an installable PWA that turns
  a chess course into offline lessons and puzzles. 37 commits: full
  internationalization (including local translation of course content),
  optional Supabase auth, and puzzle navigation. *Sign-in required — the link
  is a product reference, not an open demo.*
- **Bancolombia → Lunch Money** — a Google Apps Script that reads bank alert
  emails and posts categorized transactions automatically, every 5 minutes.
  **To be precise about my role: I didn't write it, I operate and maintain it**
  for the client who depends on it daily. When the bank changes an email
  format, the parser silently stops matching — finding and fixing that is my
  job. Automation is easy to write and hard to keep alive.

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
