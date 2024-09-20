# yardang
[yardang](https://github.com/python-project-templates/yardang) documentation builder action.

## `.github/workflows/docs.yml`:

```yaml
name: Docs
on:
  push:
    branches: ["main"]
    tags: ["v*"]
    paths-ignore: ["LICENSE", "README.md"]

permissions:
    contents: write

jobs:
  docs:
    runs-on: ubuntu-latest
    steps:
      - uses: actions-ext/yardang@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```
