# timecodeinputmask
A simple jQuery input mask for SMPTE timecode

timecodeinputmask is a jQuery library which creates an input mask for easily entering SMPTE timecode.

## Setup
Include the main js file
```html
<script src="jquery.js"></script>
<script src="jquery.timecodeinputmask.js"></script>
```

## Usage
### via jQuery plugin
```javascript
$(selector).timecodeinputmask(options)
```
### via data-timecodeinputmask attribute
```html
<input type="text" data-timecodeinputmask />
```

#### Any option can be passed through the use of a data attribute. Use data-timecodeinputmask-<**_the name of the option_**>="value"

## Options
### allowNegative
Allow the timecode to be negative by pressing `-` key anywhere in the input field.
Default: false

### framerate
Define the framerate. This is useful for automatically set the maxValue of the `FF` group.
Default: 25

### format
Define the format of the mask. See Groups definitions.
Default: HH:MM:SS:FF

## Groups definitions
- `HH`: Hours
- `MM`: Minutes
- `SS`: Seconds
- `FF`: Frames

## Custom groups
You can use the `groups` option to define custom groups options. 
Available properties are:
- `start`: The 0-based index of the first character of the group.
- `end`: The 0-based index of the character after the last character of the group.
- `maxValue`: maximum value of the group

### Example
```javascript
groups: [
  {
    start: 0,
    end: 2,
    maxValue: 23
  },
  {
    start: 3,
    end: 5,
    maxValue: 59
  },
  {
    start: 6,
    end: 8,
    maxValue: 59
  }...
]
```

#### Feel free to request any other option !
