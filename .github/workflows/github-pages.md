
```mermaid
flowchart TD
    A[build] -->  B(deploy)
    A[build] -->  C(report-build-status)
    C(report-build-status) <-->  B(deploy)
```