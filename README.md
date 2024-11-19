# ApuntesMetodologiaCSS

## PROBLEMAS CSS 
Los problemas + comunes de CSS son: 
- Malas prácticas como selectores, especificidad...
- ¿Qué nombre le pongo a una etiqueta?


Para resolver estos problemas existen varias soluciones como: 
- Básicas (header, wrapper...)
- Metodologías




## Arquitectura y metodología
Cuando queremos definir como equipo cómo se desarrollará el proyecto, nos encontramos que debemos definir: 
- Estructura del CSS (`Aquitectura - se centra en la organización de carpetas`)
- Cómo trabajar CSS (`Metodología - se centra en cómo nombrar las clases`)

Y tienen como objetivo cumplis que CSS sea: 
- Comprensible
- Predecible
- Reutilizable
- Escalable
- Modular






# METODOLOGÍA CSS 
Es un método a seguir para conseguir un objetivo concreto
El objetivo en CSS es ponerle `nombre a las clases` y en términos generales se pueden dividir en dos conceptos: 

- Bloque/ estructura
- Funcionalidad/ herramientas

<!-- BEM, SUIT CSS, CUBE CSS -->



## Metodologia BEM
BEm es una metodología que se basa en el concepto de bloque/estructura. 
Es decir, las reglas de cómo definir clases se basan en la estructura de HTML teniendo en cuenta: 

- `Bloque`: es la <contenedora/padre>
- `Elemento`: son las <hijas> de la <contenedora/padre>
- `Modificador`: son <hijas> con propiedades dif.

web oficial: http://getbem.com


Sólo se usan class, nada de id.
Los nombres de las clases no usan ningún tipo de nomenclaturas como Pascal Case o Kebab Case.

- `Bloque`:           .bloque
- `Elemento`:         .bloque__elemento
- `Modificador`:      .bloque__elemento--modificador


```html
<div class= "bloque">
    <div class= "bloque__elemento"></div>
        <div class= "bloque__elemento--modficador"></div>
</div>
```

```html
<div class= "container">
    <div class= "container__item"></div>
        <div class= "container__item container__item--active"></div>
</div>
```

```html
<div class= "menu">
    <div class= "menu__li"></div>
        <div class= "menu__li menu__li--active"></div>
</div>
```


```css
.menu {}
.menu__li {}
.menu__li--active {}
```



### Ventajas y desventajas de BEM
BEM tiene muchas `ventajas` en el código del día a día:
- Los nombres de las clases en CSS son fáciles
- Muy pensado para usar con preprocesadores (SCSS)

Pero tb tiene muchas `desventajas`: 
- El HTML queda muy largo







## Metodologia SUIT CSS
Es una metodología que parte del concepto de funcionalidad/utilidades o herramientas. 
Es decir, los nombres de las clases se basan en propiedades como color, centrar...

Es recomemdada para usar con REACTJS y las clases se organizan en base a: 
- Utilidades
- Componentes