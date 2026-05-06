sequenceDiagram
  ```mermaid
  participant browser
  participant server

  Note right of browser:User writes a note and clicks save

  browser->>server POST /newnote https://studies.cs.helsinki.fi/exampleapp/new_note
  Note left of server: Note stored on server

  server->>browser: HTTP redirects to /notes

  browser->>server GET https://studies.cs.helsinki.fi/exampleapp/notes

  
