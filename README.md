## Example repo for https://github.com/gohugoio/hugo/issues/6730


This minimal project imports the following Hugo Module: https://github.com/theNewDynamic/hugo-module-imgix

It attempds to map mounts following this settings: 

```
module:
  imports:
  - path: github.com/theNewDynamic/hugo-module-imgix
    mounts:
      - source: func
        target: layouts/partials/func
      - source: markup
        target: layouts/_markup
      - source: data
        target: data
```

Results in
```
Error: add site dependencies: load resources: loading templates: walk: open "func" (""): file does not exist
```

func is the only failling mount, which might indicate it is bound to "sub directories" might be related to https://github.com/gohugoio/hugo/issues/6209
