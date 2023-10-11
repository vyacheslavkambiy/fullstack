# 0.6: New note in the SPA page diagram
```mermaid
graph TD
  subgraph User
    A[Open Browser]         %% User opens the web browser
    B[Enter SPA URL]        %% User enters the SPA URL
    C[SPA Loaded]           %% User sees the SPA loaded in the browser
    D[Click New Note]       %% User clicks the "New Note" button
    E[Enter Note Content]   %% User enters the note content
    F[Click Save]           %% User clicks the "Save" button
  end

  subgraph Browser
    G[Request SPA Page]     %% Browser sends a request for the SPA page
    H[Load SPA Content]     %% Browser loads the content of the SPA
    I[Send Create Note]     %% Browser sends a request to create the note
    J[Display Confirmation] %% Browser displays a confirmation message
  end

  subgraph SPA Server
    K[Process SPA Request]  %% SPA server processes the request
    L[Retrieve SPA Content] %% SPA server retrieves SPA content
    M[Create Note]          %% SPA server creates a new note
  end

  A -->|Open| B
  B -->|Navigate to| G
  G -->|Request| K
  K -->|Retrieve| L
  L -->|Load| H
  H -->|Display| C
  C -->|Click New Note| D
  D -->|Create Note| I
  I -->|Note Data| M
  M -->|Confirmation| J
  D -->|Enter Note Content| E
  E -->|Save| F
  F -->|Confirmation| J

```
