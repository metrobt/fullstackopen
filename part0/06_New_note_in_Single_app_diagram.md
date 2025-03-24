sequenceDiagram
    Note right of Browser: Form button pushed
    Note right of Browser: Browser executes the event handler that creates a new note, rerenders the note list with it, then sends the new note to the Server
    Browser->>+Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server-->>-Browser: HTTP Created (201)