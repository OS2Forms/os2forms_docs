# OS2Forms

## Table of contents

* [Description](#description)
* [License](#license)
* [Testing and CI](#testing-and-ci)
* [Git guideline](#git-guideline)
* [Code review](#code-review)
* [Patching principles](#patching-principles)
* [Code of Conduct](#coc)
* [Links](#links)

<a name="description"></a>
## Description

__OS2Forms__ is a drupal based solution for creating advanced webform functionality for Danish Municipalities.

Solution main repositories:
* Drupal core incl. installatioj profile: https://github.com/OS2Forms/os2forms8
* OS2Forms forløb profile: https://github.com/OS2Forms/os2forms_forloeb_profile
* OS2Forms main Drupal module https://github.com/OS2Forms/os2forms

<a name="license"></a>
## License
All OS2Forms projects are using [EUPL v1.2 License](https://opensource.org/licenses/EUPL-1.2).

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
Since OS2Forms projects are Drupal friendly, there was used drupal-friendly
git branch/tag names like 8.x, 8.x-2.x. Please keep use it or ask about changes
in case this names are not compatible with changes you have.

For new repositories it was decided to switch back to github,
composer way to for branch names.

<a name="code-review"></a>
## Code review proces
New changes or bugfixes in existing codebase have to be added to repository
through general [code review process](https://github.com/features/code-review/).
To request a code review, use the following process:
1. Add Github pull request from the feature/bugfix branch to 8.x or other related dev branch.
2. Request code review from internal department
3. Test features with customer on test setting
4. Fix bugs or get approval from customer
5. Request code review from one of project contributor (other department/company).
6. Reviewer approves, requests changes or rejects pull request.
7. Discuss/Add requested changes or merge approved pull request.

NOTE: There are preconditions that have to be met before accepting a pull request:
- All requested changes have to be done
- All discussion have to be resolved
- Pull request should have green Travis CI build status.

##Code review tasks
Giving codereview to other developers code should cover
1.	The use of [Code of conduct](docs#coc)
2.  The following of the [Testing standards](docs#testing-and-ci)
3.	That kode is handling successes and errors, can not end in loops and other logical 
4.	Other questions the developers might see. 

<a name="patching-principles"></a>
## Patching principles
To patch a drupal composer project see:
https://www.drupal.org/docs/develop/git/using-git-to-contribute-to-drupal/working-with-patches/applying-a-patch-in-a-feature-branch#s-composer

- Composer based projects in os2forms should always use [cweagans/composer-patches](https://github.com/cweagans/composer-patches) package to patch extensions.
- To allow patching of project dependencies add "enable-patching" to your composer file configuration:
```
  "extra": {
      "enable-patching": true
  }
```
- Patching should only be used for drupal contributed modules, drupal core and other packages maintained outside os2forms organisation.
- Patching should be handled by the os2forms project that introduces the externally maintained code.
- Patches should include a link reference to the issue it addresses, if any exist.
- If an external package(1) introduces another external package(2) the patch should be handled by the project that introduced package 1.

Example:

Given the following dependency tree:
```
composer why drupal/dynamic_entity_reference -r

drupal/recommended-project        -                    requires os2forms/os2forms_forloeb_profile (dev-composer_cleanup)  
drupal/recommended-project        -                    requires os2forms/os2forms_forloeb (dev-composer_cleanup as 2.5.0) 
os2forms/os2forms_forloeb_profile dev-composer_cleanup requires os2forms/os2forms_forloeb (^2.5)                          
os2forms/os2forms_forloeb         dev-composer_cleanup requires drupal/workflow_participants (^2.4)                       
drupal/workflow_participants      2.6.0                requires drupal/dynamic_entity_reference (^2.0) 
```
...the os2forms/os2forms_forloeb project is responsible for patching drupal/dynamic_entity_reference contributed module.
Leave a comment about why the patch belongs here.
```
"patches": {
  "//": "Note: drupal/dynamic_entity_reference is required by drupal/workflow_participants",
  "drupal/dynamic_entity_reference": {
    "entityQuery reference JOINs should specify target_type (https://www.drupal.org/project/dynamic_entity_reference/issues/3120952#comment-14141038)": "https://www.drupal.org/files/issues/2021-06-22/entityquery-reference-joins-should-specify-target_type-3120952-24.patch"
  }
```


<a name="coc"></a>
## Code of Conduct
See [Drupal community code of Conduct](https://www.drupal.org/dcoc)

<a name="links"></a>
## Links
* [Drupal code standards](https://www.drupal.org/docs/develop/standards)
