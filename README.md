# MadeForScan

Is a sample iOS project of how to use dependencies scan.

The purpose of scan you project or app is to which dependency you use are not secure or have an security issue.

## Setup

1. You must have [brew](https://brew.sh) in your machine.
2. Then you may install [dependency-check](http://www.owasp.org/index.php/OWASP_Dependency_Check) via brew by enter `brew bundle` in your terminal.
3. You may need `bundler`, install by `[sudo] gem install bundler`
4. Then install gem via bundler by enter `bundle install`

## Run

Dont' forgot to update bundle-audit first

```sh
bundle-audit update
```

Then

```sh
dependency-check --failOnCVSS 0 -s . -o .
```

Or ignore some CVEs that already defined in [dependency-suppressions.xml](dependency-suppressions.xml). If you ignore the CVE will not be report.

```sh
dependency-check -s . -o . --suppression dependency-suppressions.xml
```

You can make command return non-zero value to make your build pipline fail by adding `--failOnCVSS <score>`. Score is from 0 to 10 (lower is better) default value is 11 so it will never be fail.

```sh
dependency-check --failOnCVSS 0 s . -o .
```

***NOTE*** `--failOnCSVSS <score>` should be always in font of `-s <path> -o <path>` or will never return non zero
