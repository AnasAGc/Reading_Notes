# CHART.JS


# Drawing a line chart

1- create a canvas element in our HTML

` <canvas id="buyers" width="600" height="400"></canvas> `

2- write a script that will retrieve the context of the canvas


```
var buyers = document.getElementById('buyers').getContext('2d'); 
 new Chart(buyers).Line(buyerData);

 ```


 3-  create our data in the Js 


 ```
var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
 ```



 # Drawing a pie chart

 1 - create a canvas element in our HTML

 ``` 
 <canvas id="countries" width="600" height="400"></canvas>

 ```

 2 - get the context and to instantiate the chart

 ```
var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);

 ```

 3- create our data in the Js 


 a - addind the  data 

 ```
 var pieData = [
	{
		value: 20,
		color:"#878BB6"
	},
	{
		value : 40,
		color : "#4ACAB4"
	},
	{
		value : 10,
		color : "#FF8153"
	},
	{
		value : 30,
		color : "#FFEA88"
	}
];
 
 ```
b - add some options 

```
var pieOptions = {
	segmentShowStroke : false,
	animateScale : true
} 

```

# Drawing a bar chart 

 1 - create a canvas element in our HTML

``` 
<canvas id="income" width="600" height="400"></canvas>

```

 2 - get the context and to instantiate the chart

```

var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);

```
 3- create our data in the Js 

 ```
var barData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "#48A497",
			strokeColor : "#48A4D1",
			data : [456,479,324,569,702,600]
		},
		{
			fillColor : "rgba(73,188,170,0.4)",
			strokeColor : "rgba(72,174,209,0.4)",
			data : [364,504,605,400,345,320]
		}

	]
}
 ```



# Drawing shapes with canvas


+ fillRect(x, y, width, height)

Draws a filled rectangle.

+ strokeRect(x, y, width, height)

Draws a rectangular outline.

+ clearRect(x, y, width, height)

Clears the specified rectangular area, making it fully transparent.

## Colors

+ fillStyle = color

 Sets the style used when filling shapes.

+ strokeStyle = color

Sets the style for shapes' outline