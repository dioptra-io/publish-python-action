# publish-python-action
Composite action to build and push a Python package to a repository.

## Usage

```yaml
name: PyPI
on:
  push:
    tags: [ 'v*' ]
jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: dioptra-io/publish-python-action@v1
        with:
          password: ${{ secrets.PYPI_TOKEN }}
```

### Inputs

Name          | Default
--------------|---------
`repository`  | `pypi`
`username`    | `__token__`
`password`    | None
