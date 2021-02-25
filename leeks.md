# leeks.js

## Usage
```js
const leeks = require('./index.js'); // Replace with "leeks.js" if not using from the Git repository

const error = leeks.colors.red;
console.log(error('Error - There were no leeks!'));

console.log(leeks.colors.red('Hello') + leeks.colors.green(' I like leeks!'));
console.log(leeks.colors.bgRed('Hello') + leeks.colors.bgGreen(' I like leeks!'));
console.log(leeks.colors.blue(leeks.styles.underline('Hello!')));

console.log(leeks.colours.grey('Hello!'));
console.log(leeks.colors.gray('Hello!'));

console.log(leeks.eightBit(32, 'hello'));
console.log(leeks.eightBitBg(32, 'hello'));

console.log(leeks.rgb([114, 137, 218], 'hello'));
console.log(leeks.rgbBg([114, 137, 218], 'hello'));

console.log(leeks.hex('#7289da', 'hello'));
console.log(leeks.hexBg('#7289da', 'hello'));
```
## Colors

Default | Background | Bright | Bright Background
--- | --- | --- | ---
black | bgBlack | blackBright | bgBlackBright
red | bgRed | redBright | bgRedBright
green | bgGreen | greenbright | bgGreenBright
yellow | bgYellow | yellowBright | bgYellowBright
blue | bgBlue | blueBright | bgBlueBright
magneta | bgMagneta | magnetaBright | bgMagnetaBright
cyan | bgCyan | cyanBright | bgCyanBright
white | bgWhite | whiteBright | bgWhitebright
gray/grey | bgGray/bgGrey | none | none

## Styles
```
reset
bold
dim
italic
overline
underline
blink
inverse
strikethrough
```

## Remove Styles
(Might change this later, this removes the style)

```
nostrikethrough
nounderline
nooverline
noblink
noinverse
```

## Other
```
8bit
8bitBg
rgb
rgbBg
hex
hexBg
supportsColour/supportsColor
```