# Useful Sass

Sass mixins and functions that I have created that could be useful in the future.

## Assign Theme Color

Assign a theme color to a list of properties with the option of darkening the theme color.

```scss
// In this example there are three themes that determine the color that will be assigned to the property. The element that uses this code MUST have one of the theme classes attached.

@mixin assignThemeColor($properties, $darkenAmount:0) {
    @each $property in $properties {
        &.basic {
            #{$property}: darken($color: $BASIC_BLUE, $amount: $darkenAmount)
        }
        &.extra {
            #{$property}: darken($color: $EXTRA_YELLOW, $amount: $darkenAmount)
        }
        &.super {
            #{$property}: darken($color: $SUPER_RED, $amount: $darkenAmount)
        }
    }
}

.class {
    @include assignThemeColor(border-color color);
}

```

## Create Stripes

Easily create a striped background by passing the degrees and entries for each stripe.

This function reduces repetition by only requiring the color and length of each stripe instead of each stripes start and end position.

```scss
@function stripes($degrees, $entries) {
    $stripes-value: '';
    $position: 0;
    
    @each $color, $length in $entries {
        @if $stripes-value == '' {
            $stripes-value: $color
        } @else {
            $stripes-value: $stripes-value + ', ' + $color + ' ' + $position;
        }
        $position: $position + $length;
        $stripes-value: $stripes-value + ', ' + $color + ' ' + $position;
    }
    @return repeating-linear-gradient($degrees, unquote($stripes-value));
}

.class {
    background: stripes(135deg, ($color1 370px, $color2 40px, $color1 50px, $color2 50px));
}
