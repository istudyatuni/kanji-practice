## こんにちは！

This is a small typst package that print selected kanji for practicing. Look is based on [@jensechu/kanji](https://github.com/jensechu/kanji).

#### Usage

```typ
#import "@local/kanji-practice:0.1.0": practice

#set page(margin: (x: 5em, y: 2em))
// Change fonts for info text
#set text(font: ("Shantell Sans", "Kiwi Maru"))

// Select kanjis. Spaces will be replaced with blank charts
#practice(kanji: "分日一国人年大")
```

Each selected kanji will look like:

![](docs/typst-screenshot.png)

## Extra requirements

Fonts:

- [KanjiStrokeOrders](https://sites.google.com/site/nihilistorguk/)
    - Some distributions, like [Fedora](https://fedoraproject.org/wiki/KanjiStrokeOrders_fonts), packages it
- YOzFontN-StdN-R

You can also download them from [fonts](https://github.com/istudyatuni/kanji-practice/tree/typst/fonts)

## Install package locally

First, you should download [kanjiapi data](https://kanjiapi.dev). Click on "API data download", and place downloaded .zip file to `data` directory. 

For converting you need Python [installed](https://www.python.org):

```py
pip install cbor2
python3 convert.py
```

Or, if you use Nix:

```sh
nix develop '.#python'
python3 convert.py
```

Then run:

```sh
just install
# install fonts for strokes order and for drawings preview
just install-fonts
```
