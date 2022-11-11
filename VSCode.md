Get list of VSCode extensions with:  
```
code --list-extensions | xargs -L 1 echo code --install-extension
```

List of all extensions:
```
code --install-extension bradlc.vscode-tailwindcss
code --install-extension christian-kohler.path-intellisense
code --install-extension eamodio.gitlens
code --install-extension GraphQL.vscode-graphql-syntax
code --install-extension mikestead.dotenv
code --install-extension mrorz.language-gettext
code --install-extension pflannery.vscode-versionlens
code --install-extension quicktype.quicktype
code --install-extension svelte.svelte-vscode
code --install-extension Tyriar.sort-lines
code --install-extension usernamehw.errorlens

# Theming
code --install-extension github.github-vscode-theme
code --install-extension PKief.material-icon-theme
code --install-extension oderwat.indent-rainbow

# Linters
code --install-extension dbaeumer.vscode-eslint
code --install-extension rome.rome

# YAML
code --install-extension redhat.vscode-yaml

# VCL
code --install-extension thomas-baumgaertner.vcl
```

User Settings (JSON):
```
{
  // Saving
  "files.autoSave": "onFocusChange",
  "files.autoSaveDelay": 800,
  // Always show minimap
  "editor.minimap.showSlider": "always",
  // Shows line of blocks, better performance
  "editor.minimap.renderCharacters": false,
  "workbench.startupEditor": "newUntitledFile",
  // Theme & Icons
  "material-icon-theme.folders.theme": "specific",
  "workbench.iconTheme": "material-icon-theme",
  // Workspace tabs
  "window.nativeTabs": true,
  "window.title": "${rootName}",
  // Window zoom
  "window.zoomLevel": -1,
  // Font
  "editor.fontFamily": "FiraCode Nerd Font Mono, Menlo, monospace",
  "editor.fontLigatures": true,
  "editor.fontSize": 16,
  "editor.cursorBlinking": "phase",
  // Terminal
  "terminal.integrated.defaultProfile.osx": "preinstalled-zsh",
  "terminal.integrated.profiles.osx": {
    "preinstalled-zsh": {
      "path": "/bin/zsh", // Explicitly specify preinstalled zsh
    },
  },
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.fontFamily": "UbuntuMono Nerd Font Mono, Menlo, monospace",
  "terminal.integrated.env.windows": {
    "LC_ALL": "C.UTF-8"
  },
  "terminal.integrated.env.osx": {
    "LC_ALL": "C.UTF-8"
  },
  "terminal.integrated.ignoreProcessNames": [
    "starship",
    "zsh"
  ],
  // Reopen workspace on start
  "window.restoreWindows": "folders",
  // Disable preview
  "workbench.editor.enablePreview": false,
  "workbench.editor.enablePreviewFromQuickOpen": false,
  "workbench.editor.showTabs": true,
  // Trust files
  "security.workspace.trust.untrustedFiles": "open",
  // Exlude watching some files, for performance
  "files.watcherExclude": {
    "**/.git/objects/**": true,
    "**/.git/subtree-cache/**": true,
    "**/.git": true,
    "**/.cache/**": true,
    "**/node_modules/**": true,
    "**/node_modules/": true,
    "**/.yarn/**": true,
    "**/.yarn/": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    "**/public/**": true,
    "**/tmp/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/tsconfig.tsbuildinfo": true,
    "**/.eslintcache": true,
    "**/CVS": true,
    "**/.DS_Store": true,
    "**/bower_components": true,
    "**/dist/**": true,
    "**/log/**": true,
    "**/logs/**": true,
    "**/.fdk/**": true
  },
  "search.exclude": {
    "**/.git/objects/**": true,
    "**/.git/subtree-cache/**": true,
    "**/.git": true,
    "**/.cache/**": true,
    "**/node_modules/**": true,
    "**/node_modules/": true,
    "**/.yarn/**": true,
    "**/.yarn/": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/pnpm-lock.yaml": true,
    "**/public/**": true,
    "**/tmp/**": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/tsconfig.tsbuildinfo": true,
    "**/.eslintcache": true,
    "**/CVS": true,
    "**/.DS_Store": true,
    "**/bower_components": true,
    "**/dist/**": true,
    "**/log/**": true,
    "**/logs/**": true,
    "**/.fdk/**": true
  },
  // Suggestions
  "editor.quickSuggestions": {
    "other": true,
    "comments": false,
    "strings": false
  },
  "editor.quickSuggestionsDelay": 90,
  // Gitlens
  "gitlens.views.repositories.location": "gitlens",
  "gitlens.views.fileHistory.location": "gitlens",
  "gitlens.views.lineHistory.location": "gitlens",
  "gitlens.views.compare.location": "gitlens",
  "gitlens.views.search.location": "gitlens",
  // Confirm delete
  "explorer.confirmDelete": true,
  // Automaticly fetch
  "git.autofetch": true,
  // No need to confirm sync
  "git.confirmSync": false,
  // Color for git status
  "git.decorations.enabled": true,
  // No need to confirm drag and drop
  "explorer.confirmDragAndDrop": false,
  // Show parent folder name in tab of file
  "workbench.editor.labelFormat": "short",
  // Format
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": false,
  "emmet.preferences": {
    "output.inlineBreak": 1
  },
  // Linting
  "eslint.runtime": "node",
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
  ],
  "eslint.enable": true,
  "eslint.format.enable": true,
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
        "arrow-body-style": "off",
        "prefer-arrow-callback": "off"
      }
    }
  },
  "eslint.codeActionsOnSave.mode": "problems",
  "editor.codeActionsOnSave": {
    "source.fixAll": true
  },
  // Disable telemetry
  "telemetry.telemetryLevel": "off",
  "enable-crash-reporter": false,
  "workbench.enableExperiments": false,
  "workbench.settings.enableNaturalLanguageSearch": false,
  "extensions.autoCheckUpdates": false,
  // Bracket pair color
  "editor.guides.bracketPairs": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.highlightActiveIndentation": true,
  "editor.guides.bracketPairsHorizontal": "active",
  // Typescript & Experimental JavaScript options
  "typescript.disableAutomaticTypeAcquisition": true,
  "js/ts.implicitProjectConfig.experimentalDecorators": true,
  "typescript.tsdk": "node_modules/typescript/lib",
  // Prevents VS Code linting JavaScript with the default linter
  "javascript.validate.enable": false,
  // Prevents VS Code from formatting JavaScript with the default linter
  "javascript.format.enable": false,
  // Associate JSX & TSX with React syntax
  "files.associations": {
    "*.tsx": "typescriptreact",
    "*.jsx": "javascriptreact",
    "*.graphql": "graphql"
  },
  // Formatters
  "[javascript][typescript]": {
    "editor.defaultFormatter": "rome.rome"
  },
  "[javascriptreact][typescriptreact]": {
    "editor.defaultFormatter": "vscode.typescript-language-features"
  },
  "[json][jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "css.format.enable": true,
  "[css][scss][less]": {
    "editor.defaultFormatter": "vscode.css-language-features"
  },
  "workbench.colorTheme": "GitHub Dark Default",
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "comment",
        "settings": {
          "fontStyle": "italic"
        }
      },
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
      {
        "scope": "string",
        "settings": {
          "foreground": "#e5c07b"
        }
      }
    ]
  },
  "terminal.integrated.commandsToSkipShell": [
    "-workbench.action.quickOpenView"
  ],
}
```
