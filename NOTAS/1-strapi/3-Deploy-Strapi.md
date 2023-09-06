# GITHUB
1. Creamos un nuevo repositorio
2. En la terminal escribimos los comandos:
[a] `git add .`
[b] `git commit -m "strapi" `
[c] `git remote add origin https://github.com/BautiLuciani/strapiBluuweb.git`
[d] `git branch -M main`
[e] `git push -u origin main`

# RENDER
1. En 'new' vamos a `Web Server`
2. Nos conectamos con github
3. Elegimos el repositorio el cual deseamos conectar y tocamos en 'connect'
4. Definimos un nombre
5. Si usamos yarn nos aseguramos que en 'Build Command' diga `yarn, yarn build`
6. Si usamos yarn nos aseguramos que en 'Start Command' diga `yarn start` 
7. En la seccion de 'Advanced' ► 'Add Enviroment Variable' debemos agregar las siguientes variables de entorno que se encuentran en el archivo '.env', cada una con su respectivo valor:
[a] `APP_KEYS`
[b] `API_TOKEN_SALT`
[c] `ADMIN_JWT_SECRET`
[d] `TRANSFER_TOKEN_SALT`
[e] `JWT_SECRET`
[f] `DATABASE_CLIENT`
[g] `DATABASE_HOST`
[h] `DATABASE_PORT`
[i] `DATABASE_NAME`
[j] `DATABASE_USERNAME`
[k] `DATABASE_PASSWORD`
[l] `DATABASE_SSL`
[m] `CLOUDINARY_NAME`
[n] `CLOUDINARY_KEY`
[o] `CLOUDINARY_SECRET`

8. Finalmente creamos el Web Service
