# Comercio_IG
Este Repositorio almacenará informacion general de Comercio para consumo de tPaGa. 
Se agregaran archivos relacionados con la planeacion de las actividades, los estados de progresos de las mismas y de igual manera de ser necesario se referenciarán los repositorios en donde se almacenarán los servicios rest y el aws. Estos ultimos seran trabajados desde Cloud 9 Plataforma en virtual en donde se podra trabajar con NodeJS, HandleBars, nodemon y demas.

### Repositorios
#### [Comercio_VW](https://github.com/carlosjara/Comercio_VW)
En este servidor se podran encontrar todos los fuentes (nodejs express, handlebars y mysql) asociados a vistas de la aplicacion que consumirá los servicios rest en [*Comercio_REST*](https://github.com/carlosjara/Comercio_REST) y en [*TPaga*](http://payment-links.docs.tpaga.co/quickstart.html#autenticacion-contra-la-tpaga-api), se busca dar detallada explicacion de cada carpeta.

Favor leer documentacion.

#### [Comercio_REST](https://github.com/carlosjara/Comercio_REST)
En este servidor se podran encontrar todos los fuentes (nodejs express, handlebars y mysql) asociados a servicios REST y a conexion con la base de datos MySQL, se busca dar detallada explicacion de cada carpeta.

Favor leer documentacion.

#### Lanzamiento de Aplicación
Para poder desplegar esta aplicacion puede hacerse clonando los repositorios en la plataforma gratuita [Cloud 9](https://c9.io/login) como proyectos en blanco o recibir permisos para compartir (Solicitar al creador) ó se puede solicitar a Carlos Jaramillo levantar estos servidores, quien realizara los siguintes pasos...

En Comercio_VW en la consola Unix (bash, en la parte inferior de Cloud 9) se debe correr 
```html
npm start
```
Puesto que en este servidor ya se encuentran instalados todos los complementos necesarios para el correcto funcionaminto.
Esto permitira visualizar la ventana principal de [SNJ](https://comercio-vw-carlosjara.c9users.io/)(que no tiene con BD no servidor REST).

En Comercio_REST en la consola Unix (bash, en la parte inferior de Cloud 9) se deben correr 
```html
mysql-ctl start
phpmyadmin-install
npm start
```
Una vez completos estos pasos sin problemas se podra navegar en el mini comercio SNJ.

#### SNJ
Plataforma de pagos y compras de libros Juveniles
URl de Acceso (una vez los dos servidores esten arriba): 
https://comercio-vw-carlosjara.c9users.io/

En la ventana de ingreso [login](https://comercio-vw-carlosjara.c9users.io/login) se podran colocar los credenciales del usuario de pruebas *tpaga_usuario* ~ _usuario_ para poder acceder.
  En caso de omitir algun campo, SNJ mencionara cual es el campo faltante
  En caso de cometer error con la contraseñna, SNJ informará el error.

En la ventana [Catalogo](https://comercio-vw-carlosjara.c9users.io/catalogo_usuario/USUARIO_ID) se podran seleccionar los libros disponibles para comprar, agregandolos al carrito uno a uno (si se quiere comprar mas de un libro del mismo volumen).
El boton con el nombre del usuario recargará la misma pagina.
El boton carrito (#) mostrará la cantidad de libros agregados al carrito y redirige a la pagina de carrito del usuario.
El boton salir cerrará la sesion de usuario llevando a Login nuevamente.

En la ventana [Carrito](https://comercio-vw-carlosjara.c9users.io/carrito_usuario/USUARIO_ID) se podran ver los libros seleccionados  seleccionar los libros disponibles para comprar, se podran borrar por unidad o completamente
El boton con el nombre del usuario recargará la misma pagina.
El boton Items (#) mostrará la cantidad de libros agregados al carrito y recarga la pagina carrito del usuario.
El boton $ #### COP mostrará el valor a pagar carrito y recarga la pagina carrito del usuario.
El boton Catalogo llevara al usuario al catalogo para seleccionar mas libros.
El boton salir cerrará la sesion de usuario llevando a Login nuevamente.

El Boton Elimiar (1) borrará uno de los libros seleccionados disminuyendo la cantidad de los libros escogidos por el usuario.
El Boton Elimiar (Todos) borrará todos los libros seleccionados quitando del carrito el libro seleccions.

El Boton Pagar (####) redirige al usuario a la aplicacion de pruebas de tpaga, en donde deberá completar el pago.

En la ventana [Finalizacion de Compra](https://comercio-vw-carlosjara.c9users.io/end_usuario/USUARIO_ID) se podran visualizar los libros comprados por el usuario y un estado de la compra dependediendo de lo entregado por TPAGA API (en este caso se pasa de creado a entregado los productos, de igual manera se guarda el registro con el token de idempotencia), agregandolos al carrito uno a uno (si se quiere comprar mas de un libro del mismo volumen).
El boton con el nombre del usuario recargará la misma pagina.
El boton Catalogo y Volver al Catalogo llevara al usuario al catalogo para seleccionar mas libros.
El boton salir cerrará la sesion de usuario llevando a Login nuevamente.


### Creado Por:
Carlos Enrique Jaramillo Aros
