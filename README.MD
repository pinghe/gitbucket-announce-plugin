# gitbucket-announce-plugin

This plugin enhances [takezoe/gitbucket](https://github.com/takezoe/gitbucket) by providing an announce mechanism.

## Features

### Global Announce

This feature allows to notify gitbucket users. It is available to _admin_ users via  the `System Administration` menu of gitbucket.

The global announce sends an email to all active users. For that, notifications and thus SMTP settings of the global gitbucket configuration have to be correctly filled in the `System Administration\System Settings\Notification email` section.

It is then possible, for example, to notify every user that an upgrade of the system is planned the next monday at midday.

## Compatibility

Plugin version | GitBucket version
:--------------|:-----------------
1.1.x          | 3.7.x
1.0.x          | 3.6.x


## Usage

- Open a shell window at the root of the project, hit `sbt package`
- if you update gitbucket-announce-plugin, remove any existing copy of gitbucket-announce-plugin from GITBUCKET_HOME/plugins
- Copy target/scala-2.11/gitbucket-announce-plugin_2.11-1.0.jar into GITBUCKET_HOME/plugins
- Restart GitBucket

## Release Notes

### 1.1

- [issue-5](https://github.com/gitbucket-plugins/gitbucket-announce-plugin/issues/5) use new `SystemSettings.useSMTP` property introduced in gitbucket 3.7
- [pullrequest-7](https://github.com/gitbucket-plugins/gitbucket-announce-plugin/pull/7) adapt markdown parser

### 1.0

- introduce gitbucket-announce-plugin
- global announce by email in `System Administration` menu
- depends on [takezoe/gitbucket#861](https://github.com/takezoe/gitbucket/pull/861)
