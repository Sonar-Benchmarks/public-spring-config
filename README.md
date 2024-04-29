# public-spring-config

Set of Spring configurations collected from various public projects.
Spring configuration files are either .properties or .yaml files.

## ConfigFiles-Sourcegraph
The configuration files were obtained using a slightly modified version of the [samples downloader](https://github.com/SonarSource/languages-experimental-tooling/tree/master/personal/gaetan-ferry/samples_downloader).

The following query was used:
```
context:global (lang:yaml OR lang:Java Properties) file:resources/application.(yaml|properties)
```
