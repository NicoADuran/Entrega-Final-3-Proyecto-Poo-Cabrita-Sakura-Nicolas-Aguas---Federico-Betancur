Tienda Virtual — Proyecto en Java

Este proyecto es una aplicación de consola desarrollada en Java, que simula la gestión básica de una tienda.
Permite registrar usuarios, realizar compras, administrar productos y exportar información, siguiendo una arquitectura simple basada en clases.

------------------------------------------------------------
 FUNCIONALIDADES PRINCIPALES

 Dueña (rol administrativo)
- Iniciar sesión como dueña (usuario: admin@tienda.com, contraseña: 1234).
- Registrar nuevos productos.
- Ver todas las compras realizadas por los clientes.
- Exportar toda la información (usuarios, productos y compras) a un archivo TXT en la carpeta Descargas.

 Clientes
- Registrarse como nuevo cliente.
- Iniciar sesión con su correo y contraseña.
- Ver los productos disponibles.
- Realizar compras seleccionando producto, cantidad y método de pago.
- Consultar su historial de compras.

------------------------------------------------------------
 DATOS INICIALES

 Dueña predefinida
Nombre: Sakura Cabrita
Correo: admin@tienda.com
Contraseña: 1234
Rol: Dueña

 Cliente de prueba
Nombre: Nico Vera
Correo: nico@correo.com
Contraseña: 1234
Rol: Cliente

🛒 Productos iniciales
ID | Producto | Descripción | Precio | Categoría | Fabricante
1  | Manzanas | Frutas frescas  | 3.0 | Frutas     | CampoVerde
2  | Leche    | Entera 1 litro  | 2.5 | Lácteos    | CampoVerde
3  | Pan      | Pan artesanal   | 1.5 | Panadería  | CampoVerde

(Categoría y fabricante son valores estáticos visibles al listar productos.)

------------------------------------------------------------
 ESTRUCTURA DE CLASES PRINCIPALES

- Usuario → Clase base para todos los usuarios.
- Cliente → Hereda de Usuario, permite comprar y consultar historial.
- Duena → Hereda de Usuario, con privilegios de administración.
- Producto → Representa los productos disponibles en la tienda.
- Compra y LineaCompra → Representan las transacciones y sus detalles.
- RegistroUsuarios → Gestiona el registro e inicio de sesión.
- TipoPago → Enumeración con métodos de pago (EFECTIVO, TARJETA, TRANSFERENCIA).
- Main → Contiene la ejecución principal y el menú interactivo.

------------------------------------------------------------
 FUNCIONALIDADES DEL MENÚ PRINCIPAL

1. Iniciar sesión
2. Registrar cliente
3. Ver productos
4. Realizar compra
5. Registrar producto (solo admin)
6. Ver compras (solo admin)
7. Ver historial (cliente)
8. Exportar información (solo admin)
0. Salir

------------------------------------------------------------
 LÓGICA DE COMPRA

Cuando un cliente realiza una compra:
1. Selecciona un producto por su ID.
2. Indica la cantidad deseada.
3. Elige el método de pago.
4. El sistema calcula el total y registra la compra tanto para el cliente como para la dueña.
5. Se muestra el detalle completo (producto, cantidad, total, pago, fecha).

------------------------------------------------------------
 EXPORTACIÓN DE INFORMACIÓN

Al seleccionar la opción 8, la dueña puede exportar toda la información registrada en el sistema a un archivo TXT con el formato:

===== INFORME DE LA TIENDA =====
Fecha: YYYY-MM-DD

=== USUARIOS REGISTRADOS ===
[Lista de usuarios]

=== PRODUCTOS ===
[Lista de productos]

=== COMPRAS ===
[Lista de compras]

El archivo se guarda automáticamente en la carpeta:
Descargas/Informacion_del_DD-MM-YYYY.txt

------------------------------------------------------------
 REQUISITOS TÉCNICOS

- Java JDK 17 o superior
- IntelliJ IDEA, NetBeans o cualquier IDE compatible con Java
- No requiere base de datos (persistencia simulada en memoria)

------------------------------------------------------------
 EJECUCIÓN

1. Clonar o copiar el proyecto.
2. Abrirlo en tu IDE.
3. Ejecutar la clase Main.
4. Interactuar mediante el menú en consola.

------------------------------------------------------------
 NOTAS FINALES

- El proyecto está diseñado para practicar POO (Programación Orientada a Objetos), listas dinámicas, herencia y gestión de flujo lógico en consola.
- La dueña actúa como administradora principal del sistema.
- Los productos incluyen categoría y fabricante estáticos para simplificar la gestión.
