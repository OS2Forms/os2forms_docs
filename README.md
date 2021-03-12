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

__OS2Forms__ is a drupal based solution for creating advanced webform functionality for Danish Municipalities.

<a name="license"></a>
## License
All OS2forms projects are released under [MPL. 2.0](https://opensource.org/licenses/MPL-2.0) unless another license is issued in the repository or another license in underlying codebases state otherwise. Drupal for instanse is released on [GPL 2.0](https://opensource.org/licenses/GPL-2.0) and all software built on Drupal must be released on the same license.

<a name="testing-and-ci"></a>
## Testing and CI
Every OS2Forms drupal project should have continuous integration builds are performing by [Travis CI](https://travis-ci.org).
To improve code quality and integration possibilities there are using set of following tools:
 * [PHP_CodeSniffer]() with [Drupal coding standards](https://www.drupal.org/docs/develop/standards/coding-standards) and best practices defined in [Coder module](https://www.drupal.org/project/coder).
 * [ESLint](https://eslint.org/) with [Drupal ESLint rules set](https://www.drupal.org/node/1955232).
 * [Stylelint](https://stylelint.io/) with rules set defined for Drupal core.
 * [Twigcs](https://github.com/friendsoftwig/twigcs) with standard set of rules
  for twig templates.
 * [Drupal-check](https://github.com/mglaman/drupal-check) to check project
 readiness to Drupal 9 via checking of deprecated code usage.
 * @TODO [PHPUnit](https://phpunit.de/) test to check key contrib modules tests.

For more details about travis-ci continuous integration builds
see `.travis-ci.yml` file in project git repository.

NOTE: Some projects couldn't have its own PHPUnit test. This is a part of future
development scope.

<a name="git-guideline"></a>
## Git guideline
Project use default approach for branch naming.

### Bracnhes
* `develop` - general development branch (Default).
* `develop-2.x` - development branch for version 2.x. (if requires)
* `master` - stable version of code.

There are no specific rules for feature branch names. However we recommend
use [OS2Forms JIRA](https://os2web.atlassian.net/browse/OS2FORMS) or
[github issue](https://github.com/OS2Forms/os2forms/issues) ticket number
as prefix for your branch name.

### Tags
Release tags should be created from related branches. Tag name space should
 follow [Semantic Versioning](https://semver.org/) rules. 
Given a version number MAJOR.MINOR.PATCH, increment the:

* MAJOR version when you make incompatible API changes,
* MINOR version when you add functionality in a backwards compatible manner, and
* PATCH version when you make backwards compatible bug fixes.

#### Outdated approach
Since OS2Forms projects are Drupal friednly, there was used drupal-friendly
git branch/tag names like 8.x, 8.x-2.x. Please keep use it or ask about changes
in case this names are not compatible with changes you have.

For new repositories it was decided to switch back to github,
composer way to for branch names.

<a name="code-review"></a>
## Code review
New changes or bugfixes in existing codebase have to be added to repository
through general [code review process](https://github.com/features/code-review/).
To request a code review, use the following process:
1. Add Github pull request from the feature/bugfix branch to 8.x or other related dev branch.
2. Request code review from one of project contributor.
3. Reviewer approves, requests changes or rejects pull request.
4. Discuss/Add requested changes or merge approved pull request.

NOTE: There are preconditions that have to be met before accepting a pull request:
- All requested changes have to be done
- All discussion have to be resolved
- Pull request should have green Travis CI build status.

<a name="coc"></a>
## Code of Conduct
See [Drupal community code of Conduct](https://www.drupal.org/dcoc)

<a name="links"></a>
## Links
* [Drupal code standards](https://www.drupal.org/docs/develop/standards)
