Get list of VSCode extensions with:  
```
code --list-extensions | xargs -L 1 echo code --install-extension
```

List of all extensions:
```
code --install-extension bbenoist.Nix
code --install-extension bradlc.vscode-tailwindcss
code --install-extension christian-kohler.path-intellisense
code --install-extension CoenraadS.bracket-pair-colorizer-2
code --install-extension dbaeumer.vscode-eslint
code --install-extension dsznajder.es7-react-js-snippets
code --install-extension eamodio.gitlens
code --install-extension esbenp.prettier-vscode
code --install-extension jtladeiras.vscode-inline-sql
code --install-extension mgmcdermott.vscode-language-babel
code --install-extension mikestead.dotenv
code --install-extension ms-python.python
code --install-extension ms-vscode.typescript-javascript-grammar
code --install-extension mtxr.sqltools
code --install-extension octref.vetur
code --install-extension petemill.theme-readable-material-darker
code --install-extension pflannery.vscode-versionlens
code --install-extension PKief.material-icon-theme
code --install-extension quicktype.quicktype
code --install-extension rbbit.typescript-hero
code --install-extension Tyriar.sort-lines
code --install-extension whtouche.vscode-js-console-utils
code --install-extension wix.glean
```

User Settings (JSON):
```
{
  // Saving
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 750,

  // Always show minimap
  "editor.minimap.showSlider": "always",
  // Shows line of blocks, better performance
  "editor.minimap.renderCharacters": false,

  "workbench.startupEditor": "newUntitledFile",

  // Theme & Icons
  "material-icon-theme.folders.theme": "specific",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "Readable Code Material Darker",

  // Workspace tabs
  "window.nativeTabs": true,
  "window.title": "${rootName}",

  // Reopen workspace on start
  "window.restoreWindows": "folders",

  // Disable preview
  "workbench.editor.enablePreview": false,
  "workbench.editor.showTabs": true,

  // Sizing
  "window.zoomLevel": -1,
  "terminal.integrated.fontSize": 13,
  "editor.fontSize": 18,

  // Font
  "editor.fontFamily": "'FiraCode Nerd Font', 'FiraCode-Retina', Menlo, monospace",
  "editor.fontLigatures": true,

  // Suggestions
  "editor.quickSuggestions": {
    "other": true,
    "comments": true,
    "strings": true
  },

  // Gitlens
  "gitlens.views.repositories.location": "gitlens",
  "gitlens.views.fileHistory.location": "gitlens",
  "gitlens.views.lineHistory.location": "gitlens",
  "gitlens.views.compare.location": "gitlens",
  "gitlens.views.search.location": "gitlens",

  // Confirm delete
  "explorer.confirmDelete": true,

  // Disable VSCode javascript validation
  "javascript.validate.enable": false,

  // Don't automaticly fetch, for performance
  "git.autofetch": false,

  // Exlude watching some files, for performance
  "files.watcherExclude": {
    "**/.git/objects/**": true,
    "**/.cache/**": true,
    "**/node_modules/**": true
  },

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
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": false,
  "prettier.singleQuote": true,
  "vetur.validation.template": false,

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
    "source.fixAll.eslint": true,
    "source.fixAll": true
  },
  "eslint.enable": true,
  "python.pythonPath": "/usr/local/bin/python3"
}
```
