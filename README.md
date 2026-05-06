# Math Problem Generator — Questionnaire Editor

A single-page web app for designing and previewing math problem prompts before sending them to an AI generator.

## Quick Start

Open `index.html` directly in any modern browser. No server, build step, or dependencies required.

## Features

- **Questionnaire Editor** — Add, remove, reorder, and configure parameter rows
- **Multiple Choice / Text Input** — Each row can be a chip-based selector or free-text field
- **Brainstorming Sidebar** — Click any idea card to inject it into the prompt
- **Profile Settings** — Click the avatar in the header to fill in profile info
- **Profile Switching** — "Switch Profile" simulates a multi-account workflow
- **More Options** — A collapsible section with additional parameters (Grade Level, Language, Context, etc.)
- **Auto Prompt Preview** — The prompt textarea updates live as you configure entries
- **Minimize Prompt** — Collapse the prompt box to save screen space
- **Generate** — Simulates AI generation with sample output

## Layout

```
+------------------+----------------------------------+
| App Title        |  [Switch Profile] [Avatar]     |
+------------------+----------------------------------+
| Brainstorming    |  Questionnaire Editor            |
| Ideas            |                                  |
| (sidebar)        |  Main Parameters [+]             |
|                  |    > Area (chips)                |
| - Real-World...  |    > Difficulty (chips)          |
| - Multi-Step...  |    > Type (chips)               |
| - Visual...      |    > Additional Instructions     |
| ...              |                                  |
|                  |  More Options (collapsible) [+]  |
|                  |    > Grade Level (chips)         |
|                  |    > Language (chips)            |
|                  |    > ...                         |
|                  |                                  |
|                  |  Prompt Preview [−]             |
|                  |  [textarea with auto-generated   |
|                  |   prompt text]                   |
|                  |                                  |
|                  |  [ Generate Problem ]           |
+------------------+----------------------------------+
```

## Customization

- **Add new entry templates**: Edit the `ENTRY_TEMPLATES` object in the `<script>` section
- **Add brainstorm items**: Add elements to the `#sidebarItems` div
- **Theme**: Modify CSS variables in the `:root` block (e.g. `--primary`, `--bg`, `--surface`)

## Browser Support

Tested on Chrome, Firefox, Safari, and Edge. Requires no polyfills.
