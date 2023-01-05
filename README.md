# Random-Str-Messages
Generar Mensajes Aleatorios

Historia

1995 Nacimiento de JS --> Uno de los lenguajes mas populares con miles de aplicaciones y grandes empresas apostando por este recurso

2009 Nace Node.js --> Un entorno en tiempo de ejecucion multiplataforma.

2009 NPM (Node Package Manager) --> Gestor de paquetes por defecto para Node.js

¿Qué son los gestores de dependencias?
Organizan, administran y tienen una serie de herramientas las cuales podemos aprovehar en nuestros proyectos y ser mucho mas agiles en la creación de nuestras aplicaciones.

Paquetes y modulos
Van a ser instalados y utlizados segun sea el caso. Podemos tener paquetes que funcionan solamente de lado de node asi como tambien de lado de la arquitectura web.

Herramientas que tenemos al instalar Node.js

Repositorio onlines --> Podemos publicar paquetes que sean mejoras y/o ayudas para la construccion de aplicaciones.

Command Line Client (CLI) --> Cliente que nos ayuda a trabajar de manera correcta con comandos


Dependencias

npm install moment

npm install eslint --save-dev ó -D —> dependencia que solo va a ser utilizada en el entorno de desarollo

npm install react --save ó -S —> dependencia para ser llevada a produccion.

Paquetes Globales

npm install -g
Ver lista de los paquetes

npm list
Ver lista de paquetes globlales

npm list -g

npm install package-name -o → Instalar una dependencia opcional

Se pueden generar conflictos cuando se tienen paquetes que usan la misma dependencia pero en versiones diferentes. Para evitar esto se puede simular una instalación con npm install package-name —dry-run. Con esto se simula la instalación pero sin agregar ningún paquete, si no hay ningún conflicto se procede a instalar de la manera convencional.

npm install package-name@0.15.0 → Instalar la versión especifica de un paquete. Si luego se quiere instalar la versión más reciente se usa npm install package-name@latest.

npm install → Instala las dependencias que estén dentro de un package.json.

Comandos en NPM (Scripts)
En Node, existen comando por defecto como lo son npm start, npm build. Pero también podremos crear comandos personalizados.
Comandos personalizados
Para crear comandos personalizados, haremos uso de nuestra sección de “scripts” agregando los comandos que necesites, creando como alias. Por ejemplo:
  "scripts": {
    "start":"node src/index.js"
  },

Para ejecutar el comando tendremos que estar dentro de la carpeta raíz y ejecutamos el comando >npm run start

También podremos concatenar varios comandos en un solo script utilizando && para unirlos. Ejemplo:

    "concat": "node src/index.js && node src/index.js"
NOTA: si se rompe el primer comando, no funcionará el siguiente.
Comandos con NPX
Node Package Execute, nos permite ejecutar acciones particulares sin instalarlos. Lo ejecutamos y realizamos una tarea en particular. Ejemplo:

npx create-react-app my-app
Aquí crearemos un Proyecto nuevo de react, el cual contendrá su package.json y sus dependencias correspondientes.
Para ejecutar la apliación utilizamos npm start

npm install

Instala las dependencias que estén dentro de un package.json. por ejemplo al clonar un proyecto.

Podrían presentarse vulnerabilidades


npm outdate

Nos muestra las nuevas versiones disponibles de las dependencias y con la que contamos actualmente

npm install name_package@latest

Instalar la versión mas reciente de la dependencia

Debemos tener en cuenta que hay dependencias que también requieran ser actualizadas

Puede haber conflicto ya que existen dependencias que se requieren así mismas

Para eliminar una dependencia Ejemplo:
npm unistall webpack-dev-server

Otra forma es ir al archivo package.json y eliminar del listado de dependencia, dependencias de desarrollo o dependencias opcionales; una vez eliminado de la lista ejecutamos
rm -rf node_modules/
npm install

Para compilar el proyecto usamos
npm run build

Para compilar el proyecto y obtener mas informacion usamos
npm run build --dd

Para ver librerias deprecadas y sincronizar el packagelog
npm ci
