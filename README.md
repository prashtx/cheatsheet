cheatsheet
==========

[R/ggplot2 intro](http://blog.echen.me/2012/01/17/quick-introduction-to-ggplot2/)

[ggplot2 docs](http://docs.ggplot2.org/current/)

[GitHub/git cool features](https://github.com/tiimgreen/github-cheat-sheet)


## Misc

```
cat rng.geojson | jq '.features |
to_entries[] |
{type:"FeatureCollection",
features: [{ geometry: .value.geometry, type: .value.type, properties: {color: ("COLOR" + (.key % 5 | tostring)) } }] }
' | less
```
