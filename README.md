# a simpel git hook for adding sub .md to main readme

To be used with [pre-commit framework](http://pre-commit.com/)


## How to install

### Install dependencies

* [`pre-commit`](https://pre-commit.com/#install)

### Add configs and hooks

Step into the repository you want to have the pre-commit hooks installed and run:

```bash
git init
cat <<EOF > .pre-commit-config.yaml
- repo: git://github.com/zamaterian/pre-commit-readme-link
  rev: <VERSION> # should be a sha
  hooks:
    - id: readme-submodule
EOF
```

###  Run

After pre-commit hook has been installed you can run it manually on all files in the repository

```bash
pre-commit run -a
```


Check the [source file](https://github.com/zamaterian/pre-commit-readme-link/blob/master/.pre-commit-hooks.yaml) to know arguments used for each hook.

### Configuration

```
<!-- BEGINNING OF PRE-COMMIT-README DOCS HOOK -->

<!-- END OF PRE-COMMIT-README DOCS HOOK -->
```
if they are present in `README.md`. The links to sub readme will be added here.


## CREDIT

This repository is based upon work by [Anton Babenko](https://github.com/antonbabenko)
## License

MIT licensed. See LICENSE for full details.
