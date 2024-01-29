## こんにちは！

This is fork of original project with added support for generating PDF via Typst.

#### Basic usage:

```typ
#import "@local/kanji-practice:0.1.0": practice, jlpt-table, categories

#set page(margin: (x: 5em, y: 2em))

// print all kanjis grouped by JLPT
#jlpt-table()
// print kanjis from JLPT N5 with their meanings in table
#jlpt-table(category: categories.jlptn5, meanings: true)

// select kanjis. for spaces will be shown blank charts
#practice(kanji: "分日一国人年大")
// select kanjis from specific catogory
#practice(category: categories.jlptn5)
```

Each selected kanji will look like:

![](docs/typst-screenshot.png)

## Install local package

```sh
just install
# install fonts for strokes order and for drawings preview
just install-fonts
```

## Contribution
Of course! Please checkout the issues in the repository, and comment on one if you are planning to submit a PR! This ensures that multiple people aren't working on the same feature at once.

Please try to follow conventions throughout the repository. I am happy to provide guidance and feedback, just ping me in a github issue! :star:
