# 05GridTemplateAreaNombreOrden
* 05 grid-template-area usando nombres, dar un orden por clases, uso de media queries usando grid


```javascript
/* contenedor-media es el padre */
.contenedor-media {
    margin: 0 auto;
    max-width: 800px;
    display: grid;

    /* para un dispositivo movil */
    /* el orden mostrar elementos lo da grid-template-areas */
    /* aunque en el html este diferente. grid-template-areas tiene prioridad */
    grid-template-areas: 
    "titulo"
    "slogan"
    "info"
    "imagen"
    "entrada";   
}

@media screen and (min-width:768px) {
    .contenedor-media {       
        grid-template-areas: 
        "titulo titulo"
        "imagen slogan"
        "imagen info"
        "entrada entrada";   
        grid-template-columns: repeat(2, 50%);
    }

}

.titulo {
    grid-area: titulo;  
}

.imagen {
    grid-area: imagen;    
}

.slogan {
    grid-area: slogan;
}

.info {
    grid-area: info;
}

.entrada {
    grid-area: entrada;
}
```
