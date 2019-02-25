# pilgram

[![PyPI version](https://badge.fury.io/py/pilgram.svg)](https://badge.fury.io/py/pilgram)
[![CircleCI](https://circleci.com/gh/akiomik/pilgram.svg?style=svg)](https://circleci.com/gh/akiomik/pilgram)
[![codecov](https://codecov.io/gh/akiomik/pilgram/branch/master/graph/badge.svg)](https://codecov.io/gh/akiomik/pilgram)

A python library for instagram filters.

![screenshot](screenshot.png)

The filter implementations are inspired by [CSSgram](https://una.im/CSSgram/).

## Requirements

- Python 3
- [Pillow](https://pillow.readthedocs.io/en/stable/) or [pillow-simd](https://github.com/uploadcare/pillow-simd)

## Install

```sh
pip install pillow # or pip install pillow-simd
pip install pilgram
```

## Usage

Available instagram filters on `pilgram`: `_1977`, `aden`, `brannan`, `brooklyn`, `clarendon`, `earlybird`, `gingham`, `hudson`, `inkwell`, `kelvin`, `lark`, `lofi`, `maven`, `mayfair`, `moon`, `nashville`, `perpetua`, `reyes`, `rise`, `slumber`, `stinson`, `toaster`, `valencia`, `walden`, `willow`, `xpro2`

```python
from PIL import Image
import pilgram

im = Image.open('sample.jpg')
pilgram.aden(im).save('sample-aden.jpg')
```

Similarly, pilgram provides css filters as a by-product.
Available css filters on `pilgram.css`: `contrast`, `grayscale`, `hue_rotate`, `saturate`, `sepia`

```python
from PIL import Image
import pilgram.css

im = Image.open('sample.jpg')
pilgram.css.sepia(im).save('sample-sepia.jpg')
```

## Test

```sh
pipenv install --dev
make test
```
