# public-spring-config

Combination of Spring configurations files either collected from various public project or handcraft for check validation on peachee.
Spring configuration files are either .properties or .yaml files.

## ConfigFiles-Sourcegraph
The configuration files were obtained using a slightly modified version of the [samples downloader](https://github.com/SonarSource/languages-experimental-tooling/tree/master/personal/gaetan-ferry/samples_downloader).

The following query was used:
```
context:global (lang:yaml OR lang:"Java Properties") file:resources/application.(yaml|properties)
```
## ConfigFiles-SpecificCheck
Handcrafted files to validate specific checks for Spring.

## Micronaut-properties-github
The samples_downloader was used and following query for GitHub (the Sourcegraph was unavailable due to reindexing sources from GitHub)
```
python download_samples.py -vk --source github --output output --auth XXXXX --max 300 "filename:resources/application.properties size:>400 micronaut"
```

## Micronaut-yaml-github
The samples_downloader was used and following query for GitHub (the Sourcegraph was unavailable due to reindexing sources from GitHub)
```
python download_samples.py -vk --source github --output output --auth XXXXX --max 300 "filename:resources/application.yaml size:>400 micronaut"
python download_samples.py -vk --source github --output output --auth XXXXX --max 300 "filename:resources/application.yml size:>400 micronaut"
```

## Micronaut-properties-SpecificCheck & Micronaut-yaml-SpecificCheck
Handcrafted files to validate specific checks for Micronaut.

## How to remove file duplicates (on Mac)
```shell
fdupes -rdN .
```
