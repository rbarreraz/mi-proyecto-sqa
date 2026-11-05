# Matriz de Pruebas Automatizadas

## 1. Casos de Prueba Unitarias y de Integración (Jest)

| ID | Tipo | Módulo / Componente | Entrada / Condición | Resultado Esperado | Resultado Obtenido |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Unitaria | Servidor Express | Petición GET a `/` | Respuesta HTTP 200 OK | Exitoso (Passed) |
| **TC-02** | Integración | API E-Commerce | Petición GET a `/api/products` | Arreglo JSON de productos | Exitoso (Passed) |
| **TC-03** | Unitaria | Autenticación | Login con credenciales válidas | Token JWT generado correctamente | Exitoso (Passed) |
| **TC-04** | Regresión | Manejo de Errores | Petición GET a `/ruta-inexistente` | Respuesta HTTP 404 Not Found | Exitoso (Passed) |
