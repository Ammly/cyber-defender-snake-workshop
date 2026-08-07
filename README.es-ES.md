

# 🛡️ CyberDefenderSnake — Taller de Safaricom De{c0}dE 2026

<p align="center">
  <img src="qr-code.png" alt="Código QR del Taller" width="250" />
</p>

Crea un juego de Snake de ciberseguridad desde cero utilizando **Agentes de IA para Codificación**.

👉 **Demo en Vivo:** [De{c0}dE Cyber Defender Snake Game](https://cyber-defender-snake.vercel.app/)

---

## Requisitos Previos

- Editor de código, p. ej., VSCode, Antigravity, Cursor, etc.
- Extensión de Agentes de IA, p. ej., Copilot, Claude Code, etc.

## 🛠️ Herramientas que puedes usar

### 💻 Editores sin conexión (Instálalos en tu portátil)

| Herramienta                                            | Agente de IA                                              | Gratuito               | Notas                                                |
| ---------------------------------------------------- | --------------------------------------------------------- | ---------------------- | ---------------------------------------------------- |
| [VS Code](https://code.visualstudio.com)             | [GitHub Copilot](https://github.com/features/copilot)     | ✅ Plan gratuito        | El más popular — recomendado para este taller        |
| [Google Antigravity](https://idx.google.com)         | Agente Gemini integrado                                   | ✅ Gratuito             | El nuevo IDE centrado en IA de Google, gran alternativa a Copilot |
| [Cursor](https://cursor.com)                         | Claude/GPT integrado                                      | ✅ Plan gratuito        | Editor nativo de IA, muy potente                     |
| [Windsurf](https://windsurf.com)                     | IA Cascade integrada                                      | ✅ Gratuito             | Fork de VS Code con IA gratuita generosa             |
| [Zed](https://zed.dev)                               | Claude/Gemini a través de API                             | ✅ Gratuito y código abierto | Extremadamente rápido, construido en Rust              |
| [Void](https://voideditor.com)                       | Cualquier modelo (trae tu propia clave)                   | ✅ Gratuito y código abierto | Alternativa de código abierto a Cursor               |

### 🌐 Editores en línea (No requiere instalación — solo abre un navegador)

| Herramienta                                                           | IA Integrada       | Notas                                                         |
| -------------------------------------------------------------------- | ------------------ | ------------------------------------------------------------- |
| [Replit](https://replit.com)                                         | ✅ Replit AI        | IDE completo en el navegador, alojamiento instantáneo, ideal para principiantes     |
| [StackBlitz](https://stackblitz.com)                                 | ✅ Bolt AI          | Ejecuta Node.js en el navegador, sensación de VS Code                     |
| [CodeSandbox](https://codesandbox.io)                                | ✅ Asistente de IA  | Entornos instantáneos, ideal para proyectos HTML/CSS/JS          |
| [CodePen](https://codepen.io)                                        | ✅ Sugerencias de IA| Lo mejor para demos rápidas de HTML/CSS/JS, no requiere registro           |
| [GitHub Codespaces](https://github.com/features/codespaces)          | ✅ GitHub Copilot   | VS Code completo en el navegador, impulsado por GitHub                |
| [Google AI Studio](https://aistudio.google.com)                      | ✅ Gemini          | Usa la IA para generar código y pégalo en cualquier editor            |
| [Claude.ai](https://claude.ai)                                       | ✅ Claude          | Pídele a Claude que escriba el código para cada paso y pégalo en cualquier editor |
| [bolt.new](https://bolt.new)                                         | ✅ Agente de IA     | Describe lo que quieres, la IA construye toda la aplicación               |

> **Para este taller**, se recomienda VS Code con GitHub Copilot o Google Antigravity. Si no puedes instalar nada, abre [CodePen](https://codepen.io) — crea tres archivos (HTML, CSS, JS), pega los prompts de `copilot-prompts.md` en Claude.ai o Google AI Studio y copia el resultado en CodePen. Funciona.

## Taller

Enlace al [taller](workshop/workshop_guide.md)

## Estructura del Repositorio

```
cyberdefender-workshop/
├── lessons.json          ← Descarga esto en tu proyecto
├── reference/            ← Implementación funcional (alternativa si la salida de la IA falla)
│   ├── index.html
│   ├── style.css
│   └── game.js
├── workshop/
│   ├── workshop_guide.md ← Comienza aquí
│   ├── 01-overview.md
│   ├── 02-setup.md
│   ├── 03-build.md
│   └── 04-threats-and-lessons.md
└── copilot-prompts.md    ← Prompts de rescate para cada paso
```

## Cómo Usarlo

1. Clona este repositorio
2. Abre `workshop/workshop_guide.md`
3. Sigue los pasos 01 → 04

---

*Safaricom De{c0}dE 2026*
