yaojizhan html template
=======================


## Image map tool

1. Open background image with GIMP
2. Resize image to width=500px
3. Save as this image to `image_map/$N.xcf`(N starts from `0`)
4. Select '''Filters > Web > Image Map''' to open GIMP Image Map tool.
5. Create all hot spots with '''Rectangler''' shape.
6. Save this image map to `image_map/$N.xcf.map`(text/html).
7. Open `image_map/$N.xcf.map` with any text editor(like vim).
8. One hot spot should like this
```
<area shape="rect" coords="65,71,144,131"  nohref="nohref" />
```
9. Copy `65,71,144,131` to `data.js`.

## Hot spot order for image map

The first hot spot should start from top-left of this map.
The second one should from the same column, then next one could the column on
the right side.

```
 .-------. .-------. .-------.
 |   1   | |       | |       |
 `-------` |   4   | |   6   |
 .-------. |       | `-------`
 |   2   | `-------` .-------.
 `-------` .-------. |   7   |
 .-------. |       | `-------`
 |   3   | |   5   |
 `-------` `-------`
```
