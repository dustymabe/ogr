# 0.6.0


## New Features

* Possibility to authenticate via github-app. (@lachmanfrantisek)
* New method `get_latest_release()` for projects. (@marusinm)
* New method for creating releases in GitHub. (@lbarcziova)
* Add method for getting releases for Pagure. (@lbarcziova)
* Add labels for GitHub pull-requests. (@marusinm)
* New methods for getting pull-request/issue permissions (`who_can_marge_pr`, `who_can_close_issue`, `can_close_issue` and `can_merge_pr`).  (@marusinm)
* New methods to get project's owners and permissions of various users.  (@marusinm)
* Link GitTag to Release object. (@lbarcziova)
* Add method for creating projects/services from url. (@lachmanfrantisek)
* Creating/closing/commenting Pagure Issues. (@marusinm)

## Fixes

* Correct status handling for Github pull-requests. (@marusinm)
* Fix error 404 on `get_file_content`. (@lbarcziova)

## Minor

* Simplify usage of persistent storage and mocking. (@lachmanfrantisek)
* CommitStatus renamed to CommitFlag. (@lbarcziova)
* Add zuul as a CI system. (@TomasTomecek)
* Removed unused functions. (@lbarcziova)
* Unify external command invocation by subprocess.run. (@lbarcziova)
* Add `__str__ ` and `__eq__` for classes. (@shreyanshrs44, @lachmanfrantisek)


# 0.5.0

## New Features

* Add support for Github issues. (@marusinm)
* New methods for updating pull-requests. (@lbarcziova)
* New methods for getting forks for user/project. (@lachmanfrantisek)

## Fixes

* Better support for forks and forking. (@lachmanfrantisek)
* Fix a problem when Pagure token is not set. (@lachmanfrantisek)

## Minor

* Write mode in testing is determined whether a respective offline file exists or not. (@lachmanfrantisek)
* Allow saving sequence of responses during tests. (@lachmanfrantisek)


# 0.4.0

* Ogr no longer uses libpagure and calls Pagure API directly.
* PersistentObjectStorage can serialize data into yaml file after calling store().


# 0.3.1

## Fixes

* Added missing module ogr.services.mock

# 0.3.0

### New Features

* Mocking of GitHub and Pagure APIs for testing ogr and packit has been greatly improved.
* GithubProject now implements adding of PR comments and also comments and status on a commit.


# 0.2.0

### New Features

* GithubProject now fully supports all the forking-related methods.
* GitProject class now has a parent property to get the original GitProject of
  a fork.
* Methods related to forking received usability updates: they should be now
  easier to work with and you'll need to write less code.
* The upstream project now has a CONTRIBUTING.md file. All your contributions are
  welcome!

## Fixes

* New github pull request now link to the URL on web interface instead of API.

## Minor

* We have implemented multiple tools to increate code quality: coverage, black, pre-commit, mypy, flake8
  * All of them run in CI as well.


# 0.1.0

### New Features

* Ogr now has an API for Github releases.

## Minor

* We have started using black, flake8 and mypy to improve the code quality.

* We are running upstream CI in CentosCI.

* Ogr is using packit to bring upstream releases to Fedora.


# 0.0.3

## Fixes

* Fix the Python3.6 compatibility:
    * remove dataclasses
    * use strings for type annotations

# 0.0.2

## New Features

* You can now search/filter pull-request comments.
* New methods for changing tokens.
* Basic support for GitHub.
* New method for a file content.

## Breaking changes

* The GitHub repo was moved to the packit-service organization.

## Fixes

* Object representation of the pull-request and pull-request commend.
