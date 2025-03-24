sequenceDiagram
    Note right of Browser: Form button pushed
    Browser->>+Server: POST https://fullstack-exampleapp.herokuapp.com/new_note
    Note left of Server: Server adds new note to the notes JSON array
    
    Server-->>-Browser: HTTP Redirect (302)

    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server-->>-Browser: HTML document

    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server-->>-Browser: CSS file

    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server-->>-Browser: JavaScript file
    Note right of Browser: Browser executes the JavaScript code that fetches the JSON from the Server
    
    Browser->>+Server: GET https://studies.cs.helsinki.fi/exampleapp/data.js
    Server-->>-Browser: notes JSON array
    Note right of Browser: Browser executes the callback function that renders the notes












