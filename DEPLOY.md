# Usage

Install

`pip3 install twine wheel`

1. Create some distributions in the normal way:

```text
$ python3 setup.py sdist bdist_wheel
```

HTTPError: 400 Client Error: Only one sdist may be uploaded per release. for url: https://test.pypi.org/legacy

```text
$ python3 setup.py bdist_wheel
```

2. Upload with twine to Test PyPI and verify things look right. Twine will automatically prompt for your username and password:

```text
$ twine upload --repository-url https://test.pypi.org/legacy/ dist/*
username: ...
password:
...
```
3. Upload to PyPI:

```text
$ twine upload dist/*
```

```text
pip3 freeze > requirements.txt

pip3 install -r requirements.txt
```