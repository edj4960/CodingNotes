# Animations

## Transition

### Properties

**Element:** color, font-size, etc.

**Length:** 2s, .5s, etc.

**Effect:** _(optional)_ ease, linear, ease-in, ease-out, ease-in-out, cubic-bezier(n,n,n,n)

### Example

```css
.some-class {
    transition: color 2s;
}
```

**NOTE:** You can only have one transition decleration per element as they will overwrite one another. However you can include multiple attributes in the same transition:

```css
transition: color 2s, font-size 3s
```

or just do the following:

```css
transition: all 2s
```
