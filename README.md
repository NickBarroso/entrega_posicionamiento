![Logo](https://framerusercontent.com/images/zJBgnto0UuieHjFzX0KB4xPLrLk.png)


# 1. Posicionamiento CSS - Segunda entrega

En el siguiente proyecto se ha abordado la construcción del CSS en las siguientes fases:

### Planteamiento general:
1. CSS Reset + aplicación de estilos principales en el body.
2. Aplicación de los bordes a los elementos para diferenciarlos.

### Header:
1. Colocación del position: fixed.

### Body:
1. Primera sección:
    - Contenido.
    - Sidebar posicionada a la derecha de la página.

2. Segunda sección:
    - "Features" con el texto alineado y con un margen aplicado.
    
### Footer:
1. Añadido position: sticky, para que el footer se pegue al final de la página.

### Revisión y optimización:

En algunos casos se optó por otras formas de escribir, un claro ejemplo es el siguiente, en la parte original se optó por construir los bordes de la siguiente manera:

```CSS
body:first-of-type, .content, .sidebar, .features, footer{
    border: dashed 1px blue
}
```

Esto complicaba un poco la estructura. Sabiendo que todos los elementos contenedores tienen que tener un borde **dashed**, aplicándolo solo a las secciones que nos interesan con asterisco:

```CSS
body > *:not(main),
main > * {
  border: dashed 1px #9ad79b;
  padding-left: 20px;
}
```
En este caso, aplicamos el estilo a todos los contenedores dentro de body. Sin embargo, las secciones *Contenido Principal* y el *Aside* están contenidos dentro del **main** por lo que excluimos el main y luego le añadimos a su contenido el resto del estilo.