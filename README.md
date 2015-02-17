# flex-grid-styl
grid based on flex-box, 100% custom

## Installation

```sh
bower install --save flex-grid-styl
```

## Usage

### Settings
theese are defaults, if you want to change them just add any of theese before requiring the grid

``` stylus
colsclassname = "cols"
rowclassname = "row"
default-cols = 12
maxWidth = 1024px
padding = 15px
```

### Include grid

``` stylus
@require "bower_components/flex-grid-styl/grid"
```

### Basic grid
builds grid like in bootstrap or foundation

``` stylus
buildBasicGrid()
```

### Call the mixin
    cols(many, from, suffix)

#### Examples
##### Simple
###### From default amount of total cols

``` stylus
cols(1)
```
    
######Yields:

``` css
.cols-1 {
  width: 8.3333%;
  *width: 8.3023%;
}
```

##### Custom amount of total cols

``` stylus
cols(1, 5)
```

###### Yields:

``` css
.cols-1-5 {
  width: 20%;
  *width: 19.969%;
}
```

##### Custom suffix

``` stylus
cols(1, 5, "sm")
```

###### Yields:

``` css
.cols-sm-1-5 {
  width: 20%;
  *width: 19.969%;
}
```
  
##### No dublicated values created
  
``` stylus  
cols(1,4)
cols(3,12)
```

###### Yields:

``` css
.cols-1-4,
.cols-3-12 {
  width: 25%;
  *width: 24.969%;
}
```

##### Try

``` stylus
for num in (1..12)
	cols(num)
```
