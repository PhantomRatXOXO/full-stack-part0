```mermaid

sequenceDiagram
    participant browser
    participant server

    Note rigth of browser: java script prevents default behavior

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa (data as JSON string)
    activate server
    server-->>browser: Status Code 201
    deactivate server

    Note right of browser: java script calls redrawNotes(), does not realod page


```
