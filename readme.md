<p align="center"><img src="https://avatars3.githubusercontent.com/u/34888056">Numeros En Letras</p>
<p align="center">
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/numeros-en-letras/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/numeros-en-letras/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/villca/numeros-en-letras"><img src="https://poser.pugx.org/villca/numeros-en-letras/license.svg" alt="License"></a>
</p>

## PHP Framework

<p align="center">
<img src="https://laravel.com/assets/img/components/logo-laravel.svg">
<img src="https://phalconphp.com/images/phalcon1.png">
<img src="https://symfony.com/logos/symfony_black_02.svg">
</p>

## Descripción
Convierte cualquier número en letras con el valor correspondiente.

3.982.908,99

Formato #1 
``Tres millones novecientos ochenta y dos mil novecientos ocho con noventa y nueve ``

Formato #2 
``Tres millones novecientos ochenta y dos mil novecientos ocho Bolivianos con noventa y nueve Centavos``

Formato #3 
``3.982.908,99 (Tres millones novecientos ochenta y dos mil novecientos ocho 99/100 Bolivianos)``


## Instalación
Segir los siguientes pasos.

Mediante comando:

    $ composer require villca/numeros-en-letras

ó modificando el archivo composer.json:

```json
{
    "require": {
        "villca/numeros-en-letras": "v1.2"
    }
}
```

## Configuración
Agregar a Controlador `use NumerosEnLetras;`

## Ejemplo Laravel

Agregar a la Ruta en "routes/web.php"

    $ Route::get('/villca', 'HomeController');
    
Crear el controlador "HomeController.php"

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

use NumerosEnLetras;

class HomeController extends Controller
{
    public function index()
    {
        echo 'Formato #1 ' . NumerosEnLetras::convertir(1988208.99) . '<br>';
        
        echo 'Formato #2 ' . NumerosEnLetras::convertir(1988208.99,'Bolivianos',false,'Centavos') . '<br>';
        
        echo 'Formato #3 ' . NumerosEnLetras::convertir(1988208.99,'Bolivianos',true) . '<br>';
        
    }
}
```

## Créditos

Basado en [AxiaCore/numero-a-letras](https://github.com/AxiaCore/numero-a-letras/blob/master/php/NumberToLetterConverter.class.php)

## Contactos

 [Facebook](https://www.facebook.com/JhessuVillca)
