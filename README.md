# MadeForScan

Is a sample iOS project of how to use dependencies scan.

The purpose of scan you project or app is to which dependency you use are not secure or have an security issue.

## Setup

1. You must have [brew](https://brew.sh) in your machine.
2. Then you may install [dependency-check](http://www.owasp.org/index.php/OWASP_Dependency_Check) via brew by enter `brew bundle` in your terminal.
3. You may need `bundler`, install by `[sudo] gem install bundler`
4. Then install gem via bundler by enter `bundle install`

## Run

```shell
dependency-check --failOnCVSS 0 -s . -o . --enableExperimental
```
