# SVG Cheatsheet

## First Steps with SVG
* SVG tag wraps entire image.
* XML namespace to define vocabulary.
* Set height and width of document.

``` xml
<svg xmlns="http://www.w3.org/2000/svg" height="75" width="200">
</svg>
```
> <svg xmlns="http:/www.w3.org/2000/svg" height="75" width="200">
> </svg>

## Drawing Basic Shapes
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="75" width="200">
    <rect
        x="10" y="10"
        width="50" height="50"
        stroke="black" stroke-width="5"
        fill="rgb(240,90,40)"
    />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="75" width="200">
>     <rect
>         x="10" y="10"
>         width="50" height="50"
>         stroke="black" stroke-width="5"
>         fill="rgb(240,90,40)"
>      />
> </svg>

### Square
``` xml
<svg svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <rect width="100" height="100" />
</svg>
```
> <svg svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <rect width="100" height="100" />
> </svg>

### Rounded Square
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <rect width="100" height="100" rx="10" ry="10" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <rect width="100" height="100" rx="10" ry="10" />
> </svg>

### Circle
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <circle cx="50" cy="50" r="20" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <circle cx="50" cy="50" r="20" />
> </svg>

### Ellipse
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <ellipse cx="50" cy="50" rx="50" ry="20" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <ellipse cx="50" cy="50" rx="50" ry="20" />
> </svg>

### Line
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <line x1="25" y1="25" x2="50" y2="50" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <line x1="25" y1="25" x2="50" y2="50" stroke="black" />
> </svg>

### Polynomial
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <polyline points="0,100 50,25 50,75 100,0" fill="none" stroke="black" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <polyline points="0,100 50,25 50,75 100,0" fill="none" stroke="black" />
> </svg>

### Polygon
``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <polygon points="100 100 200 100 10 20" />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <polygon points="100 100 200 100 10 20" />
> </svg>


## Drawing with Path Elements
* `d` attribute specifies direction.
* `M` moves drawing pen to specified coordinates.
* `l` draws line to coordinates specified.
* `h` draws horizontal line of specified number of pixels.
* `z` closes the curve.

``` xml
<svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
    <path
        d="M 100, 7
           l 50, 100
           h -100
           z"
    />
</svg>
```
> <svg xmlns="http://www.w3.org/200/svg" height="100" width="200">
>     <path
>         d="M 100, 7
>            l 50, 100
>            h -100
>            z"
>     />
> </svg>

| Command   | Purpose                           |
| :---      | :---                              |
| M or m    | Move absolute or relative         |
| L or l    | Line                              |
| H or h    | Horizontal line                   |
| V or v    | Vertical line                     |
| C or c    | Bezier curve                      |
| S or s    | Smooth adjacent Bezier curves     |
| Q or q    | Quadratic curve                   |
| T or t    | Smooth adjacent quadratic curves  |
| A or a    | Arc                               |
| Z or z    | Close curve                       |


### Quadratic
``` xml
<svg xmlns="http://www.w3.org/2000/svg" height="100" width="200">
    <path d="M 200, 200 q 65, -65 0, -130" stroke="#b3702d" fill="transparent" />
</svg>
```
> <svg xmlns="http://www.w3.org/2000/svg" height="100" width="200">
>     <path d="M 100, 100 q 65, -65 0, -130" stroke="#b3702d"
        fill="transparent" />
> </svg>


## Adding Text to SVG Documents
* `<text></text>` tag.

``` xml
<svg xmlns="http://www.w3.org/2000/svg" height="50" width="200">
    <text x="20" y="30" text-anchor="middle" font-family="sans-serif"
        fill="#123456" font-size="25">
        Bethany's Custom Pie Maker
    </text>
</svg>
```
> <svg xmlns="http://www.w3.org/2000/svg" height="50" width="200">
>     <text x="20" y="30" text-anchor="middle" font-family="sans-serif"
          fill="#123456" font-size="25">
>         Text
>     </text>
> </svg>

* `<tspan></tspan>` tag allows to define different styles for different parts of
text.

``` xml
<svg xmlns="http://www.w3.org/2000/svg" height="50" width="200">
    <text x="80" y="30" text-anchor="middle" font-family="sans-serif"
        fill="#123456" font-size="25">
        <tspan fill="#456123" font-weight="bold">
            Text A
        </tspan>
        Text B
    </text>
</svg>
```
> <svg xmlns="http://www.w3.org/2000/svg" height="50" width="200">
>     <text x="80" y="30" text-anchor="middle" font-family="sans-serif"
>         fill="#123456" font-size="25">
>         <tspan fill="#456123" font-weight="bold">
>             Text A
>         </tspan>
>     Text B
>     </text>
> </svg>

## Adding Images to SVG Documents
``` xml
<svg xmlns="http://www.w3.org/2000/svg" height="100" width="200">
    <image x="20" y="20" width="50" height="50"
        href="image.png"/>
</svg>
```
> <svg xmlns="http://www.w3.org/2000/svg" height="100" width="200">
>     <image x="20" y="20" width="50" height="50"
>         href="image.png"/>
> </svg>

## Gradients
* `<defs></defs>` tag allows to create definitions to be used further down
in document.
* `<stop>` tags define gradient.
* `fill` attribute of `rect` points to defined gradient.

### Linear
``` xml
<svg xmlns="https://www.w3.org/200/svg" height="200" width="200">
    <defs>
        <linearGradient id="gradient1">
            <stop offset="0%" stop-color="rgb(63, 127, 0)"/>
            <stop offset="100%" stop-color="rgb(31, 63, 255)"/>
        </linearGradient>
    </defs>
    <rect x="10" y="10" width="180" height="180" fill="url(#gradient1)"/>
</svg>
```
> <svg xmlns="https://www.w3.org/200/svg" height="200" width="200">
>     <defs>
>         <linearGradient id="gradient1">
>             <stop offset="0%" stop-color="rgb(63, 127, 0)"/>
>             <stop offset="100%" stop-color="rgb(31, 63, 255)"/>
>         </linearGradient>
>     </defs>
>     <rect x="10" y="10" width="180" height="180" fill="url(#gradient1)"/>
> </svg>

### Radial
``` xml
<svg xmlns="https://www.w3.org/200/svg" height="200" width="200">
    <defs>
        <radialGradient id="gradient2">
            <stop offset="0%" stop-color="rgb(63, 127, 0)"/>
            <stop offset="100%" stop-color="rgb(31, 63, 255)"/>
        </radialGradient>
    </defs>
    <rect x="10" y="10" width="180" height="180" fill="url(#gradient2)"/>
</svg>
```
> <svg xmlns="https://www.w3.org/200/svg" height="200" width="200">
>     <defs>
>         <radialGradient id="gradient2">
>             <stop offset="0%" stop-color="rgb(63, 127, 0)"/>
>             <stop offset="100%" stop-color="rgb(31, 63, 255)"/>
>         </radialGradient>
>     </defs>
>     <rect x="10" y="10" width="180" height="180" fill="url(#gradient2)"/>
> </svg>
