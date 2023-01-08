# flake8-no-inheritance

[![Build Status](https://github.com/blablatdinov/flake8-no-inheritance/workflows/test/badge.svg?branch=master&event=push)](https://github.com/blablatdinov/flake8-no-inheritance/actions?query=workflow%3Atest)
[![codecov](https://codecov.io/gh/blablatdinov/flake8-no-inheritance/branch/master/graph/badge.svg)](https://codecov.io/gh/blablatdinov/flake8-no-inheritance)
[![Python Version](https://img.shields.io/pypi/pyversions/flake8-no-inheritance.svg)](https://pypi.org/project/flake8-no-inheritance/)
[![wemake-python-styleguide](https://img.shields.io/badge/style-wemake-000000.svg)](https://github.com/wemake-services/wemake-python-styleguide)

flake8 plugin for check and inheritance of implementations

Inheritance is bad and that composition over inheritance is a good idea

[yegor256 blog post](https://www.yegor256.com/2016/09/13/inheritance-is-procedural.html)

## Features

- Fully typed with annotations and checked with mypy, [PEP561 compatible](https://www.python.org/dev/peps/pep-0561/)


## Installation

```bash
pip install flake8-no-inheritance
```


## Example

Wrong:

```python
class Animal(object):
    
    def move(self, to_x: int, to_y: int):
        # Some logic for change coordinates

    def sound(self):
        print('Abstract animal sound')


class Dog(Animal):

    def sound(self):
        print('bark')


class Cat(Human):

    def sound(self):
        print('meow')
```

## License

[MIT](https://github.com/blablatdinov/flake8-no-inheritance/blob/master/LICENSE)


## Credits

This project was generated with [`wemake-python-package`](https://github.com/wemake-services/wemake-python-package). Current template version is: [9899cb192f754a566da703614227e6d63227b933](https://github.com/wemake-services/wemake-python-package/tree/9899cb192f754a566da703614227e6d63227b933). See what is [updated](https://github.com/wemake-services/wemake-python-package/compare/9899cb192f754a566da703614227e6d63227b933...master) since then.
