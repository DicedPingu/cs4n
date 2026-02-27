# pip — Python package installer & dependency manager

Use pip to install, upgrade, list, remove Python packages from PyPI or other sources. This guide expands on pip’s core workflows and groups commands by common task. It is structured so you can quickly find how to check state, install packages, manage requirements files, work offline, and troubleshoot issues.

---

## Syntax & safety
- `<package>` = the name of the package (e.g., `requests`)
- `<version>` = version spec (e.g., `==2.31.0` or `~=2.0`)
- `[options]` = optional flags; many commands support `-h/--help` for details
- `pip` commands run in the current environment; to avoid polluting system Python, run inside a virtual environment (`python -m venv .venv && source .venv/bin/activate` or use `uv run`)

---

## 0) Inspecting your pip environment

| Command | Purpose |
| --- | --- |
| `pip --version` | show pip and Python versions used |
| `pip list` | list installed packages in current environment |
| `pip list --outdated` | list packages with newer versions available |
| `pip show <package>` | display metadata for installed package |
| `pip help` | list top-level pip commands |
| `pip cache dir` | show pip’s cache directory |
| `pip debug` | show environment and configuration information |
| `python -m pip list` | explicit invocation via Python (useful when multiple pip versions are installed) |

---

## 1) Installing packages

### Basic installs

| Command | Description |
| --- | --- |
| `pip install <package>` | install a package from PyPI |
| `pip install <package>==<version>` | install a specific version |
| `pip install '<package><version-spec>'` | install with version specifier (e.g., `<2.0`) |
| `pip install --upgrade <package>` | upgrade an already-installed package |
| `pip install --force-reinstall <package>` | reinstall even if version is present |
| `pip install --pre <package>` | allow pre-release versions |
| `pip install --user <package>` | install into user-site (`~/.local`) instead of system |
| `pip install <url>` | install from URL (git+https, wheel, tar.gz, etc.) |
| `pip install -r requirements.txt` | install all requirements listed in file |

### Dependency groups / extras

| Command | Description |
| --- | --- |
| `pip install <package>[dev]` | install an extra group defined by the package (like dev/test extras) |
| `pip install -e .` | install current project in editable (development) mode |
| `pip install .` | install current project as a package |
| `pip install -c constraints.txt -r requirements.txt` | apply constraint file when installing requirements |
| `pip install --target path/to/dir <package>` | install into custom directory instead of site-packages |

### Performance & caching

| Command | Description |
| --- | --- |
| `pip install --no-cache-dir <package>` | don’t use or store HTTP cache |
| `pip install --no-binary :all: <package>` | force source install; avoid wheels |
| `pip install --only-binary :all: <package>` | install only from binary wheels |
| `pip install --no-deps <package>` | skip installing dependencies (advanced) |
| `pip install --progress-bar off <package>` | disable progress bar (useful in CI logs) |
| `pip install --quiet <package>` | reduce output verbosity |
| `pip install --verbose <package>` | increase output detail (debugging) |

---

## 2) Removing, freezing, and listing

| Command | Description |
| --- | --- |
| `pip uninstall <package>` | remove a package interactively |
| `pip uninstall -y <package>` | remove without confirmation |
| `pip freeze` | output installed packages in `pkg==ver` format |
| `pip freeze > requirements.txt` | write current env to requirements file |
| `pip check` | verify installed packages have compatible dependencies |
| `pip list --format=freeze` | show freeze-style list (similar to `pip freeze`) |
| `pip list --not-required` | list packages that are not dependencies of others |
| `pip list --format=columns` | pretty printed columns (default) |

---

## 3) Working with requirement files & constraints

