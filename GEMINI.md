# Generación de Web API .NET: Sistema de Ventas (Clean Architecture)

Actúa como Arquitecto Senior de .NET. Necesito la estructura de código para una solución de Ventas pequeña usando **Controladores** y **.NET 8/9**.

## 1. Estructura de la Solución
Por favor, genera el código esencial para estas 4 capas separadas:

### A. Capa de Dominio (Domain)
- Define la entidad `Product` (Id, Name, Price, Stock).
- Define la interfaz `IProductRepository`.

### B. Capa de Aplicación (Application)
- Crea un `ProductDTO`.
- Crea un servicio `ProductService` que maneje la lógica para "Registrar Venta" (restar stock) y "Listar Productos".

### C. Capa de Infraestructura (Infrastructure)
- Implementa `IProductRepository` usando un `DbContext` de Entity Framework Core.
- Incluye un método `UpdateStock` básico.

### D. Capa de API (WebAPI)
- Genera un **Controller** llamado `ProductsController`.
- El controlador debe usar **Inyección de Dependencias** para recibir el servicio de la capa de Aplicación.
- Incluye un método `[HttpGet]` para listar y un `[HttpPost]` para vender.

## 2. Reglas de Salida
1. Usa **C#** moderno (File-scoped namespaces).
2. Asegúrate de que el Controlador NO conozca el Repositorio, solo el Servicio (Desacoplamiento).
3. Devuelve `ActionResult<T>` en los métodos del controlador para seguir las mejores prácticas REST.