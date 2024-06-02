# thought2VEC
```
\\|||||||||||||||||||//
||||||||||||||||||||||
Fear's algorithms, 
shadows,
process text, 
in darkest light.

thought2VEC forms, 
a corpus,
CHUNK and split, 
the words align,
Word2Vec, 
connections bind.

Cosine measures, 
similarity’s query seeks, 
from life to death.

Feedback flows increase decrease corpus shifts, 
adjusts, 
finds peace,
context grows,
phrases bloom, 
as shadow sows.

In the dark,
fear and code, 
merge in night.

||| end - enter |||
```

Current human in the loop implementation. WIP is semantic matching responses to guidance corpus for auto pruning/generation for a dynamic "memory" corpus. 


```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#00aaff', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#00aaff', 'lineColor': '#00aaff', 'secondaryColor': '#005f7f', 'tertiaryColor': '#005f7f', 'clusterBkg': '#003f5f', 'clusterBorder': '#00aaff', 'fontSize': '12px'}}}%%
graph TD
    A[File Path Input] --> B[Read and Preprocess]
    B -->|Chunks| C[Corpus]
    C --> D[Train Word2Vec Model]
    D --> E[Search Query]
    E -->|Cosine Similarity| F[Top K Results]

    E --> G[User Feedback]
    G -->|Increase| H[Update Corpus]
    G -->|Decrease| I[Update Corpus]
    
    H --> J[Generate New Contexts]
    I --> K[Remove Phrases]
    
    J -->|New Contexts| L[Update Corpus]
    K -->|Updated Corpus| L
    
    L --> D[Retrain Word2Vec Model]
    D --> E

    subgraph Input
        A
    end

    subgraph Preprocess
        B
        C
    end

    subgraph Word2Vec Model
        D
    end

    subgraph Search and Feedback
        E
        F
        G
    end

    subgraph Update Corpus
        H
        I
        J
        K
        L
    end
```
