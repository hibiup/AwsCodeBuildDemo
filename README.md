Create `buildspec.yml` with content:

```yaml
version: 0.2

phases:
  install:
    runtime-versions:
      nodejs: latest
    commands:
      - echo "Installing..."

  pre_build:
    commands:
      - echo "Pre-build phase..."
  
  build:
    commands:
      - echo "Building phase..."
      - echo "Testing phase..."
      - grep -Fq "Hello World!" index.js

  post_build:
    commands:
      - echo "Building is finished."
```
