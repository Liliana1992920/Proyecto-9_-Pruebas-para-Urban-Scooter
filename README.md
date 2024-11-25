# Informe Final del Proyecto: Pruebas de Urban Scooter

## **Descripción del Proyecto**
Este proyecto se centró en la validación de la aplicación **Urban Scooter**, incluyendo:
1. **Aplicación Web:** Pruebas del formulario de pedido y funciones asociadas.
2. **Aplicación Móvil:** Validación de funciones clave y diseño.
3. **API:** Verificación de endpoints y cumplimiento de requisitos del backend.

El objetivo fue asegurar que la aplicación cumpla con los requisitos funcionales y de diseño, proporcionando una experiencia de usuario sin errores.

---

## **Tarea 2: Aplicación Web Urban Scooter**

### **Objetivo**
Probar las funciones principales de la aplicación web, enfocándose en:
1. La lógica y diseño del formulario de pedido.
2. La funcionalidad de la pantalla "Estado del pedido".
3. La validación de campos en la pantalla "Hacer pedido".

### **Resultados**

#### **Mapa Mental: Función de Formulario de Pedido**
El mapa mental abarcó los siguientes puntos:
- **Entrada de datos:**
  - Campos requeridos: Nombre, Dirección, Teléfono, Tipo de Scooter, Fecha y Hora.
  - Validaciones: Restricciones de formato y campos obligatorios.
- **Acciones:**
  - Enviar pedido y mostrar confirmación visual.
- **Errores:**
  - Mensajes claros para entradas inválidas.

#### **Lista de Comprobación: Pantalla "Estado del Pedido"**
| **Elemento**             | **Requisito**                                                                 | **Resultado**       |
|---------------------------|-------------------------------------------------------------------------------|---------------------|
| Lista de pedidos          | Mostrar pedidos activos con ID, estado, fecha y hora.                        | Aprobado            |
| Cambios de estado         | Actualización en tiempo real del estado del pedido.                          | Fallo menor*        |
| Diseño responsivo         | Adaptación correcta en diferentes resoluciones.                              | Aprobado            |

#### **Validación de Campos: Pantalla "Hacer Pedido"**
| **Campo**        | **Validación**                              | **Prueba Positiva**  | **Prueba Negativa**              | **Resultado**       |
|-------------------|--------------------------------------------|----------------------|-----------------------------------|---------------------|
| Nombre            | Texto, mínimo 2 caracteres.               | "Juan Pérez"         | "@"                               | Aprobado            |
| Dirección         | Texto, mínimo 5 caracteres.               | "Calle Luna 45"      | "12"                              | Aprobado            |
| Teléfono          | Solo números, longitud 10.                | "1234567890"         | "ABC123"                          | Aprobado            |
| Tipo de Scooter   | Selección de una lista de opciones.        | "Eléctrico"          | Sin seleccionar                   | Aprobado            |
| Fecha y Hora      | Formato válido (DD/MM/AAAA HH:MM).         | "25/11/2024 14:00"   | "2024/11/25"                      | Aprobado            |

---

## **Tarea 3: Aplicación Móvil Urban Scooter**

### **Objetivo**
Validar las funciones principales y el diseño de la aplicación móvil.

### **Resultados**
| **Función**       | **Escenario**                                            | **Resultado**       |
|--------------------|----------------------------------------------------------|---------------------|
| Registro           | El usuario puede registrarse con datos válidos.          | Aprobado            |
| Inicio de Sesión   | El usuario puede iniciar sesión con credenciales válidas. | Aprobado            |
| Realizar Pedido    | El pedido se completa y muestra confirmación.            | Aprobado            |
| Cancelar Pedido    | El usuario puede cancelar un pedido en estado inicial.   | Aprobado            |
| Diseño             | La interfaz es coherente con los diseños de Figma.       | Aprobado            |

---

## **Tarea 4: API de Urban Scooter**

### **Objetivo**
Probar los endpoints principales de la API de Urban Scooter.

### **Lista de Comprobación**
| **Endpoint**                            | **Escenario**                                                    | **Resultado**       |
|-----------------------------------------|-------------------------------------------------------------------|---------------------|
| `POST /api/v1/orders`                   | Crear un pedido con datos válidos.                               | Aprobado            |
| `GET /api/v1/orders/{id}`               | Obtener los detalles de un pedido existente.                     | Aprobado            |
| `PUT /api/v1/orders/{id}/cancel`        | Cancelar un pedido existente.                                    | Aprobado            |
| `GET /api/v1/scooters`                  | Listar los tipos de scooters disponibles.                        | Aprobado            |
| `GET /api/v1/orders`                    | Obtener todos los pedidos realizados por un usuario.             | Fallo menor*        |

---

## **Conclusión**

### **Resultados Generales**
1. **Aplicación Web:**
   - Se identificaron errores menores en la actualización en tiempo real de estados en navegadores antiguos.
2. **Aplicación Móvil:**
   - Todas las funciones y el diseño cumplen con los requisitos.
3. **API:**
   - Funciona correctamente en general, aunque el endpoint `GET /api/v1/orders` devuelve pedidos duplicados en algunos casos.

### **Recomendaciones**
1. Resolver los fallos menores detectados:
   - Mejorar la actualización en tiempo real en navegadores antiguos.
   - Corregir duplicados en la respuesta de `GET /api/v1/orders`.
2. Realizar una ronda de pruebas adicionales tras implementar las correcciones.
3. Automatizar las pruebas de regresión para las funciones críticas.

---

**Equipo QA de Urban Scooter**  

**Enlaces Relacionados:**
- **Lista de Comprobación:** [[Ver Informe Final](https://drive.google.com/drive/folders/1vIOGxGKLC3L0EMAj-a577h6QW6aeUjsR?usp=sharing)](#)

