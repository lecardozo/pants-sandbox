## Debugging pants issue

```shell
git@github.com:lecardozo/pants-sandbox.git && cd pants-sandbox && git switch debug
pants --changed-since=origin/main \
      --changed-dependees=transitive \
      --filter-address-regex="src/python/py310/*" \
      --filter-target-type=pex_binary \
    package
