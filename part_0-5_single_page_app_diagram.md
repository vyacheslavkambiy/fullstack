# 0.5: Single page app diagram
```mermaid
graph TD
  subgraph User
    A[Open Browser]         %% User opens the web browser
    B[Enter SPA URL]        %% User enters the SPA URL
    C[SPA Loaded]           %% User sees the SPA loaded in the browser
  end

  subgraph Browser
    D[Request SPA Page]     %% Browser sends a request for the SPA page
    E[Load SPA Content]     %% Browser loads the content of the SPA
  end

  subgraph SPA Server
    F[Process SPA Request]  %% SPA server processes the request
    G[Retrieve SPA Content] %% SPA server retrieves SPA content
  end

  A -->|Open| B
  B -->|Navigate to| D
  D -->|Request| F
  F -->|Retrieve| G
  G -->|Load| E
  E -->|Display| C
```
