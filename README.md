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

Solution main repositories:
* OS2Forms main module https://github.com/OS2Forms/os2forms
* OS2Forms forløb main module https://github.com/OS2Forms/os2forms_forloeb
* OS2Forms forløb profile: https://github.com/OS2Forms/os2forms_forloeb_profile

<a name="license"></a>
## License
All OS2Forms projects are using [EUPL v1.2 License](https://opensource.org/licenses/EUPL-1.2).

<a name="testing-and-ci"></a>
## Testing and CI
Every OS2Forms drupal project should have CI build performed by [Github actions](). Your project might have different sets of implmented checks.
To improve code quality and integration possibilities there are recommended to use following tools:
 * [PHP_CodeSniffer]() with [Drupal coding standards](https://www.drupal.org/docs/develop/standards/coding-standards) and best practices defined in [Coder module](https://www.drupal.org/project/coder).
 * [ESLint](https://eslint.org/) with [Drupal ESLint rules set](https://www.drupal.org/node/1955232).
 * [Stylelint](https://stylelint.io/) with rules set defined for Drupal core.
 * [Twigcs](https://github.com/friendsoftwig/twigcs) with standard set of rules
  for twig templates.
 * [Drupal-check](https://github.com/mglaman/drupal-check) to check project
 readiness to Drupal 9 via checking of deprecated code usage. (ONLY FOR FULL INSTALLATIONS)

For more details about github-action builds see:
* YAML files in `.github/workflows` directory of specidif git repository,
* `Actions` tab in github repository.

<a name="git-guideline"></a>
## Git guideline
For all projects and git repositories there is used default approach with git branching. 

If you are in doubt on "What branch you should use?" or "How to create it?" See [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) tutorial from Atlassian.

### Bracnhes
* `develop` - general development branch (Default).
* `master` or `main` - stable version of code.

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

<a name="code-review"></a>
## Code review
New features of hotfixes existing codebase have to be added to repository
through general [code review process](https://github.com/features/code-review/).
To request a code review, use the following process:
1. Add Github pull request from the new branch to base branch accordingly with [gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).2. Request code review from internal department
3. Test features with customer on test setting
4. Fix bugs or get approval from customer
5. Request code review from one of project contributor (other department/company).
6. Reviewer approves, requests changes or rejects pull request.
7. Discuss/Add requested changes or merge approved pull request.

NOTE: There are preconditions that have to be met before accepting a pull request:
- All requested changes have to be done
- All discussion have to be resolved
- Pull request should have green CI build status.

<a name="coc"></a>
## Code of Conduct
See [Drupal community code of Conduct](https://www.drupal.org/dcoc)

<a name="links"></a>
## Links
* [Drupal code standards](https://www.drupal.org/docs/develop/standards)
