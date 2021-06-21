# @mixin

Define reusable styles. Mixins can take arguments for customizable behaviour.

```scss
@mixin rtl($property, $ltr-value, $rtl-value) {
  #{$property}: $ltr-value;

  [dir=rtl] & {
    #{$property}: $rtl-value;
  }
}

.sidebar {
  @include rtl(float, left, right);
}
```

## Optional Parameters

@mixins allow optional parameters by defining the default value.

```scss
@mixin someFunc($property:0) {
    // do something
}
```

## @each

Can be used to loop through parameters in mixins.

```scss
@mixin someFunc($properties) {
  @each $property in $properties {
    // do something
  }
}

.class {
    @include someFunc(property1 property2);
}
```

## Useful functions

```scss
// Assign a theme color to a list of properties with the option of darkening the theme color.

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
