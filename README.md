# PasaPalabra
Proyecto realizado en [Skylab CODERS][4]. 

Tecnologias usadas **Back-End**: `Node` `Express` `EJS` `bcrypt-nodejs` `MongoDB` `nodemon` `API`

Tecnologias usadas **Frond-End**: `javascript` `fech` (para las peticiones HTTP) `Materializecss`  (framework style)

### Visualización del proyecto
-------------


### Dependencias necesarias
-------------
Necesitas tener [Node.js][1] (Recomiendo la v8.9.3), [MongoDB][2] Instalados en tu ordenador para poder ejecutar esta aplicacion en tu Local.

Dependencias del proyecto - Package.json 
>"dependencies": {

>    "bcrypt-nodejs": "0.0.3",

>  "body-parser": "^1.5.1",

>    "consolidate": "^0.15.0",

>    "ejs": "^2.5.6",

 >   "express": "^4.15.2",

  >  "method-override": "^2.1.2",

   > "mongoose": "^4.13.6",

  >  "mustache": "^2.3.0"

  >}
  

### Instalacion del proyecto
-------------
Si quieres instalarte el proyecto y continuar añadiendo nuevas ideas. realiza un `git clone`


- `git clone https://github.com/VGamezz19/skylabPasaPalabra.git`

Despues,  abre tu `Terminal` y accede a la carpeta del proyecto `cd skylabPasaPalabra` e instala las dependencias del proyecto 

 - `npm install`

Proximamente, tendras que importar el fichero `preguntas.json` que se te abra descargado en tu proyecto `/skylabPasaPalabra` a tu MongoDB. Para que la aplicacion tenga los datos necesarios. Ejecuta este comando en la raíz del proyecto: 

- `mongoexport localhost:27017  --collection pasapalabras --db userpasapalabra --out preguntas.json `

Por ultimo, para ejecutar el proyecto. Abre tu `Terminal` y ejecuta el comando: 

- `npm run server`

Tambien puedes ejecutar el comando `node index.js`para ejecutar la aplicacion, pero no levantaras el [nodemon][3]

>  "scripts": {

>  "server": "nodemon index.js",

 > "start": "node index.js",

 >"test": "echo \"Error: no test specified\" && exit 1"

 > },

Como podemos ver  en el `package.json`. En el apartado "scripts" estan definidos `server`(que ejecuta el **nodemon** como he comentado antes) y `start` (Heroku recomienda reservar el comando **start** para la ejecucion de la aplicacion en produccion. 

Por defecto Node arrancara la aplicación en el puerto :5000 a no ser que previamente hayamos definido un puerto en nuestro Node 

>PORT = process.env.PORT || 5000,

No tendras que configurar tu `MongoDB` para conectarlo al proyecto. Ya que por defecto utiliza la conexión `mongodb://localhost/{nombre DB}`

### Estructura del proyecto
-------------
>controller

>------preguntas.js

>------user.js

>models

>------preguntas.js

>------user.js

>public

>------img

>------js

>------------pasa-palabra.js

>------lib

>------------materializecss

>------------font-awesome

>------tyle

>------------pasa-palabra.css

>views

>------pasa-palabra.ejs

>index.js

>Procfile

>package.json

Las carpetas más importantes con son: 

`models`, donde especificaremos los modelos que `mongoose` ha de seguir (usuario y preguntas).

 `controllers`, los **metodos que realizara el servidor a nuestra BD** y que se usaran en el cliente (updates, inserts, finds).
 
  Y por ultimo `views`, Aqui guardamos el HTML que Node tendra que compilar (por eso esta en formato EJS)

[1]: https://nodejs.org/es/
[2]: https://docs.mongodb.com/manual/installation/
[3]: https://nodemon.io/
[4]:http://www.skylabcoders.com/es

### Deploy Heroku
-------------