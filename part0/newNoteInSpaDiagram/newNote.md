Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.

```mermaid
  sequenceDiagram
    participant browser
    participant server 

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: the json file (Status code 201)
    deactivate server

    Note right of browser: This time the server does not ask for a redirect, the browser stays on the same page, and it sends no further HTTP requests.

    Note right of browser: The browser executes the callback function that renders the notes
```
