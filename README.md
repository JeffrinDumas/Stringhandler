# Stringhandler

### Site link
[Stringhander Site](http://21254.hosts.ma-cloud.nl/www/bae/Les1/stringhandler_basis.php "Stringhandler")

## De code van Stringhandler opdracht
<!DOCTYPE html>
<html lang="nl">
	 <head>
		<meta charset="utf-8">
		<meta name="description" content="scripting GD">
		<meta name="author" content="Ma">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link href="https://fonts.googleapis.com/css?family=Source+Code+Pro" rel="stylesheet">
		<link rel="stylesheet" type="text/css" href="style.css">
		<title>PHP String handler</title>
	</head>
	 <body>
		 <?php
		 if ( !empty($_GET)) {
				 $input1 =  $_GET['input1']; // input uit html
				 $input2 =  $_GET['input2']; // input uit html
				 $input3 = $input1 . $input2;
			 }
			else{
				 $input1 = ""; //lege string
				 $input2 = ""; //lege string
				 $input3 = "";
			 }
		  ?>
		<div class="wrapper">
			<form method="GET" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
				<fieldset>
				 <legend>Jeffrin GD1B</legend>
				 <input type = "text" name = "input1"  placeholder = <?php echo $input1 ?>> <br>
				 <input type = "text" name = "input2"   placeholder =  <?php echo $input2?>> <br>
				 <input type = "submit"  id = "submit" name = "submit" value = "submit">
			 </fieldset>
			</form>
			<hr>
			<?php

			?><ul>
				<li>Ingevoerde string 1:  <?php  echo $input1;  ?> </li>
				<li>Ingevoerde string 2:  <?php  echo $input2;  ?> </li>
				<li>String 1 getrimd trim():  <?php echo trim($input1, " ");  ?> </li>
        <li>String 2 getrimd trim():  <?php echo trim($input2, " ");  ?> </li>
        <li>String 3 concatenation van 1 en 2:  <?php echo $input3 ?> </li>
				<li>String 3 length van 1 en 2:  <?php echo $lenght = strlen($input3); ?> </li>
				<li>Zoeken naar spaties: <?php echo strpos($input3," "); ?></li>
				<li>Zoeken naar @ :<?php echo strpos($input3,"@"); ?></li>
				<li>Zoeken naar . : <?php echo strpos($input3,"."); ?></li>
				<li>Zoeken naar html en verander naar php :<?php echo str_replace("html","php",$input3);?></li>
				<li>Eerste 3 hoofdletter : <?php $hoofd = substr($input3,-$lenght,3); echo strtoupper($hoofd); ?></li>
				<li>Alles hoofdletters : <?php echo strtoupper($input3); ?></li>
				</ul>
				<hr>
				<h4>Bonus opdracht: maak code waarmee jij controleert of een input een geldig e-mail adres is</h4>
				<h4>Bonus opdracht: na submitten form, schrijf de eerder ingevoerde strings terug met PHP</h4>
			</div>
	 </body>
	 
</html>
