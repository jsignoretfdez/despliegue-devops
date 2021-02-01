<h1 align="center">Despliegue Nginx 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
</p>

> Practica Despliegue de Apps en Nginx.

## Importante

>La app de Node y la de react están conectadas y las peticiones desde la app
>de React se comunica con la App de node que hace las funciones de API.

>Para realizar las pruebas del Backend pueden realizarse con PostMan u otro
> programa similar o bien desde la app de React con uno de los 2 usuarios que
> están creados como ejemplo 
> usuario: user@example.com password: 1234 una vez dentro podremos consultar 
> los productos de la base de datos en la que esta conectada la App de Node, podemos
> crear un nuevo anuncio y que se guarde en la Base de Datos y borrarlo.

## Url's

>App de React desplegada en Nginx conexión mediante protocolo seguro https.

>Repositorio utilizado:
> https://github.com/davidjj76/nodepop-react-fundamentos

[jsignoret.co](https://jsignoret.co)

<hr>

>Web de fundamentos de HTML desplegada en Nginx conexión mediante protocolo seguro https.

>Repositorio utilizado:
>https://github.com/jsignoretfdez/PracticaFundamentosWeb

[sofa.jsignoret.co](https://sofa.jsignoret.co)

<hr>

>Backend Node desplegada en Nginx conexión mediante protocolo seguro https.

>Repositorio utilizado:
>https://github.com/davidjj76/nodepop_web_avanzado

[nodepop.jsignoret.co](https://nodepop.jsignoret.co)

<hr>

## Despliegue

>El despligue se ha realizado sobre un servidor Nginx, se ha instalado una
> base de datos MongoDB securizada y supervisor para que se inicie automáticamente
> y se levante de nuevo si ocurre un problema con el servidor.

## Peticiones HTTP

### Login

[POST] https://nodepop.jsignoret.co/apiv1/auth/login

> Nos devuelve el token debemos pasarle los parametros en body x-form... usuario y contraseña
> usuario: user@example.com password:1234
> Nos devuelve un token.

{
    "ok": true,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2MDE3M2I2OTk5NDAyMDJjMzM3YTU1YTQiLCJpYXQiOjE2MTIyMTQ4ODEsImV4cCI6MTYxMjM4NzY4MX0.f7TLDcDf6d-R9cJ9kqCf9cKaGXUuHPkcRO7ixNJ3i8k"
}

<hr>

### Listado Anuncios

[GET] https://nodepop.jsignoret.co/apiv1/adverts

> Nos devuelve la lista de anuncios, debemos pasarle en params el token obtenido y en Auth->Type Bearer Token y pasarle el token.

{
    "ok": true,
    "result": {
        "rows": [
            {
                "_id": "60173b699940202c337a55a3",
                "name": "iPhone 3GS",
                "sale": false,
                "price": 5000,
                "photo": "/images/anuncios/iphone.png",
                "__v": 0,
                "tags": [
                    "lifestyle",
                    "mobile"
                ]
            },
            {
                "_id": "60180ec54f1f55733ad03deb",
                "photo": "/images/anuncios/450_1000.jpeg",
                "name": "Ps5",
                "sale": true,
                "price": 500,
                "__v": 0,
                "tags": [
                    "lifestyle",
                    "work"
                ]
            },
            {
                "_id": "60180f384f1f55733ad03dec",
                "photo": "/images/anuncios/descarga.jpeg",
                "name": "Nintendo Switch",
                "sale": false,
                "price": 150,
                "__v": 0,
                "tags": [
                    "work"
                ]
            },
            {
                "_id": "60180f864f1f55733ad03ded",
                "photo": "/images/anuncios/HP-Portatiles-Profesionales-630x450.jpg",
                "name": "Portatil HP 680Pro",
                "sale": true,
                "price": 250,
                "__v": 0,
                "tags": [
                    "work"
                ]
            }
        ]
    }
}

<hr>

## Author

👤 **Jose Manuel Signoret Fernández**


## Show your support

Give a ⭐️ if this project helped you!

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
