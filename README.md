# ts-cie1931-rgb
A TypeScript fork of [js-CIE-1931-rgb-color-converter](https://github.com/Shnoo/js-CIE-1931-rgb-color-converter) for usage in TypeScript Projects

## Additional Features:
- Type Declarations
- Works without modifications in TypeScript

## Installation
### NPM
`npm i ts-cie1931-rgb`

### CDN
`<script src="https://unpkg.com/ts-cie1931-rgb"></script>`


## Usage

```ts
//Import library
import ColorConverter from 'ts-cie1931-rgb';

//Convert RGB to XY for Philips Hue lights
let xy = ColorConverter.rgbToXy(red, green, blue, light.modelid);
// xy = {x: xValue, y: yValue};


//Convert RGB to XY for non Philips lights

let xy = ColorConverter.rgbToXy(red, green, blue);
// xy = {x: xValue, y: yValue};

/*Note: Colors may be off due to gamut capabilities of the Light. This setting uses a default gamut range provided by Philips Hue Docs. This may exceed the lights capabilities, resulting in wrong colors depending on lights behaviour.*/

//Convert XY + bightness to RGB

let rgb = ColorConverter.xyBriToRgb(x, y, brightness);
// rgb = {r: redValue, g: greenValue, b: blueValue}
```
