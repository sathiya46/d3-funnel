# D3 Funnel

d3-funnel.js is a JavaScript library for rendering SVG funnel and pyramid charts
using the D3.js framework. This libray was initially inspired by [smilli/d3-funnel-charts](https://github.com/smilli/d3-funnel-charts),
but includes many improvements that can be specified through initialization
options.

# Examples

An example showing some of the possible options can be found [here](https://cdn.rawgit.com/jakezatecky/d3-funnel/master/example/index.html).

# Usage

To use this library, you must include include jQuery and D3 in addition to the
`d3-funnel.js` source file.

``` html
<script src="jquery-1.11.1.min.js"></script>
<script src="d3.min.js"></script>
<script src="d3-funnel.js"></script>
```

Drawing the funnel is relatively easy:

``` javascript
var data = [
    ["Plants",     5000],
    ["Flowers",    2500],
    ["Perennials", 200],
    ["Roses",      50]
];

var chart = new D3Funnel("#funnel");
chart.draw(data);
```

More advanced options also exist:

``` javascript
var options = {
    width: 350,          // In pixels; defaults to container's width (if non-zero)
    height: 400,         // In pixels; defaults to container's height (if non-zero)
    bottomWidth: 1/3,    // The percent of total width the bottom should be
    bottomPinch: 0,      // How many sections to pinch
    isCurved: false,     // Whether the funnel is curved
    curveHeight: 20,     // The curvature amount
    fillType: "solid",   // Either "solid" or "gradient"
    isInverted: false,   // Whether the funnel is inverted
    hoverEffects: false  // Whether the funnel has effects on hover
    dynamicArea: false   // Whether the funnel should calculate the blocks by
                         // the count values rather than equal heights
};
chart.draw(data, options);
```

# License

MIT license.
