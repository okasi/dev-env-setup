Get list of VSCode extensions with:  
```
code --list-extensions | xargs -L 1 echo code --install-extension
```

List of all extensions:
```
code --install-extension bbenoist.Nix
code --install-extension bmewburn.vscode-intelephense-client
code --install-extension bradlc.vscode-tailwindcss
code --install-extension christian-kohler.path-intellisense
code --install-extension CoenraadS.bracket-pair-colorizer-2
code --install-extension csantiago132.intellij-ish-darcula-theme
code --install-extension dbaeumer.vscode-eslint
code --install-extension dsznajder.es7-react-js-snippets
code --install-extension eamodio.gitlens
code --install-extension esbenp.prettier-vscode
code --install-extension GraphQL.vscode-graphql
code --install-extension hashicorp.terraform
code --install-extension jpoissonnier.vscode-styled-components
code --install-extension jtladeiras.vscode-inline-sql
code --install-extension kokororin.vscode-phpfmt
code --install-extension mgmcdermott.vscode-language-babel
code --install-extension mikestead.dotenv
code --install-extension ms-mssql.mssql
code --install-extension ms-python.python
code --install-extension ms-toolsai.jupyter
code --install-extension ms-vscode.typescript-javascript-grammar
code --install-extension mtxr.sqltools
code --install-extension octref.vetur
code --install-extension oderwat.indent-rainbow
code --install-extension petemill.theme-readable-material-darker
code --install-extension pflannery.vscode-versionlens
code --install-extension PKief.material-icon-theme
code --install-extension quicktype.quicktype
code --install-extension rbbit.typescript-hero
code --install-extension thomas-baumgaertner.vcl
code --install-extension tungvn.wordpress-snippet
code --install-extension Tyriar.sort-lines
code --install-extension whtouche.vscode-js-console-utils
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

  // Reopen workspace on start
  "window.restoreWindows": "folders",

  // Disable preview
  "workbench.editor.enablePreview": false,
  "workbench.editor.enablePreviewFromQuickOpen": false,
  "workbench.editor.showTabs": true,

  // Exlude watching some files, for performance
  "files.watcherExclude": {
    "**/.git/objects/**": true,
    "**/.git/subtree-cache/**": true,
    "**/.cache/**": true,
    "**/node_modules/**": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/public/**": true,
    "**/tmp/**": true,
    "**/.git": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    "**/.DS_Store": true,
    "**/node_modules": true,
    "**/bower_components": true,
    "**/dist/**": true,
    "**/log/**": true,
    "**/logs/**": true,
    "**/.fdk/**": true
  },
  "search.exclude": {
    "**/.git/objects/**": true,
    "**/.git/subtree-cache/**": true,
    "**/.cache/**": true,
    "**/node_modules/**": true,
    "**/package-lock.json": true,
    "**/yarn.lock": true,
    "**/public/**": true,
    "**/tmp/**": true,
    "**/.git": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    "**/.DS_Store": true,
    "**/node_modules": true,
    "**/bower_components": true,
    "**/dist/**": true,
    "**/log/**": true,
    "**/logs/**": true,
    "**/.fdk/**": true
  },
  "terminal.integrated.fontSize": 13,

  // Font
  "editor.fontFamily": "FiraCode Nerd Font Mono, Menlo, monospace",
  "editor.fontLigatures": true,
  "editor.fontSize": 18,
  "editor.cursorBlinking": "phase",

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

  // Prevents VS Code linting JavaScript with the default linter
  "javascript.validate.enable": false,

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

  // Associate JSX & TSX with React syntax
  "files.associations": {
    "*.tsx": "typescriptreact",
    "*.jsx": "javascriptreact"
  },

  // Format
  "editor.tabSize": 2,
  "editor.defaultFormatter": "standard.vscode-standard",
  "editor.formatOnSave": true,
  // "editor.formatOnSaveMode": "modifications",
  "editor.formatOnPaste": false,
  "prettier.singleQuote": true,
  "prettier.semi": false,
  "emmet.preferences": { "output.inlineBreak": 1 },

  // Linting
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],

  "eslint.codeActionsOnSave.mode": "problems",
  "editor.codeActionsOnSave": {
    // "source.organizeImports": true,
    "eslint.format.enable": true
    // "source.fixAll.eslint": true,
    // "source.fixAll": true
  },

  "python.pythonPath": "/usr/local/bin/python3",

  // Typescript settings
  "typescript.disableAutomaticTypeAcquisition": true,

  // Terminal settings
  "terminal.integrated.defaultProfile.osx": "zsh",
  "terminal.integrated.env.windows": {
    "LC_ALL": "C.UTF-8"
  },
  "terminal.integrated.env.osx": {
    "LC_ALL": "C.UTF-8"
  },

  // Disable telemetry
  "workbench.enableExperiments": false,
  "workbench.settings.enableNaturalLanguageSearch": false,
  "extensions.autoCheckUpdates": false,

  //Intelephense settings
  "intelephense.diagnostics.undefinedFunctions": false,
  "intelephense.diagnostics.unexpectedTokens": false,
  "intelephense.diagnostics.undefinedSymbols": false,
  "intelephense.diagnostics.undefinedMethods": false,

  // phpcs settings
  "phpcs.standard": "WordPress",
  "phpSniffer.autoDetect": true,
  "[php]": {
    "editor.defaultFormatter": "wongjn.php-sniffer"
  },

  // Theme
  "workbench.colorTheme": "Readable Code Material Darker",

  // Typescript & Experimental JavaScript options
  "js/ts.implicitProjectConfig.experimentalDecorators": true,
  "typescript.tsdk": "node_modules/typescript/lib",

  // Prevents VS Code from formatting JavaScript with the default linter
  "javascript.format.enable": false,

  // Lints with Standard JS
  "standard.enable": false,

  // Format files with Standard whenever you save the file
  "standard.autoFixOnSave": false,

  // Files to validate with Standard JS
  "standard.validate": [
    "javascript",
    "javascriptreact",
    // "typescript",
    // "typescriptreact",
    "html"
  ],
  "standard.options": {
    "plugins": ["html"]
  },
  "security.workspace.trust.untrustedFiles": "open",
  "redhat.telemetry.enabled": false,
  "window.zoomLevel": -1
}
```
