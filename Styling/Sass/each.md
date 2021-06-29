# @Each

@each can be used to loop through parameters.

```scss
@mixin someMixin($properties) {
  @each $property in $properties {
    // do something
  }
}

.class {
    @include someMixin(property1 property2);
}
```

## Maps

@each can iterate over key/value pairs.

```scss
@each $key, $value in $map {
    // do something
}

// (key: value, key: value, ...)
```

## Lists of Lists

@each can take multiple values from lists.

```scss
@each $value1, $value2, $value3 in $list {
    // do something
}

$list:
    '1-1' '1-2' '1-3',
    '2-1' '2-2' '2-3',
    '3-1' '3-2' '3-3'
```
