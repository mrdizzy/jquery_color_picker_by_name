##Introduction

This swatch picker provides the following features:

* Hover over a main colour swatch to bring up a grid containing a palette of colours
* Change the main colour swatch by hovering over the smaller swatches in the grid. Each time you hover over a small swatch, an event will also be emitted with the hex code value of the swatch
* Colour grids are paginated and sorted by hue
* You can choose the number of swatches per grid (default is 16) and the number of swatches per row in the grid (default is 4)
* Takes a simple array of hex codes, or if you wish to label the swatches with descriptive names such as "Olive", an object containing key-value pairs where the hex code is the key and the value is the label
* Comes with a list of default colours
* Customise the style of the swatches with CSS

##Quick start
First of all make sure you include jQuery before anything else:

    <script src="http://ajax.googleapis.com/ajax/libs/jquery/2.1.0/jquery.min.js"></script>

Then include the stylesheets:

    <link rel="stylesheet" href="/stylesheets/default.css" type="text/css">

Then the color picker file itself:

    <script src="http://www.dizzy.co.uk/javascripts/jquery.color_picker.min.js"></script>


Then if you wish to use the default colour list, please include it <i>after</i> the main colour picker file.

    <script src="http://www.dizzy.co.uk/javascripts/colour_list.js"></script>

If you do not include the default colour list file, then you will need to pass a list of colours as an option. This can be either an array of hex codes:

    ["#83434", "#00000", "#00FF00"]

or an object of key-value pairs:

    { "#000000": "Black",
      "#FFFFFF": "White }

We then initialise the plugin on an element:</p>

    $('#chosen_div').colorPicker({
        default_selected_color: '#4b5320',
        colours_per_grid: 16,
        colours_per_row: 4,
    });

We can then listen for events on the element when colours are hovered over:</p>

    $('#chosen_div").on("dizzy-cp:hoverColor", function(event, hexcode) {
        console.log("Colour hexcode hovered is: " + hexcode);
    })

## Advanced

Now...