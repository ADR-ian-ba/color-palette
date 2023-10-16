![image](https://github.com/ADR-ian-ba/color-palette/assets/119506352/7f41c5bb-19ff-4319-8a77-49c4bdc3a2f1)
<<<<<<< HEAD
=======

>>>>>>> 20ed333ec746870c751d43cc3484c8d0a6c70c44
# Color-Palette Generator 🎨

A simple package allowing you to create color s easily.

## About 📰

Hi i am adrian, a college student wanting to do stuff, this package will allow you to create color palette easily, even knowing the name of the color given.

## installation 🌏
for javascript you can install using npm install (i)
```javascript
npm install @adr-ian/color-palette

```

## usage 📰

### color Palette Generation 🌈
generate simple color palette
```js
import {Analogus} from "color-palette"

let color = Analogus(10)
```
this will generate a random color palette using **Analogus** color theory
```
[ [ '267ef0' ],[ 'b324e3' ],[ 'fa202f' ],[ '000000' ],[ '074219' ] ]
```
![My Logo](https://github.com/ADR-ian-ba/color-palette/blob/main/gradient.png?raw=true)
**Generation method**
* Monochromatic
* Analogus
* Square
* Triadic
* Complimentary

#### Parameters
there is 6 parameter. 1 Parameter for **Amount of Color** is mandatory, and the other is
* Hex (default is **True**)
* RGB (default is **False**)
* CMYK (default is **False**)
* HSB (default is **False**)
* Real Name (default is **False**)

```js
import {Analogus} from "color-palette"

let color = Monochromatic(10, {
    hex: true, 
    rgb: true, 
    cmyk: true, 
    realName: true, 
    hsb: true
})
```
the code provided will generate data as follows
```js
let color = [
 [
    '281e5e', //hex
    [ 40, 30, 94 ], //rgb
    [ 57, 68, 0, 63 ], //cmyk
    [ 249, 68, 37 ], //hsb
    'Intergalactic Cowboy' //real name
  ]
]
```


### Color Blindness Manipulation 🦯
currently this package support 7 type of color blindness

##### Color blindness support
* Protanopia (weak red)
* Deuteranopia (weak green)
* Tritanopia (weak blue)
* Protanomaly (Blind red)
* Deuteranomaly (Blind green)
* Tritanomaly (Blind blue)
* Achromatopsia (Total Color Blindness)

to use, put "simulate" in front of the color blindness, and the para meter will be rgb, and the result will be a list of **[R, G, B]**

```js
import {simulateProtanopia} from "color-palette"

let colorBlind = simulateProtanopia(250,202,56)

//colorBlind = [ 229, 228, 91 ]

//simulateProtanopia (r, g b)
//simulateDeuteranopia (r, g b)
//simulateTritanopia (r, g b)
//simulateProtanomaly (r, g b)
//simulateDeuteranomaly (r, g b)
//simulateTritanomaly (r, g b)
//simulateAchromatopsia (r, g b)
```
![Alt text](https://github.com/ADR-ian-ba/color-palette/blob/main/colorblind.png?raw=true)
### Color Conversion Support 💁‍♂️
this package also helps you to convert color from one type to other type

##### Color Conversion Support
* **HSB** to **HEX**
* **HSB** to **RGB**
* **HSB** to **CMYK**
* **HEX** to **RGB**
* **RGB** to **HEX**

```js
import {hsbToHex} from "color-palette"

let color = hsbToHex(h, s, b)

// let color = hsbToCmyk(h, s, b)
// let color = hsbToRgb(h, s, b)
// let color = hexToRgb(hex)
// let color = rgbToHex(r, g, b)

//hex = 'faca38'
//rgb = [r, g, b]
//cmyk = [c, m, y, k]
//hsb = [h, s, b]
```

the return will be a list, excepet for hex, hex result will be the hex code without the "#"

### Color Naming Support 🔥

this package support name to color, with precision of **30.200** color, this also takes refrence from [NTC.Js](https://chir.ag/projects/ntc/).

![Alt text](https://github.com/ADR-ian-ba/color-palette/blob/main/image-1.png?raw=true)

```js
import {ntc} from "color-palette"

let colorName  = ntc.name("faca38")
//colorName = sunGlow
```




