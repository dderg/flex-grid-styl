# flex-grid-styl
grid based on flex-box, 100% custom

## Usage

### Settings
theese are defaults, if you want to change them just add any of theese before requiring the grid
    colsclassname = "cols"
    rowclassname = "row"
    default-cols = 12
    maxWidth = 1024px
    padding = 15px

### Include grid
    @require "bower_components/flex-grid-styl/grid"

### Call the mixin
cols(many, from, suffix)

#### Examples
##### Simple
###### From default amount of total cols

    cols(1)
    
######Yields:

    .cols-1 {
      width: 8.3333%;
      *width: 8.3023%;
    }

##### Custom amount of total cols

    cols(1, 5)
###### Yields:

    .cols-1-5 {
      width: 20%;
      *width: 19.969%;
    }

##### Custom suffix

    cols(1, 5, "sm")

###### Yields:

    .cols-sm-1-5 {
      width: 20%;
      *width: 19.969%;
    }
  
##### No dublicated values created
  
    cols(1,4)
    cols(3,12)
    
###### Yields:

    .cols-1-4,
    .cols-3-12 {
      width: 25%;
      *width: 24.969%;
    }



