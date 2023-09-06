# CREAR COLLECTION
# POST
1. Una vez levantada la pagina vamos a ir a la seccion `Content-Type Builder`
2. Creamos una nueva collection llamada 'Post'
3. Creamos los campos:
[a] `Type`: Text
    `Name`: title
    `Basic Settings`: Short text
    `Advanced Settings`: Required field

[b] `Type`: Text
    `Name`: description
    `Basic Settings`: Long text
    `Advanced Settings`: Required field

[c] `Type`: Rich text
    `Name`: body
    `Advanced Settings`: Required field

[d] `Type`: UID
    `Name`: slug
    `Basic Settings`: 'Attached field' ► title

[e] `Type`: Media
    `Name`: image
    `Basic Settings`: Single media
    `Advanced Settings`: Required field / 'Select allowed types of media' ► images

/* Con 'Configure the view' podemos order los campos */
/* Puede que la pagina tarde en cargar, en caso de que se caiga la refrescamos y listo */

# BOOK
1. Creamos una nueva collection llamada 'Book'
2. Creamos los campos:
[a] `Type`: Text
    `Name`: title
    `Basic Settings`: Short text
    `Advanced Settings`: Required field

[b] `Type`: Text
    `Name`: description
    `Basic Settings`: Long text
    `Advanced Settings`: Required field

[c] `Type`: Number
    `Name`: price
    `Number format`: big integer
    `Advanced Settings`: Required field

[d] `Type`: Number
    `Name`: stock
    `Number format`: integer
    `Advanced Settings`: Required field

[e] `Type`: UID
    `Name`: slug
    `Basic Settings`: 'Attached field' ► title

[f] `Type`: Media
    `Name`: image
    `Basic Settings`: Single media
    `Advanced Settings`: Required field / 'Select allowed types of media' ► images
3. Obtenemos los books (como explicamos en 4-Api.md)
/* En el caso que agreguemos mas colleciones una vez hecho el deploy de la aplicacion, basta con subir los nuevos cambios a github y el deploy se va a actualizar automaticamente */