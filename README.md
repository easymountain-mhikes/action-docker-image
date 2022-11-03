# Docker image Action

Github Action to build and publish a Docker image to Amazon ECR.

## Usage

```bash
- name: Checkout repo
  uses: actions/checkout@v3

- name: Build artifact
  run: |
    some build commands...

- name: Build image and push to Amazon ECR
  uses: easymountain-mhikes/action-docker-image@v1
  with:
      aws-access-key-id: ${{ secrets.aws-access-key-id }}
      aws-secret-access-key: ${{ secrets.aws-secret-access-key }}
      repository: my-ecr-repo
      tag: ${{ github.sha }}
```