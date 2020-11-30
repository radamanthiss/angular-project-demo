# AngularProjectDemo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.2.

## Development server

Ejecutar `npm start` para levantar el ambiente en dev. abrir la url `http://localhost:4200/`. La aplicacion se recarga automaticamente si se hace algún cambio.

## Librerias y apps
para realizar la demo se usaron las siguientes librerias

PWA
proxy-api
NgRX
Ngx Bootstrap
json-server

Se recomienda tener instalado vs code para abrir el proyecto y poder realizar pruebas de una manera sencilla
## Proceso para realizar pruebas

### Listado de comandos
- npm install -g @angular/cli
- ng add @angular/pwa
- npm install
- json-server --watch .\json-server\db.json
- npm start
Contar con node instalado en el computador, adicionalmente se debe tener angular-cli instalado, con este comando se instala npm install -g @angular/cli
Se debe clonar la aplicación en una ubicación y luego ubicarnos dentro del proyecto descargado, ejecutar el comando npm install y ejecutar después el comando ng add @angular/pwa. Una vez realizado esto podemos ejecutar npm install para que se instalen todas las dependencias

En una nueva terminal y sobre la ruta del proyecto c:user/carpeta/angular-project-demo ejecutar el comando json-server --watch .\json-server\db.json, lo que hará este comando es inicializar un json que simula una db, para poder probar la API

se verá algo como lo siguiente:
![json-server](https://user-images.githubusercontent.com/22681704/100566447-08da3980-3294-11eb-9f55-7424a277e98c.PNG)

Lo siguiente será abrir una nueva terminal ya sea dentro de vs code o en cmd, y ubicarse en la ruta del proyecto para ejecutar el comando npm start, si todo funciona se verá algo de la siguiente manera

![compile](https://user-images.githubusercontent.com/22681704/100566812-fb717f00-3294-11eb-93ca-8ef41eaf2e3f.PNG)

Después podemos abrir la url http://localhost:4200/ y nos llevara a la pantalla principal de la aplicación y se verá de la siguiente manera

![home](https://user-images.githubusercontent.com/22681704/100567085-b13ccd80-3295-11eb-9e63-d15fe4fe021c.PNG)

En esta pantalla podemos dar clic en la opcion que dice user y nos aparecerá un formulario como el siguiente

![user](https://user-images.githubusercontent.com/22681704/100567175-e47f5c80-3295-11eb-9ada-eacd56d08c10.PNG)

El listado de usuarios que aparece son usuarios ya creados en nuestro archivo db.json que se ve de la siguiente manera

![db](https://user-images.githubusercontent.com/22681704/100567277-1c869f80-3296-11eb-85d6-f45ca0de26ac.PNG)

De esta manera cada vez que colocamos un nombre y apellido en el formulario y le damos enviar se almacena en nuestro archivo db.json y cada vez que recargamos la url se puede ver el nuevo usuarion en el listado.

## Arquitectura de carpetas

La aplicación se desarrollo bajo la siguiente estructura

![folders](https://user-images.githubusercontent.com/22681704/100568030-fb26b300-3297-11eb-84d4-11af0a587513.PNG)

Se realizó de esta manera ya que se puede escalar la aplicacion creando tantos componentes como se necesiten, sin necesidad de afectar lo que ya se encuentra creado

### folder app
En esta carpeta se mantiene en el proyecto para poder orquestar la aplicación como el módulo principal de la aplicación.

### folder core
La carpeta core tendrá librerías que se ocupan a través del todo el proyecto, puede ser librerías de terceros o desarrolladas por nosotros mismos.

### folder global
global liberará la carga del archivo app.module.ts para no tener todo en este archivo para evitar que se crezca innecesariamente en código

### folder shared
Aqui se crearan componentes que se necesiten en toda la aplicación por ejemplo headers y footers

### folder user
En este folde dejaremos la logica de la aplicación como tal. Por cada módulo de la aplicación tendremos una carpeta. A su vez ésta carpeta contendrá lo siguiente para ser mas escalable:

Los archivos *.module.ts tendrán configuración del componente angular. Luego el folder component tendrán lo básico para manejar la vista y el controlador. El folder services tendrá la lógica para invocar la API. Por último el folder store tendrá el código para trabajar de manera reactiva nuestra aplicación junto con nuestro almacén que contiene el objeto que se ocupara en el componente.

### folder json-server
Aqui colocaremos nuestra emulación para base de datos, se almacenara los usuarios creados al invocar la api
## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
