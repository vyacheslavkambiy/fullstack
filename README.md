# Excercise 0.4: New note diagram
```mermaid
graph TD
  subgraph User
    A[Enter Text]
    B[Click Save]
  end

  subgraph Browser
    C[Send Request]
    D[Display Confirmation]
  end

  subgraph Server
    E[Process Request]
    F[Save Note]
  end

  A -->|User Input| C
  B -->|Click| C
  C -->|New Note Data| E
  E -->|Note Saved| F
  F -->|Confirmation| D

```
