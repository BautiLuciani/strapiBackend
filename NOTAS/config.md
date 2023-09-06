# RENDER
1. Creamos una nueva base de datos de `PostgreSQL`
2. Colocamos un nombre a la base de datos
3. Dejamos todo el resto por defecto y creamos la base de datos
4. Esperamos a que se cree la base de datos, esto puede tardar unos minutos

# STRAPI
1. Instalamos strapi con `yarn create strapi-app my-proyect` o `yarn create strapi-app .` en caso de ya estar dentro de la carpeta del proyecto
2. Elegimos la opcion `Custom (manual setting)` para hacer la configuracion manual con los datos que nos brinda Render una vez que termina de crearse la base de datos
3. En este caso elegimos la opcion `TypeScript`
4. En este caso elegimos la opcion `PostgreSQL` ya que fue la base de datos que creamos
5. El resto de las configuraciones las hacemos con los datos que nos brinda Render:
[a] Database name → `Database (Render)`
[b] Host → del `External Database URL` extraemos desde despues del @ hasta el .com, un ejemplo seria: 
    dpg-cjo9uesdfrcc73f3en2g-a.oregon-postgres.render.com
[c] Port → `Port (Render)`
[d] Username → `Username (Render)`
[e] Password → `Password (Render)`
6. Le decimos que si al `Enable SSL connection`

# CLOUDINARY
1. Instalamos un plugin para poder usar cloudinary con `yarn add @strapi/provider-upload-cloudinary`
2. Creamos el archivo `plugins.ts` dentro de la carpeta 'config'
3. Pegamos la configuracion en el archvio que creamos anteriormente. Esta configuracion esta en la documentacion oficial [https://www.npmjs.com/package/@strapi/provider-upload-cloudinary]
4. Agregamos las variables de entorno que se encuentran en la configuracion anterior en el archivo '.env'
5. Definimos las variables de entorno con los datos que nos brinda Cloudinary:
[a] CLOUDINARY_NAME → `Cloud Name (Cloudinary)`
[b] CLOUDINARY_KEY → `API Key (Cloudinary)`
[c] CLOUDINARY_SECRET → `API Secret (Cloudinary)`
6. En el archivo `middlewares.ts` dentro de la carpeta 'config' remplazamos 'strapi::security' por el objeto, el cual tambien esta en la documentacion oficial

# INICIO
1. Levantamos la pagina con `yarn run develop`
2. Puede que debido a render al principio tire errores, en ese caso volvemos a ejecutar el comando hasta que funcione
3. Al levantar la pagina nos va a agregar automaticamente una variable de entorno `JWT_SECRET` en el archivo '.env', si sigue tirando errores hay que verificar que se este agregando correctamemte