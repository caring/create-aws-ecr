# create-aws-ecr-repository

This GitHub Action creates an Amazon ECR repository

## Usage

```yaml

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Create ECR repository
        uses: caring/create-aws-ecr-repository@v1
        with:
          name: <repository-name>
```

## Inputs

- `name` (required): The name of the repository. If not provided, the default value is set to the name of the current GitHub repository.

## Example

```yaml

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Create ECR repository
        uses: caring/create-aws-ecr-repository@v1.0.1
        with:
          name: my-repository
```

This example workflow checks out the repository and creates an Amazon ECR repository named "my-repository" using the `create-aws-ecr-repository` action.

## License

This project is licensed under the [MIT License](LICENSE).

## Author

Written by the Devops Team.