# Labelled Switch

A customzied HTML built-in checkbox that supports the labelled two-state toggling.

# Features
+ Have two states: ON or OFF, customized on top of the built-in `<input type="checkbox">`.
+ Added element attributes to support on and off value and label.
+ Allow to specify border, outline, foreground, and background color.
+ Font style properties inherit from the containing element.

# Usage Examples
+ Load the live demo at https://johnwu-pro.github.io/labelled-switch/index.html
+ Check the source at this repository.

# Custom Attributes
| Attribute Name | Description | Required | Default Value |
|:---|:---|:---|:---|
| off-label | the OFF state label | N | Off |
| off-value | the OFF state value | N | off |
| on-label | the ON state label | N | On |
| on-value | the ON state value | N | on |

NOTE: To set the initial state, use the built-in `value` attribute. If the `value` equals to the `on-value`, the initial state will be ON; otherwise, it will be OFF.

# How to Style the Element
1. To specify the **selected button background color**:
   ```
   input[is="labelled-switch"]::selection { // or more specific selector
      background-color: rgba(255, 255, 255, 0.16);
   }
   ```
   When not specified, falls back to the "element default background color".
1. To specify the **element default background color** (i.e. whole labelled-switch background color):
   ```
   input[is="labelled-switch"] { // or more specific selector
      background-color: white; // i.e. rgb(255, 255, 255)
   }
   ```
   When not specified, falls back to the inherited background color.
1. To specify the **element border**:
   ```
   input[is="labelled-switch"] { // or more specific selector
      border: 1px solid lightgrey;
   }
   ```
   When not specified, falls back to the effective border for **text** input at that spot.
1. To specify the **selected color** (i.e. the selected option foreground (i.e. font) color):
   ```
   input[is="labelled-switch"]::selection { // or more specific selector
      color: green; // i.e. rgb(0, 128, 0)
   }
   ```
   When not specified, falls back to the "element default color".
1. To specify the **element default color** (i.e. the un-selected option foreground (i.e. font) color):
   ```
   input[is="labelled-switch"] { // or more specific selector
      color: rgba(0, 128, 0, 0.32)
   }
   ```
   When not specified, falls back to the inherited foreground (i.e. font) color.
   CAVEAT:
   * To use the ***black*** color (i.e. `rgb(0, 0, 0)`), set `{color: rgb(1, 1, 1);}`, since any color that would be resolved/computed to `rgb(0, 0, 0)` is considered that the color is not specified.
1. To specify the **element focused outline** (i.e. the outline when it's focused):
   ```
   input[is="labelled-switch"] { // or more specific selector
      outline: 1px solid lightblue;
   }
   ```
   When not specified, falls back to the effective outline for **text** input at that spot.
1. All **other sytle properties** (examples followed) will **inherit from its parent**, no need to style the element itself. 
   In fact, styling the element itself on those properties will have no effect.
    * `font-family`
    * `font-size`
    * `font-stretch`
    * `font-style`
    * `font-variant`
    * `font-weight`
    * `direction`
    * `line-height`
1. NOTE: The element size will purely depend on the font (size, weight, etc.) and the ON and OFF labels.
