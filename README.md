## Setup

```shell
git@github.com:lecardozo/pants-sandbox.git && cd pants-sandbox && git switch debug
```

## Command

Althought I wouldn't expect the following command to look for an interpreter that fits into the `CPython==3.8.inexistingversion` constraint, it currently does.

```shell
pants --changed-since=origin/main \
      --changed-dependees=transitive \
      --filter-address-regex="src/python/py310/*" \
      --filter-target-type=pex_binary \
    package
```
