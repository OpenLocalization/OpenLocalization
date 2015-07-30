# OpenLocalization

> **Star** [OpenLocalization](https://github.com/OpenLocalization/OpenLocalization) to localize your git content to hundreds of languages

## Getting Started

After you star this repository, we automatically translate your git repositories based on the `localization.json` configuration file. Everytime any changes are made to your repository, we translate your changes and send you pull requests with the localized contents. 

See this [example](https://github.com/yufeih/LocPlayground) repository in action.



## Configuration

`localization.json` is placed at the root folder of your git repository.

The content of `localization.json` contains the following properties:

- `quality` specifies the translation quality, default to *machine*. Only *machine* is supported.
```json
    "quality": "machine"
```
- `branch` specifies the name of the branch to localize,  default to *master*. We only localize one branch for each repository.
```json
    "branch": "master"
```
- `locales` specifies a list of locales to localize, default to an empty list.
```json
    "locales": [ "zh-Hans", "de", "fr", "ja" ]
```
- `files` specifies the file format and globbing pattern of the files to translate. We currently support two file formats:`Markdown (md)` and `.NET Managed Resource File (resx)`.
```json
    "files": {
        "md": "content/**/*.md; !content/excluded/*.md",
        "resx": [ "src/app1/**/*.resx", "src/app2/**/*.resx" ]
    }
```

