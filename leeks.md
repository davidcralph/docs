# leeks.js
Simple ANSI styling for your terminal.

## Usage
```js
const leeks = require('../dist/index.js'); // Replace with "leeks.js" if not using from the Git repository

const error = leeks.colors.red;
console.log(error('Error - There were no leeks!'));

console.log(leeks.colors.red('Hello') + leeks.colors.green(' I like leeks!'));
console.log(leeks.colors.bgRed('Hello') + leeks.colors.bgGreen(' I like leeks!'));
console.log(leeks.colors.blue(leeks.styles.underline('Hello!')));

console.log(leeks.styles.underline('Hello'));

console.log(leeks.colours.grey('Hello!'));
console.log(leeks.colors.gray('Hello!'));

console.log(leeks.eightBit(32, 'hello'));
console.log(leeks.eightBitBg(32, 'hello'));

console.log(leeks.rgb([114, 137, 218], 'hello'));
console.log(leeks.rgbBg([114, 137, 218], 'hello'));

console.log(leeks.hex('#7289da', 'hello'));
console.log(leeks.hexBg('#7289da', 'hello'));

console.log(leeks.keywords.aqua('Hello'));
console.log(leeks.bgKeywords.aqua('Hello'));

leeks.disableColours();
console.log(error('test'));

leeks.enableColours();
console.log(error('test'));

console.log(leeks.colours.blue`hello there`);

leeks.short('&a&lIam light green and bold&r &cand I am light red');

leeks.alias('primary', leeks.colours.green);
console.log(leeks.colours.primary('hi'));
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

## CSS Keywords
See the [W3C](https://www.w3.org/wiki/CSS/Properties/color/keywords) page

## Short codes

```js
leeks.short('&3&lHello &2world');
```

### Foreground colours

|Code    |Colour         |
|:-------|:--------------|
|`&0`    |`black`        |
|`&1`    |`blue`         |
|`&2`    |`green`        |
|`&3`    |`cyan`         |
|`&4`    |`red`          |
|`&5`    |`magenta`      |
|`&6`    |`yellow`       |
|`&7`    |`blackBright`  |
|`&8`    |`whiteBright`  |
|`&9`    |`blueBright`   |
|`&a`    |`greenBright`  |
|`&b`    |`cyanBright`   |
|`&c`    |`redBright`    |
|`&d`    |`magentaBright`|
|`&e`    |`yellowBright` |
|`&f`    |`white`        |
|`&#...` |hex(...)       |

### Background colours

|Code    |Colour           |
|:-------|:----------------|
|`&!0`   |`bgBlack`        |
|`&!1`   |`bgBlue`         |
|`&!2`   |`bgGreen`        |
|`&!3`   |`bgCyan`         |
|`&!4`   |`bgRed`          |
|`&!5`   |`bgMagenta`      |
|`&!6`   |`bgYellow`       |
|`&!7`   |`bgBlackBright`  |
|`&!8`   |`bgWhiteBright`  |
|`&!9`   |`bgBlueBright`   |
|`&!a`   |`bgGreenBright`  |
|`&!b`   |`bgCyanBright`   |
|`&!c`   |`bgRedBright`    |
|`&!d`   |`bgMagentaBright`|
|`&!e`   |`bgYellowBright` |
|`&!f`   |`bgWhite`        |
|`&!#...`|hexBg(...)       |

### Styles

|Code    |Style |
|:-------|:--------------|
|`&i`	 |`inverse`      |
|`&j`	 |`dim`          |
|`&k`	 |`blink`        |
|`&l`	 |`bold`         |
|`&m`	 |`strikethrough`|
|`&n`	 |`underline`    |
|`&o`	 |`italic`       |
|`&p`	 |`overline`     |
|`&r`	 |`reset`        |


## Other
```
8bit
8bitBg
rgb
rgbBg
hex
hexBg
supportsColour/supportsColor
alias
enableColours/enableColors
disableColours/enableColors
```
