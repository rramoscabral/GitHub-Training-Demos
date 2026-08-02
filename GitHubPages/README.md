# GitHub Pages Demo

How to publish a static website using GitHub Pages and GitHub Actions.

## Demo Workflow

```mermaid
flowchart TD

    build([build])
    report([report-build-status])
    deploy([deploy])

    build --> report
    build --> deploy
    report --> deploy
```