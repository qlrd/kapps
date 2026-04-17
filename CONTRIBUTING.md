# Contributing to kapps

Thank you for your interest in contributing to kapps! This project builds signed applications for [Krux](https://github.com/selfcustody/krux) devices.

## Getting started

1. Fork the repository
2. Clone your fork with submodules: `git clone --recursive <your-fork-url>`
3. Install dependencies: `uv sync`
4. Install pre-commit hooks: `uv run pre-commit install --install-hooks`

## How to contribute

### Reporting bugs

- Open an [issue](https://github.com/selfcustody/kapps/issues/new?template=bug_report.md) with the bug report template
- Be specific about the steps to reproduce
- Include device model and firmware version

### Requesting features

- Open an [issue](https://github.com/selfcustody/kapps/issues/new?template=enhancement.md) with the enhancement template
- Describe the use case and expected behavior

### Submitting pull requests

1. Start a discussion or issue before working on large changes
2. Branch off `main`
3. Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages:
   - `feat:` new feature
   - `fix:` bug fix
   - `docs:` documentation
   - `test:` tests
   - `build:` build system
   - `ci:` CI/CD
   - `refactor:` code refactoring
   - `style:` formatting
   - `chore:` maintenance
   - `i18n:` translations
4. Each PR should focus on solving one issue
5. Ensure all pre-commit hooks pass before submitting
6. Explain what the PR solves and why

### Changes checklist

- [ ] Code changes include tests
- [ ] Pre-commit hooks pass (`uv run pre-commit run --all-files`)
- [ ] Commit messages follow conventional commits

## Code style

- **Formatting**: [black](https://github.com/psf/black) (enforced by pre-commit)
- **Import sorting**: [isort](https://pycqa.github.io/isort/) with black profile
- **Linting**: [pylint](https://pylint.org/) (errors-only in pre-commit)
- **Dead code**: [vulture](https://github.com/jendrikseipp/vulture)
- **Spell checking**: [typos](https://github.com/crate-ci/typos)

## Writing a kapp

A kapp is a Python module in `src/` that runs on Krux devices. Kapps can use the full `krux` API (display, input, settings, pages, themes, etc.).

Each kapp should:

1. Have a corresponding test in `tests/kapps/`
2. Follow the existing code style
3. Import from `krux` for device interaction

## Questions?

Open a [discussion](https://github.com/selfcustody/kapps/discussions) or reach the community via the [Krux Telegram group](https://t.me/kraboratory).
