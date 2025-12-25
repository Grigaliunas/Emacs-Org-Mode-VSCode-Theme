# Emacs Org Mode Theme Pack (Obsidian + VS Code)

Courier New + dark palette theme set for:
- **Obsidian** (theme folder)
- **Visual Studio Code** (theme extension + raw theme JSON)

## Contents

### Obsidian theme
Folder: `Emacs-Org-Mode/`
- `manifest.json`
  - `name`: `Emacs Org Mode`
  - `version`: `1.0.0`
  - `minAppVersion`: `1.0.0`
  - `author`: `Ailia`
- `theme.css`

### VS Code theme
Folder: `emacs-org-mode-theme/`
- `package.json`
  - `name`: `emacs-org-mode-theme`
  - `displayName`: `Emacs Org Mode Theme`
  - `version`: `0.0.1`
  - `publisher`: `ailia`
  - `engines.vscode`: `^1.80.0`
- `themes/Emacs Org Mode-color-theme.json`

Extra file (same theme JSON, for direct inspection/copy):
- `Emacs-Org-Mode-color-theme.json`

## Palette (from `index.html`)

- Backgrounds:
  - `#1c1c1c` (page/sidebar)
  - `#282828` (buffer/editor)
  - `#2a2a2a` (panels)
  - `#2f2f2f` (counters/selection base)
  - `#343434` (modeline/status)
  - `#383838` (header/title bar)
- Borders/dim:
  - `#696969` (borders)
  - `#505050` (dashed underline / dim UI)
- Text:
  - `#d0d0d0` (default)
  - `#c0c0c0` (muted)
  - `#dcdccc` (counter text)
- Accents:
  - `#7cb8bb` (cyan)
  - `#8cd0d3` (bright cyan)
  - `#93e0e3` (link teal)
  - `#6fb86f` (green)
  - `#f0dfaf` (yellow)
  - `#7f9f7f` (comment green)
  - `#cc9393` (red)

## Install

### VS Code

#### Option A — local extension folder
1. Copy `emacs-org-mode-theme/` into your VS Code extensions dir:
   - Windows: `%USERPROFILE%\\.vscode\\extensions\\emacs-org-mode-theme\\`
   - macOS: `~/.vscode/extensions/emacs-org-mode-theme/`
   - Linux: `~/.vscode/extensions/emacs-org-mode-theme/`
2. Restart VS Code.
3. Command Palette → **Preferences: Color Theme** → select **Emacs Org Mode**.

#### Option B — package a `.vsix` (vsce)
Requirements:
- Node.js + npm
- `vsce` (`@vscode/vsce`)

Commands:

```bash
npm i -g @vscode/vsce
cd emacs-org-mode-theme
vsce package
code --install-extension emacs-org-mode-theme-0.0.1.vsix
```

## Matching the font in VS Code

Theme files do not set editor font settings. To use the same font family as `index.html`:

```json
{
  "editor.fontFamily": "Courier New, monospace",
  "editor.fontLigatures": false
}
```

## Edit / dev workflow

### Obsidian
- Edit: `Emacs-Org-Mode/theme.css`
- Reload: toggle theme or restart Obsidian.

### VS Code
- Edit: `emacs-org-mode-theme/themes/Emacs Org Mode-color-theme.json`
- Reload: Command Palette → **Developer: Reload Window**.

## Notes
- Theme outputs are CSS (Obsidian) + JSON (VS Code).
