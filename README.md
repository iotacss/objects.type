# Type Object #

The type object is responsible for making responsive typography a piece of cake.


### Installation ###

```
npm install --save iotacss-type
```


### Dependencies ###

* [Settings.Default](https://github.com/iotacss/settings.default)
* [Settings.Breakpoint](https://github.com/iotacss/settings.breakpoint)


### Options ###

```
$iota-type-namespace    : 'type-' !default;
$iota-type-sizes-base   : () !default;
$iota-type-sizes-extra  : () !default;
```


### Example ###

```sass
$iota-type-sizes-base: (
  null : ( 14px, 1.3 ),
  sm   : 16px
);

$iota-type-sizes-extra: (
  'text-small': (
    null: ( 12px, 1.2 ),
    sm: 14px
  ),
  'text-large': (
    null: ( 18px, 1.4 ),
    sm: ( 20px, 1.5 )
  )
);

html {
  @include iota-type-base;
}
```

It will generate:

```css
html {
  font-size: 14px;
  line-height: 1.3;
}

.o-type-text-small {
  font-size: 12px;
  line-height: 1.2;
}

.o-type-text-large {
  font-size: 18px;
  line-height: 1.4;
}


@media screen and (min-width: 768px) {
  html {
    font-size: 16px;
  }

  .o-type-text-small {
    font-size: 14px;
  }

  .o-type-text-large {
    font-size: 20px;
    line-height: 1.5;
  }
}
```
