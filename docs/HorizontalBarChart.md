<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>Bar Chart</title>
		<script src="https://d3js.org/d3.v4.min.js"></script>  <!-- link to D3 library -->
	</head>
	<body>
		<script>

		    var svg = d3.select("body")
		        .append("svg")
		          .attr("width", "500")
		          .attr("height", "500");

		    var bardata = [300, 100, 150, 225, 75, 275];

		    var bars = svg.selectAll("rect")
		    	.data(bardata);

		    bars.enter()
		    	.append("rect")
		    	  .attr("x", "30")
				  .attr("y", (d, i) => i*50)
				  .attr("width", d => d)
				  .attr("height", "35")
				  .attr("fill", "lightgreen");

		</script>
	</body>
</html>
