# YML Intellisense in VS Code

- VS Code extension
  - https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml
- JSON Schema Store
  - https://www.schemastore.org/json/
- A few different ways to use

  - User or workspace setting
    ```json
    "yaml.schemas": {
      "https://json.schemastore.org/github-action.json": ["action.yml"]
    }
    ```
  - Tag in file ("modeline")
    ```yml
    # yaml-language-server: $schema=https://json.schemastore.org/github-action.json
    ```
  - Well-known filename
    - Use a filename found in https://www.schemastore.org/api/json/catalog.json
