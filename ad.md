## Architecture

```mermaid
flowchart LR
    U[User Upload] --> V[Validation & Schema Checks<br/>(Python)]
    V --> T[Cleaning & Transformation <br/>(Pandas)]
    T --> S3R[(AWS S3<br/>Raw Data)]
    T --> S3P[(AWS S3<br/>Processed Data)]
    S3P --> G[AWS Glue<br/>Batch Jobs]
    G --> S3P
```

This diagram shows the end-to-end flow from file upload through validation, transformation, and scalable batch processing, highlighting clear separation between ingestion, processing, and storage.
