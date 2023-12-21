# Sass
1. ¿Que es sass?
    - Es como una versión mejorada a las reglas de estilo de que se hacen con css,
    ayuda a tener codigo organizado y mas facil de actualizar.
2. Ventajas:
    - variables: nos ayuda a implementar variables.
    ```scss
    $white: #fff;

    body {
      background-color: $white;
    }
    
    ```
    - anidamiento: nos ayuda a poder anidar los selectores dentro de otros para tener una mejor estructura.
    ```scss
    nav {
      ul {
        li {
          a {
          }
        }
      }
    }
    
    ```
    - mixins: nos ayuda a la reutilización de bloques de codigo.
    ```scss
    @mixin border-radius($radius) {
      -webkit-border-radius: $radius;
      -moz-border-radius: $radius;
      border-radius: $radius;
    }

    .button {
      @include border-radius(5px);
      background-color: #fff;
    }
    ```
    - herencia: nos ayuda a heredar estilos de un padre a un hijo.
    ```scss
    %padre {
      border: 1px solid #ccc;
      padding: 10px;
    }

    .hijo {
      @extend %padre;
      color: green;
    }
    ```
    - funciones: nos brinda la oportunidad de crear funciones que ayudan a realizar calculos o manipular de mejor manera el css.
    ```scss
    $base-font-size: 16px;

    body {
      font-size: $base-font-size * 2;
    }
    ```
    - modularidad: nos permite dividir el codigo por bloques mas pequeños.
    <br>
    -base
    <br>
    -- _color.scss
    <br>
    -main.scss

# BEM
- es una metodologia para escribir css o scss de manera que sea mantenible
```scss
<button class="boton boton--rojo">Click</button>
.boton{
  &--rojo{
  }
}
```
# SMACSS
- es una metodologia de organización que estan partidos en 5 categorias
    - base: se establecen los estilos por defecto o variables
    ```scss
    $rojo: red;
    $blanco: white;
    ```
    - layout: permite estructurar el diseño general.
    ```scss
    .container {
      width: 100%;
      margin: auto;
    }
    ```
    - module: es donde se agregan los componentes que se van a reutilizar.
    ```scss
    .modulo{}
    .modulo__titulo{}
    .modulo__contenido{}
    ```
    - state:
    ```scss
    .modulo:hover{}
    ```
    - theme:
    body {
      background-color: #fff;
    }