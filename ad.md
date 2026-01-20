## Architecture

```mermaid
flowchart LR
    U[User Upload] --> V[Validation and Schema Checks (Python)]
    V --> T[Cleaning and Transformation (Pandas)]
    T --> S3R[(AWS S3 Raw Data)]
    T --> S3P[(AWS S3 Processed Data)]
    S3P --> G[AWS Glue Batch Jobs]
    G --> S3P
```

This simplified diagram shows the end-to-end flow from file upload through validation, transformation, and scalable batch processing, optimized for GitHub README rendering.
