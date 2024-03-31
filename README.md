# advanced-testing-techniques
Repository for doing advanced techniques.

## Setup Project

1. Create and source virtualenv

```bash
virtualenv ~/.advanced-testing
source ~/.advanced-testing/bin/activate
```

2. Create Scaffold

```bash
touch Makefile && touch requirements.txt && touch hello.py && touch hello_test.py
```

3. Populate 'Makefile'

```bash
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt

test:
	python -m pytest -vv --cov=hello --cov=hellocli test_hello.py

lint:
	pylint --disable=R,C hello.py 

all: install lint test
```

### how to debug
* print
* pdb
* testing