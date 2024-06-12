Claro, las estructuras de control en PHP son fundamentales para dirigir el flujo de un programa. Aquí tienes una descripción y ejemplos de las principales estructuras de control en PHP.

### 1. **Condicionales**

#### `if`, `else`, `elseif`

```php
<?php
$edad = 20;

if ($edad < 18) {
    echo "Eres menor de edad.";
} elseif ($edad == 18) {
    echo "Tienes 18 años.";
} else {
    echo "Eres mayor de edad.";
}
?>
```


#### `switch`

```php
<?php
$dia = "lunes";

switch ($dia) {
    case "lunes":
        echo "Hoy es lunes.";
        break;
    case "martes":
        echo "Hoy es martes.";
        break;
    default:
        echo "No es lunes ni martes.";
}
?>
```

### 2. **Bucles**

#### `while`

```php
<?php
$contador = 0;

while ($contador < 5) {
    echo "El contador es: $contador <br>";
    $contador++;
}
?>
```

#### `do...while`

```php
<?php
$contador = 0;

do {
    echo "El contador es: $contador <br>";
    $contador++;
} while ($contador < 5);
?>
```

#### `for`

```php
<?php
for ($i = 0; $i < 5; $i++) {
    echo "El valor de i es: $i <br>";
}
?>
```

#### `foreach`

```php
<?php
$colores = array("rojo", "verde", "azul", "amarillo");

foreach ($colores as $color) {
    echo "El color es: $color <br>";
}
?>
```

### 3. **Control de Salto**

#### `break`

```php
<?php
for ($i = 0; $i < 10; $i++) {
    if ($i == 5) {
        break;
    }
    echo "El valor de i es: $i <br>";
}
?>
```

#### `continue`

```php
<?php
for ($i = 0; $i < 10; $i++) {
    if ($i == 5) {
        continue;
    }
    echo "El valor de i es: $i <br>";
}
?>
```

#### `goto`

El uso de `goto` es generalmente desaconsejado, pero aquí tienes un ejemplo:

```php
<?php
goto marca;

echo "Este texto será omitido.";

marca:
echo "Este texto será mostrado.";
?>
```

### 4. **Funciones**

Las funciones también pueden considerarse una forma de control de flujo.

```php
<?php
function saludar($nombre) {
    return "Hola, $nombre!";
}

echo saludar("Juan");
?>
```

### 5. **Declaraciones `try...catch`**

Para el manejo de excepciones:

```php
<?php
try {
    // Código que puede lanzar una excepción
    if (rand(0, 1) == 0) {
        throw new Exception("Ha ocurrido un error.");
    }
    echo "No ha ocurrido ningún error.";
} catch (Exception $e) {
    echo "Excepción capturada: " . $e->getMessage();
}
?>
```

Estas son las principales estructuras de control en PHP. Usarlas adecuadamente te permitirá dirigir el flujo de tu aplicación de manera eficiente y clara.