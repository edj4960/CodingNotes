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
