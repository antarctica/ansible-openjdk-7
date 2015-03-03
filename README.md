# OpenJDK 7 (`openjdk-7`)

**Part of the BAS Ansible Role Collection (BARC)**

Installs version 7 of the OpenJDK

## Overview

* Installs OpenJDK 7
* By default, sets the default Java installation to OpenJDK 7

## Availability

This role is designed for internal use but if useful can be shared publicly.

## Usage

### Requirements

#### BAS Ansible Role Collection (BARC)

* `core`

## Variables

* `openjdk_7_make_default_java_installation`
    * If "true" the openJDK will be made the default JDK using a symlink to `default_java_installation_directory_path`/`default_java_installation_directory_name`. 
    * Default: "true"
* `default_java_installation_directory_path`
    * Where the openJDK will become the system default this path will be verified to exist and if not it will be created.
    * This variable **MUST** be a valid UNIX path without a trailing slash (i.e. `/`).
    * You **SHOULD NOT** need to change this value.
    * Default: "/usr/java"
* `default_java_installation_directory_name`
    * Where the openJDK will become the system default this directory will be used as the destination of symlink used to achive this.
    * This variable **MUST** be a valid UNIX directory name and it **MUST** not already exist
    * You **SHOULD NOT** need to change this value.
    * Default: "default"

## Contributing

This project welcomes contributions, see `CONTRIBUTING` for our general policy.

## Developing

### Committing changes

The [Git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow/) workflow is used to manage development of this package.

Discrete changes should be made within *feature* branches, created from and merged back into *develop* (where small one-line changes may be made directly).

When ready to release a set of features/changes create a *release* branch from *develop*, update documentation as required and merge into *master* with a tagged, [semantic version](http://semver.org/) (e.g. `v1.2.3`).

After releases the *master* branch should be merged with *develop* to restart the process. High impact bugs can be addressed in *hotfix* branches, created from and merged into *master* directly (and then into *develop*).

### Issue tracking

Issues, bugs, improvements, questions, suggestions and other tasks related to this package are managed through the BAS Web & Applications Team Jira project ([BASWEB](https://jira.ceh.ac.uk/browse/BASWEB)).

## License

Copyright 2015 NERC BAS. Licensed under the MIT license, see `LICENSE` for details.