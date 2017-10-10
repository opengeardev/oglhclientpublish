# Pypi package builder for Lighthouse API Client

It is a package builder for distributing [oglhclient](https://github.com/opengear/oglhclient) throught Pypi.

For uploading a new version it is necessary to update the versions inside `setup.py`, something like:

```python
version = '0.1.5'
```

In case of a change in the [oglhclient](https://github.com/opengear/oglhclient), it is also necessary to update the `download_url` variable in `setup.py` for matching the proper release.

## Uploading

For uploading a new version:

```bash
$ git submodule update --remote
$ pandoc --from=markdown --to=rst --output=README.rst oglhclient/README.md
$ python setup.py sdist upload
```
