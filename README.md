# click-app-copier-template-demo

[![PyPI](https://img.shields.io/pypi/v/click-app-copier-template-demo.svg)](https://pypi.org/project/click-app-copier-template-demo/)
[![Changelog](https://img.shields.io/github/v/release/kj-9/click-app-copier-template-demo?include_prereleases&label=changelog)](https://github.com/kj-9/click-app-copier-template-demo/releases)
[![Tests](https://github.com/kj-9/click-app-copier-template-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/kj-9/click-app-copier-template-demo/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/kj-9/click-app-copier-template-demo/blob/master/LICENSE)

Demonstrating https://github.com/kj-9/click-app-copier

## Installation

Install this tool using `pip`:
```bash
pip install click-app-copier-template-demo
```
## Usage

For help, run:
<!-- [[[cog
import cog
from click_app_copier_template_demo import cli
from click.testing import CliRunner
runner = CliRunner()
result = runner.invoke(cli.cli, ["--help"])
help = result.output.replace("Usage: cli", "Usage: click-app-copier-template-demo")
cog.out(
    f"```bash\n{help}\n```"
)
]]] -->
```bash
Usage: click-app-copier-template-demo [OPTIONS] COMMAND [ARGS]...

  Demonstrating https://github.com/kj-9/click-app-copier

Options:
  --version  Show the version and exit.
  --help     Show this message and exit.

Commands:
  command  Command description goes here

```
<!-- [[[end]]] -->

You can also use:
```bash
python -m click_app_copier_template_demo --help
```
## Development

To contribute to this tool, first checkout the code. Then create a new virtual environment:
```bash
cd click-app-copier-template-demo
python -m venv venv
source venv/bin/activate
```
Now install the dependencies and test dependencies:
```bash
make install-e
```
To run the tests:
```bash
make test
```

To run pre-commit to lint and format:
```bash
make check
```

`make check` detects if cli help message in `README.md` is outdated and updates it.

To update cli help message `README.md`:
```bash
make readme
```

this runs [cog](https://cog.readthedocs.io/en/latest/) on README.md and updates the help message inside it.
