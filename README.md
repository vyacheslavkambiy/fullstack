# Excercise 0.4: New note diagram
```mermaid
# Excercise 0.4: New note diagram
```mermaid
graph TD
  subgraph User
    A[Enter Text]          %% User entering text into a text field
    B[Click Save]         %% User clicks the "Save" button
  end

  subgraph Browser
    C[Send Request]       %% The browser sends a request to the server
    D[Display Confirmation] %% The browser prepares to display a confirmation message
  end

  subgraph Server
    E[Process Request]    %% The server receives and processes the request
    F[Save Note]          %% The server saves the new note
  end

  A -->|User Input| C     %% User input is sent to the server
  B -->|Click| C          %% Click event triggers the request
  C -->|New Note Data| E  %% New note data is processed by the server
  E -->|Note Saved| F    %% The server saves the note
  F -->|Confirmation| D  %% The browser confirms the note has been saved
```

```
