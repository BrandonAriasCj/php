```php
$edad = 20;
if ($edad < 18){
	echo "ya eres mayor de edad"
} elseif($edad == 18){
	echo "Tienes 18 años"
} else {
	echo "Eres menor de edad"
}
```

```php
$dia = "lunes";
switch ($dia){
	case "lunes":
		echo "Hou es lunes";
		break;
	case "martes":
		echo "Hoy es martes";
		break;
	default:
		echo "No es lunes ni martes";
	
}
```