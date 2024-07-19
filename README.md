<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
   <h3 align="center">Prueba Laboral Incomex - API REST con Base de Datos</h3>
  <p align="center">
    Este proyecto tiene como objetivo crear una API REST que maneje una base de datos con categorías y productos, alojada en un servicio de cloud computing gratuito.
    <br />
    <br />
  </p>
</div>

<!-- ABOUT THE PROJECT -->
## Descripción del proyecto

Este proyecto se llevó a cabo siguiendo un enfoque estructurado utilizando las herramientas de la suite de MuleSoft:

1. **Diseño de la API con RAML**: 
   - inicialmente diseñé la API utilizando RAML para especificar los endpoints, los métodos HTTP, los parámetros de entrada y salida, así como los tipos de datos involucrados.
   - En el siguiente enlace se puede revisar el exchange:
     * [Documentacion Exchange](https://anypoint.mulesoft.com/exchange/portals/prueba-948/d5e0a5d5-ffb7-4a60-9c64-b88aa27e1659/prueba_intcomex/minor/1.0/console/summary/)

2. **Transformación con Anypoint Studio**: 
   - Luego, utilicé Anypoint Studio para implementar la lógica y las transformaciones necesarias. Configuré los flujos de integración para manejar las operaciones de creación y consulta de categorías y productos, asegurando la integración con la base de datos y la generación de datos aleatorios.

3. **Despliegue con Runtime Manager**:
   - Una vez finalizada la implementación, desplegué todo en Anypoint Runtime Manager. 


### Requerimientos

- Por medio del API de Crear Categoría, se deben crear las categorías SERVIDORES y CLOUD.
- Por medio del API Crear Producto, se deben generar datos aleatorios para insertar 100,000 productos asociados a las dos categorías creadas anteriormente.
- Por medio del API de listar productos, se deben listar los 100,000 productos creados anteriormente. Esta opción deberá poder paginarse y por medio de parámetros decidir cuántos productos se mostrarán.
- El endpoint de listar productos deberá poder buscar un producto en la base de datos y traer la foto de la categoría a la que corresponde.


<!-- GETTING STARTED -->
## Getting Started

Para consumir cada una de las API lo que se debe realizar es ingresar a POSTMAN y ejecutar los siguiente endpoints.

## Crear categoria

En esta API se crean las categorias con su respectivo nombre, descripción e imagen
* ENDPOINT
  ```sh
  http://prueba-intcomex.us-e2.cloudhub.io/api/prueba-intcomex/v1/category
  ```
Para la ejecución es importante agregar la siguiente información tanto en el header como en el body:
* HEADER
 ```sh
  Content-Type:application/json
  ```
* BODY
 ```sh
  {
  "name": "CLOUD",
  "description": "Descripción cloud",
  "image_url": "https://citelia.es/wp-content/uploads/que-es-cloud-computing.jpg"
}
  ```

## Crear productos

En esta API se crean los productos con su respectivo nombre, descripción y precio. Es importante mencionar que en el desarrollo de la api se realizó un script para realizar la inserción de 100.000 productos a la base de datos
* ENDPOINT
  ```sh
  http://prueba-intcomex.us-e2.cloudhub.io/api/prueba-intcomex/v1/products
  ```
Para la ejecución es importante agregar la siguiente información tanto en el header como en el body:
* HEADER
 ```sh
  Content-Type:application/json
  ```
* BODY
 ```sh
  {
  "name": "Producto A",
  "description": "Descripción del producto",
  "price": 400000,
  "category_id": 2
  }
  ```

## Listar productos

En esta API se listan todos los productos. Es importante mencionar que en el desarrollo de la api se realizó un script para realizar la inserción de 100.000 productos a la base de datos
* ENDPOINT
  ```sh
  http://prueba-intcomex.us-e2.cloudhub.io/api/prueba-intcomex/v1/products?page=1&pageSize=10
  ```
Para la ejecución es importante agregar la siguiente información tanto en el header como en el body:
* HEADER
 ```sh
  Content-Type:application/json
  ```
* PARAMETROS
 ```sh
  page:1
  pageSize:10
  ```

## Listar productos id

En esta API se lista el producto por id
* ENDPOINT
  ```sh
  http://prueba-intcomex.us-e2.cloudhub.io/api/prueba-intcomex/v1/products/{id}
  ```
Para la ejecución es importante agregar la siguiente información en el header:
* HEADER
 ```sh
  Content-Type:application/json
  ```




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/juan-sebastian-murcia-zu%C3%B1iga-904aa921a/
[product-screenshot]: images/screenshot.png
[Next.js]: Color=white
[Next-url]: https://anypoint.mulesoft.com/exchange/portals/prueba-948/d5e0a5d5-ffb7-4a60-9c64-b88aa27e1659/prueba_intcomex/minor/1.0/console/summary/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
