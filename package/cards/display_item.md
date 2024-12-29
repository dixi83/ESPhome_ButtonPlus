# ESPHome Button+ - Music card

## Usage

* Add the music card file to the package files
    ```
    package:
        remote_package_files:
        url: https://github.com/dixi83/ESPHome_ButtonPlus
        files: [<other files>,'package/cards/display_item.yaml'] 
    ```
* Add the display item card to the (main) display `lambda` and give it the position and [parameters](#parameters) you want
    It requires fonts and colors to be defined, this can be called as lambda, for instance:
    ```
    //id(display_item).execute(x, y, label, labelfont, labelcolor, valuenum, decimals, valuestr, valuefont, valuecolor, unit, unitfont, unitcolor, align)
    id(display_item).execute(160, 2, "External", "size_3_label", "orange", id(outside_temperature).state, 1, "", "size_3_value", "white", "°C", "size_3_unit", "grey", "TOP_LEFT");
    ```
    This will position a block with label "External" in size 3 and color orange, below that a value with 1 decimal, in white, size 3. Next to that unit "°C", size 3 in grey, anchored at x,y = 160,2 top left corner


## Parameters:

```
x:            int     x of anchor point
y:            int     y of anchor point
label:        string  label, to be shown above the value
labelfont:    string  any of size_1_value, size_2_unit, size_3_label and everything in between
labelcolor:   string  any of white, orange, red, green or grey
valuenum:     float   value to display (numerical)
decimals:     int     rounding of value to display
valuestr:     string  if left empty it will select display the value float 
valuefont:    string  any of size_1_value, size_2_unit, size_3_label and everything in between
valuecolor:   string  any of white, orange, red, green or grey
unit:         string  displayed unit
unitfont:     string  any of size_1_value, size_2_unit, size_3_label and everything in between
unitcolor:    string  any of white, orange, red, green or grey
align:        string  TOP_LEFT, TOP_CENTER or TOP_RIGHT
```
