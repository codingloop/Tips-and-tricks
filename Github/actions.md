## Setup github action depending on another github action
1. Create github action which needs to run first
```
name: Run tests

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest
    
    steps:
    - setup: ...
```
2. Create second action which will run only when first github action is successfull
```
name: Deploy App

on:
  workflow_run:
    workflows: ["Run tests"]
    types:
      - completed

jobs:
  deploy:
    runs-on: ....
```
