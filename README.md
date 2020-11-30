# AngularProjectDemo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.0.2.

## Development server

Ejecutar `npm start` para levantar el ambiente en dev. abrir la url `http://localhost:4200/`. La aplicacion se recarga automaticamente si se hace algún cambio.

## Librerias
para realizar la demo se usaron las siguientes librerias

PWA
proxy-api
NgRX
Ngx Bootstrap
json-server
## Proceso para realizar pruebas
Contar con node instalado en el computador, adicionalmente se debe tener angular-cli instalado, con este comando se instala npm install -g @angular/cli
Se debe clonar la aplicación en una ubicación y luego ubicarnos dentro del proyecto descargado, ejecutar el comando npm install y ejecutar después el comando ng add @angular/pwa.

En una nueva terminal y sobre la ruta del proyecto c:user/carpeta/angular-project-demo ejecutar el comando json-server --watch .\json-server\db.json, lo que hará este comando es inicializar un json que simula una db, para poder probar la API

se verá algo como lo siguiente:
![json-server](https://user-images.githubusercontent.com/22681704/100566447-08da3980-3294-11eb-9f55-7424a277e98c.PNG)

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
