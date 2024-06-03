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
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffaa00', 'primaryTextColor': '#000000', 'primaryBorderColor': '#ffaa00', 'lineColor': '#ffaa00', 'secondaryColor': '#ffaa00', 'tertiaryColor': '#ffaa00', 'clusterBkg': 'none', 'clusterBorder': 'none', 'fontSize': '20px'}}}%%
graph TD
    style Input fill:none,stroke:none
    style Preprocess fill:none,stroke:none
    style Word2Vec fill:none,stroke:none
    style SearchAndFeedback fill:none,stroke:none
    style UpdateCorpus fill:none,stroke:none
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
