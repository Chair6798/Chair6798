# Start steps

## Step 1:Add html code

for start you should create ```.html``` file

Stater code:

```
<!DOCTYPE HTML>
<html>
    <head>
        <title  >123</title>
    </head>
    <body style="margin: 0px;" id = "body">
        <canvas id ="myCanvas" width="300" height="300" style="margin:0%;">
        <script src="Engine.js"></script>
    </body>
</html>
```
You can change ```width``` and ```heught``` vaalues if you want.

## Step2:Add javascript

create new ```<script>``` tag after ```<script src="Engine.js"></script>```

it should look like this:

```
<!DOCTYPE HTML>
<html>
    <head>
        <title  >123</title>
    </head>
    <body style="margin: 0px;" id = "body">
        <canvas id ="myCanvas" width="300" height="300" style="margin:0%;">
        <script src="Engine.js"></script>
        <script>

        </script>
    </body>
</html>
```

Cool! You end work with html!

Now i tell you about Javascript!

## Step 3: Javascript code

Classes:

```rect```,```Screen```,```layer```,```Physics```,```Velocity```

### Class: rect
This class takes 5 arguments

X
Y
Width
Height
Html color

How to use:

```

var myRect = new rect(100,60,50,50,"green")

```
You added your first rectangle! But you can't see this while you hasn't layer for this layer!

### Class: layer

Takes 1 argument:```Screen```

```

var myScreen = new Screen(60,document.getElementById("myCanvas")) // takes fps and canvas
var myLayer = new layer(myScreen) // takes screen

```
Here you can add Rectangle!

```
var myScreen = new Screen(60,document.getElementById("myCanvas"))
var myLayer = new layer(myScreen)
var myRect = new rect(100,60,50,50,"green")
myLayer.AddObject(myRect) // add rectangle to layer
myScreen.RunRender() // start render
```
it working! Now you see green rectangle on screen

### Class: Velocity

Takes 1 argument: TPS (ticks per second)

Connecting:

```
var myVelocity = new Velocity(60) // 60 default
var myScreen = new Screen(60,document.getElementById("myCanvas"))
var myLayer = new layer(myScreen)
var myRect = new rect(100,60,50,50,"green")
myLayer.AddObject(myRect) // add rectangle to layer
myScreen.RunRender() // start render
myVelocity.RunPhysics() // start velocity class
myVelocity.AddPhysicsTask(myRect)// add rectangle to velocity class
```
Using example:

```
myRect.velocity.X = 10
myRect.velocity.Y = -9
```

#Tutorial ended! Full api in Documentation.md

