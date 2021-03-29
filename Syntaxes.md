## Abstract

PHP is an acronym for "PHP: Hypertext Preprocessor"

PHP is a script language which is executed on the server

- That means you should run a server use

```php
php -S localhost:4000
```

first. (Looks like node.js)

A .php file looks like

```php
<!DOCTYPE html>
<html>
    <body>

        <?php
            echo "Looks like an script element in html";
        ?>

    </body>
</html>

```

## Class

```php
class Solution {

    // Properties
    public $p1;
    /**
     * Ducumentation like Java, not like C#
     * @return int
     */
    function func1() {
        // Not this.
        echo $this->p1;

        return 0;
    }
}
```
