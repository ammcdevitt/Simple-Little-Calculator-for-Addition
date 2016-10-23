<!--Using HTML, CSS, and JS to make a calculator that adds.

Requirements:
-display area
-buttons 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
-calculate button (=)
-addition sign
-->

<!doctype html>
<html>

<head>
<title> Simple Little Calculator </title>

<style>

	table {
		border-radius: 5%;
		border: 1px solid black;
	}

	td {
		border-radius: 10%;
	}
	
	input[type=button] {
		font-family: sans-serif;
		font-size: 1500%
	}

	#display {
		height: 150%;
	}

</style>

</head>

<body>

<!--form tag used to create an HTML form for user input-->
<form name = 'simple calculator'>
	<!--center the calculator on the page-->
	<div align="center">
		<table border="1">
			<tr>
				<td align="center" colspan = '3' id = 'display'>result</td>
			</tr>
			
			<tr>
				<td><input type = 'button' value = '1' name = 'one' onclick = "register('1')"></td>
				<td><input type = 'button' value = '2' name = 'two' onclick = "register('2')"></td>
				<td><input type = 'button' value = '3' name = 'three' onclick = "register('3')"></td>
			</tr>

			<tr>
				<td><input type = 'button' value = '4' name = 'four' onclick = "register('4')"></td>
				<td><input type = 'button' value = '5' name = 'five' onclick = "register('5')"></td>
				<td><input type = 'button' value = '6' name = 'six' onclick = "register('6')"></td>
			</tr>
			
			<tr>
				<td><input type = 'button' value = '7' name = 'seven' onclick = "register('7')"></td>
				<td><input type = 'button' value = '8' name = 'eight' onclick = "register('8')"></td>
				<td><input type = 'button' value = '9' name = 'nine' onclick = "register('9')"></td>
			</tr>

			<tr>
				<td><input type = 'button' value = '0' name = 'zero' onclick = "register('0')"></td>
				<td><input type = 'button' value = '+' onclick = "register('+')"></td>
				<td><input type = 'button' value = '=' onclick = "register('=')"></td>
			</tr>
		</table>
	</div>

</form>

</body>

<script>
	var sequence = '';

	function register (input) {
		sequence += input;
		if (input == '=') {
			var x = parseInt(sequence[0]);
			var y = parseInt(sequence[2]);
			var z = x + y;
			console.log(z);
			document.getElementById('display').innerHTML = z;
		}
	}
</script>

</html>
