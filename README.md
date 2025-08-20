# PI_ecommerce
Repositorio del Proyecto Integrado de DAW 

## Requisitos Previos
- **Instalar:** 
    - XAMPP: Para tener el servidor web y base de datos (MySQL o MariaDB).
    - Composer: Para gestionar las dependencias de PHP.
    - Laravel: Instalado a través de Composer.
    - Node.js y NPM: Para utilizar tecnologías de frontend como Vue.js, React, o compilar archivos CSS/JS.

- **Descargar dependencias:**
    
    Php: composer install

    ## IMPORTANTÍSIMO:
    No poner npm run build, porque se te rompe toda la vista.

- **Crear el archivo .env**
    cp .env.example .env (copiar del .env.example)

- **Generar la clave de la aplicación Laravel:**
    php artisan key:generate

- **Configurar la base de datos en .env:**
    
    - DB_CONNECTION=mysql
    - DB_HOST=127.0.0.1
    - DB_PORT=3306
    - DB_DATABASE=ecommercedb 
    - DB_USERNAME=root 
    - DB_PASSWORD=

- **Realizar la migración de las tablas:**
    php artisan migrate

- **Insertar productos en la bd:**
    php artisan db:seed
    
## Iniciar el servidor de Laravel
php artisan serve

## Dentro de la web
(Si se han cargado los seeders) Para iniciar sesión hay dos usuarios creados:
- TestUser: 

    email: test@example.com

    password: 123456789
- AdminUser: 

    email: admin@example.com

    password: 123456789

## Urls funcionales

- **De cara al usuario:** (Se puede llegar a ellas navegando por la web)

  [Página principal](http://127.0.0.1:8000/)  
  [Tienda](http://127.0.0.1:8000/tienda)  
  [Carrito](http://127.0.0.1:8000/carrito)  
  [Detalles de un producto](http://127.0.0.1:8000/productos/{id})  
  [Confirmación del pedido](http://127.0.0.1:8000/confirmacionPedido)  
  [Sobre nosotros](http://127.0.0.1:8000/sobreNosotros)  
  [Contacto](http://127.0.0.1:8000/contacto)  
  [Aviso legal](http://127.0.0.1:8000/avisoLegal)  
  [Accesibilidad](http://127.0.0.1:8000/accesibilidad)  
  [Mapa web](http://127.0.0.1:8000/mapaWeb)  

- **Páginas de autenticación:**

  [Login](http://127.0.0.1:8000/login)  
  [Registrarse](http://127.0.0.1:8000/register)  
  [Olvidé mi contraseña](http://127.0.0.1:8000/forgot-password)  
  [Restablecer contraseña](http://127.0.0.1:8000/reset-password/{token})  
  [Verificación de email](http://127.0.0.1:8000/email/verify)  
  [Confirmar contraseña](http://127.0.0.1:8000/confirm-password)  
  [Verificación en dos pasos (2FA)](http://127.0.0.1:8000/2fa)  

- **Zona de usuario (autenticado):**

  [Perfil](http://127.0.0.1:8000/perfil)  
  [Pedidos](http://127.0.0.1:8000/pedidos)  

- **Zona de administración (admin):**

  [Dashboard](http://127.0.0.1:8000/admin/dashboard)  
  [Gestión de productos](http://127.0.0.1:8000/admin/productos)  
  [Gestión de pedidos](http://127.0.0.1:8000/admin/pedidos)  
  [Gestión de usuarios](http://127.0.0.1:8000/admin/usuarios)  

- **Configuración del perfil:**

  [Editar perfil](http://127.0.0.1:8000/perfil/configuracion)  
  [Cambiar contraseña](http://127.0.0.1:8000/perfil/contraseña)  
  [Cambiar apariencia](http://127.0.0.1:8000/perfil/apariencia)  


# Errores:
- Sino se ha configurado el correo de administrador en .env, saldrá un error a la hora de hacer el login, y cuando se ha realizado un pedido.
- (A solucionar) El login se guarda en la caché, y aunque no se haga la segunda verificación se loguea.
- La parte de cambiar a pariencia no está configurada en la mayoría de páginas, sólo en las que por defecto se crearon junto al proyecto de laravel.

