+++
images = "/uploads/CryptoMedication Original.png"
text_field = "Rocketman is on his fucking way bitch "
title = "Rocketman"
view = 7
[header]
caption = ""

+++
# Front Matter

Front matter allows page-specific metadata and functionality to be included at the top of a Markdown file.

In the documentation and the example site, we will predominantly use [YAML](https://learnxinyminutes.com/docs/yaml/) to format the front matter of content files and [TOML](https://learnxinyminutes.com/docs/toml/) to format the configuration files and widget files. This is because TOML is more human-friendly but popular Markdown editors primarily support YAML front matter in content files.

For editing your content locally on your computer, we recommend [Typora](https://www.typora.io/) or [Visual Studio Code](https://code.visualstudio.com/).

If a content file has front matter variables set between triple-minus `---` lines, then it is YAML formatted. Otherwise, a content file will have front matter variables set between triple-plus `+++` lines, indicating that it is TOML formatted. The front matter may include metadata such as page title, date published, author, categories, tags, and so on. Here is a simple example:

    ---
    date: 2017-12-01
    title: My first blog post
    ---
    

## TOML

The example configuration and publication files are formatted in [TOML](https://learnxinyminutes.com/docs/toml/).

set between triple-plus `+++` lines. The variables may include metadata such as page title, date published, author, categories, tags, and so on. Here is a simple example:

    +++
    date = 2017-12-01
    title = "My first blog post"
    +++
    

Each configuration section (referred to as a _table_ in TOML) is defined by a name in square brackets (e.g. `[image]`). If you are adding new parameters to a file, consider which configuration section they should belong to. Often the first configuration section in front matter will not be explicitly defined, but can be thought of as the _root_ or _main_ section. If you are **adding parameters to a file**, they **should always be added to the root section** at the top of the file unless they define their own configuration section, in which case they can be placed at the end of the front matter. Otherwise, you may see strange behavior such as your new parameters having no effect.

TOML aims to be simpler and more human friendly than other popular configuration formats that are designed more for machines, such as YAML. Thus, managing your site configuration is designed to be as easy as possible.

## RStudio

If you are using RStudio to edit your site and wish to include an RMarkdown file, you’ll need to utilise [YAML](https://learnxinyminutes.com/docs/yaml/) in your RMarkdown file as RMarkdown does not yet support the TOML format.