| Command | Description |
| --- | --- |
| `pip install -r requirements.txt` | install packages specified in file |
| `pip install -r requirements-dev.txt` | install a separate dev requirements file |
| `pip install -r <(sed 's/#.*//' requirements.txt)` | skip comments (bash process substitution) |
| `pip install -c constraints.txt -r requirements.txt` | apply constraints while installing |
| `pip install --require-hashes -r requirements.txt` | enforce `sha256` hashes for reproducible installs |
| `pip download -r requirements.txt -d wheels/` | download wheels for offline installation |
| `pip wheel -r requirements.txt -w wheels/` | build wheels into local directory |
| `pip compile requirements.in -o requirements.txt` | use pip-tools to compile pin file (external) |
| `pip install --dry-run -r requirements.txt` | show what would be installed without doing it |

---

## 4) Indexes and mirrors

| Command | Description |
| --- | --- |
| `pip install --index-url https://pypi.org/simple <package>` | specify base index (default) |
| `pip install --extra-index-url https://example.com/simple <package>` | add additional index |
| `pip install --no-index -f ./wheels <package>` | install only from local wheels dir |
| `pip search <term>` | search PyPI (deprecated, may need `pip search --index`) |
| `pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org <package>` | trust hosts for HTTP (when disabling HTTPS) |

---

## 5) Configuration & environment

| Command | Description |
| --- | --- |
| `pip config list` | list global and local pip config settings |
| `pip config edit` | open pip config file in $EDITOR |
| `pip config get global.index-url` | show configured index |
| `pip config set global.index-url https://mirror.example.com/simple` | set global index |
| `pip config unset global.index-url` | remove config setting |
| `python -m site --user-site` | show user site-packages path |
| `pip install --break-system-packages <package>` | allow install into externally managed environments (pip 23.2+) |

---

## 6) Upgrading pip & packaging tools

| Command | Description |
| --- | --- |
| `python -m pip install --upgrade pip` | upgrade pip itself |
| `python -m pip install --upgrade setuptools wheel` | upgrade build tools |
| `python -m ensurepip` | bootstrap pip into a virtual environment |
| `python -m pip uninstall pip` | remove pip (not recommended) |
| `pip install pipx` | install pipx for isolated CLI tool management |
| `pipx run <tool>` | run a tool in an isolated environment (via pipx) |

---

## 7) Debugging & troubleshooting

| Command | Purpose |
| --- | --- |
| `pip install --verbose <package>` | show detailed build logs |
| `pip cache purge` | clear pip’s HTTP and wheel caches |
| `pip install --retries 5 --timeout 60 <package>` | control network retries and timeout |
| `pip install --use-pep517 <package>` | force using PEP 517 build system |
| `pip download <package> -d tmp/` | download package for manual inspection |
| `pip wheel <package> -w dist/` | build a wheel (useful for debugging compile failures) |
| `pip install --no-build-isolation <package>` | use system environment for build (can solve issues when dependencies are missing) |
| `pip install --report report.json <package>` | produce JSON installation report (pip ≥ 22.1) |
| `PIP_PROGRESS_BAR=off pip install <package>` | disable progress bar via env var |

---

## 8) Miscellaneous & lesser-known commands

| Command | Description |
| --- | --- |
| `pip search --limit 10 'search term'` | search PyPI for packages matching term (requires opt-in) |
| `pip check --quiet` | check dependency conflicts without verbose output |
| `pip show -f <package>` | list files installed by package |
| `pip cache info` | show cache statistics |
| `pip cache remove <package>` | remove package from cache |
| `pip download --no-binary :all: <package>` | force source download only |
| `pip uninstall -y -r requirements.txt` | uninstall all packages listed in file |
| `pip completion --bash` | generate shell completion script |
| `pip help <command>` | show help for subcommand |
| `pip install --upgrade-strategy eager <package>` | upgrade dependencies even if not required |
| `pip install --upgrade-strategy only-if-needed <package>` | (default) only upgrade if necessary |
| `pip install --root /usr/local/tmp/env <package>` | install into given root prefix |

---

## Version & resources

- Check pip docs: https://pip.pypa.io/en/stable/ (always refer to your installed pip’s help for accurate options)
