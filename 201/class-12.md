# Canvas Charts

## Read 012

### Joshua McCluskey

#### Canvas

- JS pulgin for draawing chart and modeling
- download Chart.js copy the Chart.min.js 
  
  Canvas HTML syntax:

  `<canvas id="" width="" height=""></canvas>`

  `<script> let variable = document. getElementBy Id('id').getContext('2d');`
  `new Chart ('id').Line('data')</script>`

From this syntax you can build many different charts repalce .Line with desired chart type like `.Pie` `.Bar`

#### MDN articles on  Canvas and Baiscs

Fallback content is the alternate content needed tfor some browsers that don't support canvas

Render canvas by using the following and the regular steps that we learned how to render ` let chart =  canwas.getContext('2d');`

#### Drawing shapes with Canvas

the following is the syntax needed to make rectandle

`fillRect(x, y, width, height)`
`strokeRect(x,y,width, height)`
`clearRect(x,y, width, height)`

- You can begin the path needed to draw the rectangle.
- Path Methods that have different paths for objects
- `closePath()` Draws the shape outline
- fill filling the path's content area

- `moveTo(x,y)` moves the pen to the coordinates
- `lineTo(x,y)` moves the pen to the specific position
- `beginPath()` to start drawing

You can baically draw any shape if you can supply the x,y coordinates

#### Make the charts look good with style and colors

- `fillStyle = color` fills in the shape
- `strokeStyle = color` sets the style of the outline
- for transparency use a value from 0.0 to 1.0 in rgba color

- You can make line meet and make shadows
  
#### You can also draw text

  - you can draw text
  - you can style the text
  - get exact measurements on what exactly you need
  - 
[<== BACK](../README.md)
