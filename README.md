# skills-ui-antigravity

Adaptación global para **Google Antigravity** de la suite de skills de diseño UI y animaciones de [Emil Kowalski (`emilkowalski/skills`)](https://github.com/emilkowalski/skills), más el comando orquestador **`/emil-ui`** para aplicar toda la suite de forma unificada.

## Qué incluye esta adaptación

- **Plugin global de Antigravity (`plugin.json`)**: listo para instalarse en `~/.gemini/config/plugins/emilkowalski-skills/` y estar disponible automáticamente en todos tus proyectos.
- **Orquestador `/emil-ui`**: una skill general (`skills/emil-ui/SKILL.md`) que detecta tu plataforma (Web, Expo/React Native o Swift) y carga dinámicamente solo las skills necesarias del paquete, aplicando el flujo completo de diseño, selección de librerías, animaciones, rendimiento, móvil y auto-revisión.
- **Frontmatter compatible con Antigravity**: se eliminó `disable-model-invocation: true` (específico de Claude Code) en las 5 skills que lo incluían para permitir activación automática y explícita.
- **Adaptación de `learn-taste`**: rutas actualizadas para transcripciones de Antigravity (`~/.gemini/antigravity/brain/<conversation-id>/.system_generated/logs/transcript.jsonl`) y archivos de reglas `GEMINI.md` / `AGENTS.md` / `.agents/skills/`.

## Instalación global en Antigravity

Copia el contenido de este repositorio en tu carpeta global de plugins de Antigravity:

- **Windows (PowerShell)**:
  ```powershell
  git clone https://github.com/jdsgnrinfo/skills-ui-antigravity.git "$env:USERPROFILE\.gemini\config\plugins\emilkowalski-skills"
  ```
- **macOS / Linux**:
  ```bash
  git clone https://github.com/jdsgnrinfo/skills-ui-antigravity.git ~/.gemini/config/plugins/emilkowalski-skills
  ```

Antigravity descubrirá el plugin automáticamente y habilitará las **21 skills** en todos tus proyectos.

## Uso rápido con `/emil-ui`

- `/emil-ui` — Activa la suite completa para toda la sesión.
- `/emil-ui <tarea>` — Construye o rediseña un componente/pantalla aplicando las skills relevantes.
- `/emil-ui polish` — Pulido visual, animaciones, móvil y rendimiento sobre UI existente.
- `/emil-ui review` — Revisión estricta de tus cambios actuales de animación y UI.
- `/emil-ui audit` — Auditoría completa del repositorio con planes priorizados.
- `/emil-ui prototype <idea>` — Genera múltiples variantes con selector visual en vivo.
- `/emil-ui break` — Prueba de estrés con datos extremos (*worst-case*).
- `/emil-ui learn` — Convierte tus correcciones de diseño en reglas en `DESIGN.md`.

## Skills incluidas (21)

- **Orquestador**: `emil-ui`
- **Animación y movimiento web**: `emil-design-eng`, `animate`, `choreograph`, `gestures`, `animation-performance`, `animation-vocabulary`, `review-animations`, `improve-animations`, `find-animation-opportunities`, `remove-animations`
- **Diseño, UI y librerías**: `apple-design`, `pick-ui-library`, `prototype`, `mobile-native`, `break-ui`, `ask-sonner`
- **Móvil nativo**: `animate-expo`, `write-swift`
- **Flujo y aprendizaje**: `ask-emil`, `learn-taste`

## Créditos

Basado en el trabajo original de [Emil Kowalski](https://emilkowal.ski) — [emilkowalski/skills](https://github.com/emilkowalski/skills) ([aiforui.dev/skills](https://aiforui.dev/skills)), bajo licencia MIT.
