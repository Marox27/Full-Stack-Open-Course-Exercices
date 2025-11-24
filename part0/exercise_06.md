```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    note right of browser: Button "Save" pressed
    server-->>browser: HTTP CODE 201: CREATED
    deactivate server
    
    note right of browser: The SPA updates its internal state and renders the new note immediately without reloading the page.
```
