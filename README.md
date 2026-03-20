# MicroservicoCancha 

# Descripción
Este proyecto implementa una arquitectura de microservicios utilizando Spring Boot y Spring Cloud OpenFeign para la comunicación entre servicios.
En lugar de realizar llamadas HTTP manuales (por ejemplo con RestTemplate), se utiliza OpenFeign, que permite declarar clientes REST basados en interfaces Java, simplificando la comunicación entre microservicios.

# Arquitectura del proyecto
[ servicio-reservas ] ---> OpenFeign ---> [ servicio-usuarios ]
         |
         v
     MySQL (XAMPP)

servicio-reservas: consume datos de usuarios

servicio-usuarios: expone endpoints REST

MySQL (XAMPP): base de datos

# Cambios que se deben implemnetar
1. Agregar dependencias

spring-cloud-starter-openfeign

Configuración de Spring Cloud BOM

# 2. Habilitar Feign

Agregar @EnableFeignClients en la clase principal

# 3. Crear interfaces Feign

Definir clientes con @FeignClient

# 4. Separar responsabilidades

Un microservicio expone datos

Otro los consume mediante Feign

# 5. Configurar endpoints correctamente

Asegurar que las rutas coincidan entre servicios
