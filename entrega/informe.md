# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller
_Taller 1 - [BPMN]_

## 👥 Integrantes del equipo
- Valentina Ruiz Torres (valentinaruito@unisabana.edu.co)
- Santiago Soler Prado (santiagosopr@unisabana.edu.co)
- Darek Aljuri Martinez (darekalma@unisabana.edu.co)

## 🧠 Descripción general del trabajo

El objetivo del taller fue modelar un proceso de negocio real del cliente utilizando la notación BPMN, identificando claramente los eventos, actividades, decisiones, actores involucrados y puntos críticos del flujo.

El proceso seleccionado corresponde a la gestión de inventario y venta de repuestos de la empresa ******* ubicada en el 7 de agosto en bogota. Este proceso inicia cuando un cliente solicita un repuesto y finaliza cuando el producto es entregado y facturado, o cuando se gestiona el pedido al proveedor en caso de no contar con disponibilidad.

La actividad se desarrolló mediante el análisis del flujo real descrito por la empresa, identificando las etapas principales, los responsables del proceso y las decisiones que afectan el flujo (por ejemplo, la verificación de disponibilidad del inventario). Posteriormente, el proceso fue estructurado en un modelo BPMN digital que representa gráficamente la secuencia lógica de actividades y puntos de decisión.

## 🔧 Proceso de desarrollo

Para realizar el trabajo, primero analizamos el proceso actual descrito por la empresa:

- Los repuestos se encuentran almacenados en la bodega.
- El cliente solicita un repuesto específico.
- Se verifica si el producto está disponible en inventario (ya sea físicamente en bodega o mediante el conocimiento estimado de “Felipe”).
- Si el producto está disponible, se realiza el cambio o venta y se genera la facturación.
- Si el producto no está disponible, se solicita al proveedor.

Decisiones tomadas

- Se identificó como evento inicial la solicitud del cliente.
- Se modeló como una decisión: ¿El producto está disponible en inventario?
- Se diferenciaron claramente los actores: Cliente, Encargado de inventario/Bodega (Felipe) y Proveedor.
- Se definió como evento final la facturación y entrega del producto o la generación del pedido al proveedor.

Herramientas utilizadas

Se utilizo drwai.io como herramienta de modelado

## 🧩 Análisis del modelo propuesto
Incluya un análisis sobre:
- Cómo se estructura el modelo entregado
    - Evento de inicio: Solicitud del cliente.
    - Tarea: Verificar disponibilidad del repuesto en bodega.
    - Compuerta exclusiva: ¿El producto está disponible?
    - Sí: Realizar cambio/venta → Facturar → Entregar producto → Evento final.
    - No: Solicitar producto al proveedor → Esperar entrega → Notificar al cliente (opcional según alcance) → Evento final.
  
- Cómo representa las necesidades del cliente

El modelo representa adecuadamente las necesidades del cliente porque:
  - Refleja el flujo real descrito por la empresa.
  - Incluye la verificación de inventario como punto clave del proceso.
  - Contempla ambos escenarios posibles: disponibilidad o no del producto.
  - Muestra la interacción con el proveedor cuando es necesario.

El control del inventario depende en parte del conocimiento de una persona “Felipe”, lo cual puede generar riesgos si no existe un sistema formal de control.
  
- Qué supuestos se tomaron

   - Que la solicitud del cliente es clara y contiene la referencia correcta del repuesto
   - Que el proceso de facturación se realiza inmediatamente después de confirmar disponibilidad en el inventario
   - Que el pedido al proveedor se gestiona de manera directa y sin procesos adicionales complejos
   - Que el tiempo de espera por parte del proveedor es indefinido 

## 📈 Diagrama final entregado
<img width="1012" height="707" alt="image" src="https://github.com/user-attachments/assets/b6097e65-a419-49ce-815f-cfa27d550df8" />

## 📋 Tabla de actores, entidades o componentes (si aplica)

| Nombre del elemento     | Tipo              | Descripción                                                             | Responsable        |
| ----------------------- | ----------------- | ----------------------------------------------------------------------- | ------------------ |
| Cliente                 | Actor             | Persona que solicita el diagnóstico o repuesto y realiza el pago        | Cliente            |
| Empleado / Vendedor     | Actor             | Persona que revisa inventario, gestiona solicitudes y coordina la venta | Empresa            |
| Proveedor               | Actor externo     | Empresa que suministra la pieza cuando no está disponible en inventario | Proveedor          |
| Solicitud / Diagnóstico | Evento          | Requerimiento inicial realizado por el cliente                          | Cliente / empleado (dependiendo del caso)           |
| Inventario              | Entidad           | Stock de piezas disponibles en la bodega                                | Empleado / Empresa |
| Pieza o Repuesto        | Entidad           | Producto solicitado por el cliente                                      | Empresa            |
| Solicitud de pieza      | Evento         | Pedido realizado al proveedor cuando no hay existencia                  | Empleado           |
| Factura                 | Evento         | Documento que formaliza la venta del producto                           | Empresa            |
| Recepción de pieza      | Evento            | Confirmación de llegada del producto desde el proveedor                 | Empleado           |

## 🔍 Investigación complementaria
### Tema investigado:
(Ej: Buenas prácticas BPMN, comparación TOGAF vs C4, principios de seguridad STRIDE, etc.)

### Resumen:
Describa en 2–3 párrafos lo investigado, citando fuentes cuando sea necesario. Incluya cómo se relaciona con el taller.

## 📚 Referencias
- [1] Apellido, Nombre. *Título*. Año. URL o DOI.
- [2] Fuente oficial BPMN: https://www.omg.org/spec/BPMN/

---

_Este documento hace parte de la entrega del taller X del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
