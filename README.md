# gradle-multi-project-example

Generic multi-project stub that we think represents the best gradle has to offer.

## Sub-Project Status

| Name | CI | Codecov | Bintray | Docs |
| :--- | :---: | :---: | :---: | :---: |
| [common-utils](https://github.com/project-aries/gradle-multi-project-example/tree/master/projects/common-utils) | [![Build Status](https://travis-ci.org/project-aries/gradle-multi-project-example.svg?branch=master)](https://travis-ci.org/project-aries/gradle-multi-project-example) | [![codecov](https://codecov.io/gh/project-aries/gradle-multi-project-example/branch/master/graph/badge.svg)](https://codecov.io/gh/project-aries/gradle-multi-project-example) | [![common-utils](https://api.bintray.com/packages/project-aries/libs-release-local/common-utils/images/download.svg) ](https://bintray.com/project-aries/libs-release-local/common-utils/_latestVersion) | [javadocs](http://htmlpreview.github.io/?https://github.com/project-aries/gradle-multi-project-example/blob/common-utils-gh-pages/docs/javadoc/index.html) |

## Latest Release

Can be sourced from Artifactory/Bintray/MavenCentral like so:
```
<dependency>
    <groupId>com.github.gradle</groupId>
    <artifactId>sub-project-name</artifactId>
    <version>X.Y.Z</version>
    <classifier>sources|tests|javadoc|all</classifier> (Optional)
</dependency>
```

## Adding New Projects

Developers should place their projects under the `projects` directory and model that 
projects `build.gradle` file on existing projects. Placing the project here will have 
it built automatically as part of this multi-project build.

## Jacoco, ErrorProne, Checkstyle, PMD, and FindBugs support

**[Jacoco](https://github.com/jacoco/jacoco)**: is a tool that ensures new code has 
proper test coverage.

**[ErrorProne](https://github.com/google/error-prone)**: is a static analysis tool 
for Java that catches common programming mistakes at compile-time and suggests fixes. 

**[Checkstyle](https://github.com/checkstyle/checkstyle)**: is a development tool that 
forces programmers to write code that adheres to a common standard.

**[PMD](https://github.com/pmd/pmd)**: is a source code analyzer that finds common programming 
flaws like unused variables, empty catch blocks, unnecessary object creation, and so forth.

**[FindBugs](https://github.com/findbugsproject/findbugs)**: is a tool which uses static 
analysis to look for and detect possible bugs in Java code.

## Use Of Test Libraries and Writing Tests

Currently we define `junit` and `assertj` as `testCompile` dependencies for all projects 
to use. Lets try to focus on using just these, and if there is a need to bring in and 
use something else, then lets first have a discussion on it before we go adding N 
number of dependencies to this project and break the look and feel we are trying to set.

Code is considered done-done when all checks have passed, code can be compiled, and at the 
very least unit and integration tests have been added to address the new code.

## Project Structure

Your package structure should start with `com.github.gradle` with your project name following. 
For example: if you're adding a project named `calamari` the root package structure of 
that project would look like `com.github.gradle.calamari`. If you're adding a project named 
`tuna-casserole` then your package structure would look like `com.github.gradle.tuna.casserole`.

## Additional Resources

* [Release Process](https://github.com/project-aries/gradle-multi-project-example/blob/master/docs/RELEASE_PROCESS.md)

