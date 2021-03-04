# How to contribute

Firstly thanks for thinking of contributing - the project is [open source](https://opensource.guide/how-to-contribute/)
and all contributions are very welcome :slightly_smiling_face: :boom: :thumbsup:

## Local development

### VS Code

The preferred development environment is on a [Visual Studio Code](https://code.visualstudio.com/) [Remote Container](https://code.visualstudio.com/docs/remote/containers)
(as this comes fully loaded with the right software and code linters etc).

* [System requirements](https://code.visualstudio.com/docs/remote/containers#_system-requirements)
  * [Visual Studio Code](https://code.visualstudio.com/)
  * [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [Fork the project](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/working-with-forks)
* [Open the forked repo (or a specific branch or pull request) in a VS Code container](https://code.visualstudio.com/docs/remote/containers#_quick-start-open-a-git-repository-or-github-pr-in-an-isolated-container-volume)

  The remote VS Code container will start with all the software you need installed and configured correctly.

### Tools and technologies

* [Gauge](https://gauge.org)
* [Python](https://www.python.org/)
  * [Black](https://github.com/psf/black) for Python formatting
  * [Flake8](https://flake8.pycqa.org/) for Python style checks
* [GitHub Actions](https://docs.github.com/en/actions) for CI

### Environment configuration

You will need to set up some Gauge properties:

1. Create the following file: `env/default/secrets.properties`
2. Populate the file with:

   ```lang-default
   JIRA_BASE_URL =
   JIRA_ADMIN_USERNAME =
   JIRA_ADMIN_PASSWORD =
   INTERNAL_EMPLOYEE_USERNAME =
   INTERNAL_EMPLOYEE_PASSWORD =
   ```

3. Ask [a maintainer](.github/CODEOWNERS) for the values for the above configuration properties and populate them in
   the file you just created.

### Running the specs

`gauge run --tags \!in-progress`

## How to make a contribution

* [Create a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests).
The project uses the _[fork and pull model](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-collaborative-development-models)_:
  * [Fork the project](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/working-with-forks)
  * Make your changes on your fork
  * Write a [good commit message(s)](https://chris.beams.io/posts/git-commit/) for your changes
  * [Create the pull request for your changes](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests)

## Updating dependencies

See the [DEPENDENCIES.md](.github/DEPENDENCIES.md)
