### Get list of VSCode extensions with:  
```zsh
code --list-extensions | xargs -L 1 echo code --install-extension
```

### List of all extensions:
```zsh
# Linters & Formaters
code --install-extension dbaeumer.vscode-eslint

# Themeing
code --install-extension PKief.material-icon-theme
code --install-extension usernamehw.errorlens
code --install-extension oderwat.indent-rainbow

# Gitlens (See git history)
code --install-extension maattdd.gitless

# Spell checker
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension streetsidesoftware.code-spell-checker-swedish

# Autocomplete
code --install-extension bradlc.vscode-tailwindcss

# AI 
code --install-extension continue.continue
```

---

## User Settings (JSON):
```json
{
  // General
  "telemetry.telemetryLevel": "off",
  "workbench.enableExperiments": false,
  "workbench.settings.enableNaturalLanguageSearch": false,
  "update.showReleaseNotes": false,
  "application.shellEnvironmentResolutionTimeout": 45,
  "security.workspace.trust.untrustedFiles": "open",
  "http.noProxy": [
    "*"
  ],
  // UI / Workbench
  "window.nativeTabs": true,
  "window.title": "${rootName}",
  "window.restoreWindows": "folders",
  "window.zoomLevel": -0.75,
  "workbench.startupEditor": "newUntitledFile",
  "workbench.colorTheme": "Monokai",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.editor.enablePreview": false,
  "workbench.editor.labelFormat": "medium",
  "workbench.editor.limit.enabled": true,
  "workbench.editor.limit.perEditorGroup": true,
  "workbench.editor.limit.value": 8,
  // Editor
  "editor.fontSize": 15,
  "editor.fontFamily": "FiraCode Nerd Font Mono, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "editor.cursorBlinking": "phase",
  "editor.guides.bracketPairs": true,
  "editor.minimap.renderCharacters": false,
  "editor.minimap.showSlider": "always",
  "editor.minimap.autohide": true,
  "editor.quickSuggestionsDelay": 134,
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit"
  },
  "editor.accessibilitySupport": "off",
  "editor.stickyScroll.enabled": false,
  // Files & Saving
  "files.autoSave": "onFocusChange",
  "files.associations": {
    "*.jsx": "javascriptreact",
    "*.tsx": "typescriptreact",
    "*.graphql": "graphql"
  },
  "files.exclude": {
    "**/.git": false
  },
  // Language-specific Formatters
  "[json][jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[html][liquid]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "[css][scss][less]": {
    "editor.defaultFormatter": "vscode.css-language-features"
  },
  // "[javascript][typescript][javascriptreact][typescriptreact]": {
  //   "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  // },
  // // Linting
  // "eslint.useFlatConfig": true,
  // "eslint.runtime": "node",
  // "eslint.codeActionsOnSave.mode": "problems",
  // "eslint.options": {
  //   "overrideConfig": {
  //     "rules": {
  //       "prettier/prettier": "error",
  //     }
  //   }
  // },
  "css.lint.unknownAtRules": "ignore",
  "javascript.validate.enable": false,
  "javascript.format.enable": false,
  // TypeScript / JavaScript
  "typescript.updateImportsOnFileMove.enabled": "always",
  "javascript.updateImportsOnFileMove.enabled": "always",
  // Terminal
  "terminal.integrated.fontSize": 14,
  "terminal.integrated.fontFamily": "UbuntuMono Nerd Font Mono, 'Courier New', monospace",
  "terminal.integrated.commandsToSkipShell": [
    "-workbench.action.quickOpenView"
  ],
  "terminal.integrated.env.windows": {
    "LC_ALL": "C.UTF-8"
  },
  "terminal.integrated.env.osx": {
    "LC_ALL": "C.UTF-8"
  },
  "terminal.integrated.ignoreProcessNames": [
    "starship",
    "zsh",
    "bash",
  ],
  // Git
  "git.autofetch": true,
  // Spelling
  "cSpell.language": "en,sv",
  // Excludes (watcher, search, etc.)
  "files.watcherExclude": {
    // Version Control Systems
    "**/.git/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    // Package Managers and Lock Files
    "**/node_modules/**": true,
    "**/.yarn/**": true,
    "**/.npm/**": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    // IDE/Editor Configurations
    "**/.idea/**": true,
    "**/.DS_Store": true,
    // Build and Distribution Directories
    "**/out/**": true,
    "**/build/**": true,
    "**/dist/**": true,
    "**/storybook-static/**": true,
    "**/tmp/**": true,
    // Cache and Temporary Files
    "**/.cache/**": true,
    "**/.eslintcache": true,
    "**/__snapshots__/**": true,
    "**/.swc/**": true,
    // Project Specific
    "**/_next/**": true,
    "**/.next/**": true,
    "**/next-env.d.ts": true,
    "**/*.tsbuildinfo": true,
    "**/{log,logs}/**": true,
    "**/.fdk/**": true,
    "**/coverage/**": true,
    "**/bower_components/**": true,
    "**/.mypy_cache/**": true,
    "**/.pytest_cache/**": true,
    "**/.ruff_cache/**": true,
    "**/mlruns/**": true
  },
  "search.exclude": {
    // Version Control Systems
    "**/.git/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    // Package Managers and Lock Files
    "**/node_modules/**": true,
    "**/.yarn/**": true,
    "**/.npm/**": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    // IDE/Editor Configurations
    "**/.idea/**": true,
    "**/.DS_Store": true,
    // Build and Distribution Directories
    "**/out/**": true,
    "**/build/**": true,
    "**/dist/**": true,
    "**/storybook-static/**": true,
    "**/tmp/**": true,
    // Cache and Temporary Files
    "**/.cache/**": true,
    "**/.eslintcache": true,
    "**/__snapshots__/**": true,
    "**/.swc/**": true,
    // Project Specific
    "**/_next/**": true,
    "**/.next/**": true,
    "**/next-env.d.ts": true,
    "**/*.tsbuildinfo": true,
    "**/{log,logs}/**": true,
    "**/.fdk/**": true,
    "**/coverage/**": true,
    "**/bower_components/**": true,
    "**/.mypy_cache/**": true,
    "**/.pytest_cache/**": true,
    "**/.ruff_cache/**": true,
    "**/mlruns/**": true
  },
  // Chat/AI
  "chat.commandCenter.enabled": false
}
```
