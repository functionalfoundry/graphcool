# 0.7 (2017-10-13)

You can download the latest Framework version by running `npm install -g graphcool@next`.

See the Forum for more information on the [Framework Preview](https://www.graph.cool/forum/t/feedback-new-cli-beta/949/1?u=nilan).

## Features 🎉

* [A new local development workflow for functions is available](https://github.com/graphcool/graphcool/issues/714). Additionally, there is a new & improved function runtime [when deploying a service to a remote cluster](https://github.com/graphcool/graphcool/issues/800), as well as in [the local `graphcool-dev` environment](https://github.com/graphcool/graphcool/issues/797).
* [You can now add templates to the service definition with a new add-template command](https://github.com/graphcool/graphcool/issues/720).

## Changes 💡

* [The initial project structure after upgrading a project to the Framework has been changed](https://github.com/graphcool/graphcool/issues/602).
* [Added GRAPHCOOL_PLATFORM_TOKEN env var](https://github.com/graphcool/graphcool/issues/753).
* [Removed the env command](https://github.com/graphcool/graphcool/issues/732). From now on `.graphcoolrc` is used to control deploy targets.
* [The CLI now can be run with node 6+](https://github.com/graphcool/graphcool/issues/777).

## Bug Fixes 🐛

* [The CLI now reauthenticates if an invalid session is found](https://github.com/graphcool/graphcool/issues/731).
* [Service aliases with dashes are now supported in the CLI](https://github.com/graphcool/graphcool/issues/616).
* [Fixed a problem with the confirmation when deleting projects](https://github.com/graphcool/graphcool/issues/735).


# 0.6 (2017-10-06)

## Features

* [Introducing Resolver Functions to extend your Graphcool API](https://github.com/graphcool/graphcool/issues/40) 🎉

## Bug Fixes

* [Fixed a bug that prevented relation queries for specific schemas](https://github.com/graphcool/graphcool/issues/718).

## Framework Preview

See the Forum for more information on the [Framework Preview](https://www.graph.cool/forum/t/feedback-new-cli-beta/949/1?u=nilan).

> **Note:** You can get the latest Framework version by running `npm install -g graphcool@next`.

* [graphcool init does not deploy the service anymore](https://github.com/graphcool/graphcool/issues/706).
* Improved usage texts [in general](https://github.com/graphcool/graphcool/issues/639) and [for delete](https://github.com/graphcool/graphcool/issues/697).
* [Added divider for project list](https://github.com/graphcool/graphcool/issues/653).
* [Improved output for written files](https://github.com/graphcool/graphcool/issues/664).
* [Allow .graphcool file in current folder](https://github.com/graphcool/graphcool/issues/622).
* [Search project configuration in parent folders](https://github.com/graphcool/graphcool/issues/646).
* [Deleting projects now asks for configuration in all cases](https://github.com/graphcool/graphcool/issues/631).
* [Introduced a shorthand notation for function code handlers](https://github.com/graphcool/graphcool/issues/529).
* [Renamed get-root-tokens to root-tokens](https://github.com/graphcool/graphcool/issues/634).
* [Added basic account command](https://github.com/graphcool/graphcool/commit/d7c9074659889bf751c79657cde32b78d205137a).


Currently, permission queries can't contain a header section, which will be changed soon. More information [here](https://github.com/graphcool/graphcool/issues/703).

# 0.4 (2017-09-29)

## Changes

* [Valid function names are now restricted](https://github.com/graphcool/graphcool/issues/538).
> Valid function names only use up to 64 alphanumeric letters, dashes and underscores. This is only checked when creating a new or updating an existing function and does *not* affect existing functions before updating them.
* Renamed Permanent Authentication Tokens (PATs) to Root Tokens.
* [Renaming relations requires usage of @rename directive with oldName parameter](https://github.com/graphcool/graphcool/issues/534).
* [Schema Extensions are renamed to Resolvers](https://github.com/graphcool/graphcool/issues/461).

## Features

* [The system fields createdAt and updatedAt are now optional](https://github.com/graphcool/graphcool/issues/452).
* The payload type of a resolver is now taken into account when validating the payload. This applies to [required payload types](https://github.com/graphcool/graphcool/issues/558) as well as [list payload types](https://github.com/graphcool/graphcool/issues/435).

## Bug Fixes

* [Fixed a bug that affected subscription queries using variables of type ID](https://github.com/graphcool/graphcool/issues/567).
* [Fixed a bug that prevented default values from being deleted](https://github.com/graphcool/graphcool/issues/418).
* [Fixed a bug when changing a unique Int field to a unique String field](https://github.com/graphcool/graphcool/issues/429).
* [Fixed several issues when migrating float fields](https://github.com/graphcool/graphcool/issues/574).
* [Fixed a bug where using an invalid type in a resolver schema resulted in an internal server error](https://github.com/graphcool/graphcool/issues/413).
* [Fixed a bug that prevented scalar list input fields for resolvers](https://github.com/graphcool/graphcool/issues/568).
* [Fixed a bug when returning null for a string in a resolver](https://github.com/graphcool/graphcool/issues/559).
* [Fixed a bug when creating two types of same name a resolver](https://github.com/graphcool/graphcool/issues/420).

## Framework Preview

See the Forum for more information on the [Framework Preview](https://www.graph.cool/forum/t/feedback-new-cli-beta/949/1?u=nilan).

> **Note:** The latest CLI version of the Framework Preview is currently available in version 1.4. This will soon be corrected to version 0.4 instead.

* [Wildcard permissions have been introduced that can be used to match all operations](https://github.com/graphcool/graphcool/issues/521). The project configuration of a new project created with the CLI includes the wildcard permission by default.
* [Added support for Modules in the project configuration](https://github.com/graphcool/graphcool/issues/523).
* [Environment variables can now be used for Graphcool Functions using the CLI](https://github.com/graphcool/graphcool/issues/548).
* [Added Root Token support in project configuration](https://github.com/graphcool/graphcool/issues/536).
* [Projects will not receive default public permissions for new fields/models](https://github.com/graphcool/graphcool/issues/459).
* [When deploying, subscription queries are now validated first](https://github.com/graphcool/graphcool/issues/464). Also see [here](https://github.com/graphcool/graphcool/issues/465).
* [User and File system types not included by default in projects created with the CLI](https://github.com/graphcool/graphcool/issues/151).
* [The module command has been renamed to modules](https://github.com/graphcool/graphcool/issues/686).
* [The --version command is now available](https://github.com/graphcool/graphcool/issues/670).
* [Changes for diff and deploy are now better grouped](https://github.com/graphcool/graphcool/issues/526).
* [Fixed a bug for displaying 504 and 502 error messages](https://github.com/graphcool/graphcool/issues/458) and [other errors](https://github.com/graphcool/graphcool/issues/520).
* [Fixed a bug that caused unnecessary updates to scalar list fields when deploying](https://github.com/graphcool/graphcool/issues/463).
* [Fixed a bug that caused deploys to not being aborted when errors occured](https://github.com/graphcool/graphcool/issues/540).
* [Fixed a bug with  the diff command for breaking changes](https://github.com/graphcool/graphcool/issues/557).
* [Fixed a bug when renaming a type with relations and deploying](https://github.com/graphcool/graphcool/issues/564).
