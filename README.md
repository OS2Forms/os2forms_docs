# OS2Forms

## Table of contents

* [Description](#description)
* [License](#license)
* [Testing and CI](#testing-and-ci)
* [Git guideline](#git-guideline)
* [Code review](#code-review)
* [Code of Conduct](#coc)
* [Links](#links)

<a name="description"></a>
## Description

__OS2Forms__ is a Drupal based solution for creating advanced webform functionality for Danish municipalities.

<a name="license"></a>
## License

All OS2Forms projects are using [EUPL v1.2 License](https://opensource.org/licenses/EUPL-1.2).

<a name="testing-and-ci"></a>
## Testing and CI

This project has continuous integration builds that are performed by [Travis CI](https://travis-ci.org). To improve code quality and integration possibilities it is using a set of following tools:

 * [PHP_CodeSniffer]() with [Drupal coding standards](https://www.drupal.org/docs/develop/standards/coding-standards) and best practices defined in [Coder module](https://www.drupal.org/project/coder).
 * [ESLint](https://eslint.org/) with [Drupal ESLint rules set](https://www.drupal.org/node/1955232).
 * [Stylelint](https://stylelint.io/) with rules set defined for Drupal core.
 * [Twigcs](https://github.com/friendsoftwig/twigcs) with standard set of rules for twig templates.
 * [Drupl-check](https://github.com/mglaman/drupal-check) to check project readiness to Drupal 9 via checking of deprecated code usage.
 * @TODO [PHPUnit](https://phpunit.de/) test to check key contrib modules tests.

For more details about travis-ci continuous integration builds see `.travis-ci.yml` file.

NOTE: The project doesn't have its own PHPUnit test. This is a part of the future development scope.

<a name="git-guideline"></a>
## Git guideline

Since OS2Forms is a Drupal module project, it uses drupal-friendly git branch/tag names.

### Branches

* `8.x` - general development branch.
* `8.x-2.x` - development branch for version 2.x.

There are no specific rules for feature branch names. However we recommend using [OS2Forms JIRA](https://os2web.atlassian.net/browse/OS2FORMS) or [github issue](https://github.com/OS2Forms/os2forms/issues) ticket number as prefix for your branch name.

### Tags

Release tags should be created from related branches. Examples for tags created from `8.x-2.x`:

* `8.x-2.0-alpha`, `8.x-2.0-alpha1`, `8.x-2.0-beta` - test release tags.
* `8.x-2.0-rc1`, `8.x-2.0-rc2` - release candidate tags.
* `8.x-2.0`, `8.x-2.1` - stable release tags.

<a name="code-review"></a>
## Code review

New changes or bugfixes in existing codebase have to be added to the repository through general [code review process](https://github.com/features/code-review/). To request a code review, use the following process:

1. Add Github pull request from the feature/bugfix branch to 8.x or other related dev branch.
2. Request code review from one of the project contributors.
3. Reviewer approves, requests changes or rejects pull request.
4. Discuss/Add requested changes or merge approved pull request.

NOTE: These are the preconditions that have to be met before a pull request is accepted:

- All requested changes have to be done.
- All discussions have to be resolved.
- The pull request should have green Travis CI build status.

<a name="coc"></a>
## Code of Conduct

See [Drupal community code of Conduct](https://www.drupal.org/dcoc).

<a name="links"></a>
## Links

* [Drupal code standards](https://www.drupal.org/docs/develop/standards).
