# API
Tenemos varias opciones para el consumo de apis:
[a] `Postman`
[b] `Insomnia`
[c] `Thunder Client (Extencion de VSC)`

# COMO OBTENER LOS POST
1. En Strapi vamos a 'Setting' ► 'Roles' (User and Permissions Plugin) ► 'Public' ► 'Post'
2. Seleccionamos en 'find' y 'findOne' y lo guardamos
3. Ahora con la url + el endpoint podemos obtener los posts. En este caso seria:
[https://strapi-webserver-p8y8.onrender.com/api/posts]

# UTILIZANDO QUERY STRING
1. Si obtenemos los post nos damos cuenta de que falta el campo 'image', esto se debe a que strapi oculta algunos campos por ser tan extensos. Para poder ver todos los campos debemos agregar `populate` como query parameter. En este caso seria: [https://strapi-webserver-p8y8.onrender.com/api/posts?populate=*]
2. 
