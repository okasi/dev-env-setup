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
  // Saving
  "files.autoSave": "onFocusChange",
  // Startup screen
  "workbench.startupEditor": "newUntitledFile",
  // Font
  "editor.fontSize": 16,
  "editor.fontFamily": "FiraCode Nerd Font Mono, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "editor.cursorBlinking": "phase",
  // Terminal
  "terminal.integrated.fontSize": 15,
  "terminal.integrated.fontFamily": "UbuntuMono Nerd Font Mono, 'Courier New', monospace",
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
    "oh-my-zsh",
    "fish",
    "oh-my-bash"
  ],
  "terminal.integrated.profiles.osx": {
    "preinstalled-zsh": {
      "path": "/bin/zsh"
    }
  },
  "terminal.integrated.defaultProfile.osx": "preinstalled-zsh",
  "terminal.integrated.commandsToSkipShell": [
    "-workbench.action.quickOpenView"
  ],
  // Icon theme
  "workbench.iconTheme": "material-icon-theme",
  // Workbench theme
  "workbench.colorTheme": "GitHub Dark Default",
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      // Italic comments
      {
        "scope": "comment",
        "settings": {
          "fontStyle": "italic"
        }
      },
      // Italic parameters
      {
        "scope": [
          "variable.parameter",
          "entity.name.variable.parameter",
          "parameter.variable"
        ],
        "settings": {
          "fontStyle": "italic"
        }
      },
      // Light beige strings
      {
        "scope": "string",
        "settings": {
          "foreground": "#F1C677"
        }
      }
    ]
  },
  // Disable preview
  "workbench.editor.enablePreview": false,
  "workbench.editor.enablePreviewFromQuickOpen": false,
  "workbench.editor.showTabs": true,
  // Trust files
  "security.workspace.trust.untrustedFiles": "open",
  // Suggestions
  "editor.quickSuggestions": {
    "other": true,
    "comments": false,
    "strings": false
  },
  // Slight delay for suggestions to appear (ms), better performance
  "editor.quickSuggestionsDelay": 110,
  // Show parent directories / folder names in tab of file
  "workbench.editor.labelFormat": "medium",
  // Formatting
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  // Linting
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  // Linting - ESLint specific
  "eslint.runtime": "node",
  "eslint.format.enable": true,
  "eslint.codeActionsOnSave.mode": "problems",
  "eslint.options": {
    "overrideConfig": {
      "env": {
        "browser": true,
        "node": true
      },
      "parserOptions": {
        "ecmaVersion": 2017
      },
      "rules": {
        "prettier/prettier": "error",
      }
    }
  },
  // Prevents VS Code linting JavaScript with the default linter
  "javascript.validate.enable": false,
  // Prevents VS Code from formatting JavaScript with the default linter
  "javascript.format.enable": false,
  // Bracket pair color
  "editor.guides.bracketPairs": true,
  // Typescript
  "typescript.tsdk": "node_modules/typescript/lib",
  // Experimental TypeScript / JavaScript options
  "typescript.disableAutomaticTypeAcquisition": true,
  "js/ts.implicitProjectConfig.experimentalDecorators": true,
  // Associate file extensions with corresponding syntax
  "files.associations": {
    "*.jsx": "javascriptreact",
    "*.tsx": "typescriptreact",
    "*.graphql": "graphql"
  },
  // Formatters
  "[javascript][typescript][javascriptreact][typescriptreact]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "[json][jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[html][liquid]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "[css][scss][less]": {
    "editor.defaultFormatter": "vscode.css-language-features"
  },
  "[svelte]": {
    "editor.defaultFormatter": "svelte.svelte-vscode"
  },
  // Disable telemetry
  "telemetry.telemetryLevel": "off",
  "extensions.autoCheckUpdates": false,
  "workbench.enableExperiments": false,
  "workbench.settings.enableNaturalLanguageSearch": false,
  // Always show minimap
  "editor.minimap.showSlider": "always",
  // Shows line of blocks, better performance
  "editor.minimap.renderCharacters": false,
  // Exclude watching some files, for performance
  "files.watcherExclude": {
    "**/.git/**": true,
    "**/node_modules/**": true,
    "**/.yarn/**": true,
    "**/.idea/**": true,
    "**/.cache/**": true,
    "**/.next/**": true,
    "**/_next/**": true,
    "**/next-env.d.ts": true,
    "**/out/**": true,
    "**/build/**": true,
    "**/dist/**": true,
    "**/.swc/**": true,
    "**/__snapshots__/**": true,
    "**/storybook-static/**": true,
    "**/tmp/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    "**/bower_components/**": true,
    "**/{log,logs}/**": true,
    "**/.fdk/**": true,
    "**/.npm/**": true,
    "**/coverage/**": true,
    "**/.eslintcache": true,
    "**/.DS_Store": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    "**/*.tsbuildinfo": true
  },
  "search.exclude": {
    "**/.git/**": true,
    "**/node_modules/**": true,
    "**/.yarn/**": true,
    "**/.idea/**": true,
    "**/.cache/**": true,
    "**/.next/**": true,
    "**/_next/**": true,
    "**/next-env.d.ts": true,
    "**/out/**": true,
    "**/build/**": true,
    "**/dist/**": true,
    "**/.swc/**": true,
    "**/__snapshots__/**": true,
    "**/storybook-static/**": true,
    "**/tmp/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    "**/bower_components/**": true,
    "**/{log,logs}/**": true,
    "**/.fdk/**": true,
    "**/.npm/**": true,
    "**/coverage/**": true,
    "**/.eslintcache": true,
    "**/.DS_Store": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    "**/*.tsbuildinfo": true
  },
  // Spelling check languages
  "cSpell.language": "en,sv",
  // Github Copilot settings
  "github.copilot.enable": {
    "*": true
  },
  // Window settings
  "window.restoreWindows": "folders",
  "window.nativeTabs": true,
  "window.title": "${rootName}",
  "window.zoomLevel": -1,
  "editor.inlineSuggest.enabled": true
}
```
