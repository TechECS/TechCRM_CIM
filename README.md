# TechCRM_CIM - Interfaz de UI y Desarrollo Interno

**TechCRM_CIM** es una aplicación front-end basada puramente en interfaz de usuario (**UI**), desarrollada íntegramente mediante código HTML, CSS y JavaScript estructurado en un único archivo. No contiene lógica de servidor real ni bases de datos de backend; toda la simulación de datos, árboles de servicio, motores de reglas, orquestador de aprovisionamiento de servicios SaaS y consolas interactivas se ejecutan directamente en el lado del cliente (navegador).

* **Autor:** Adan Nahir Abad Mora (nahirnewlife@gmail.com)
* **Organización:** TechECS_EU
* **Propósito:** Entorno de pruebas, prototipado y desarrollo interno de flujos UI para la gestión de clientes, cuentas corporativas y aprovisionamiento de servicios en la nube (SaaS).

---

## 🖥️ Funcionalidades Implementadas en el Código (Frontend UI)

El código incluye las siguientes capacidades simuladas a nivel de interfaz:

### 1. Sistema de Ventanas y Pestañas Múltiples
* **Gestión de Fichas Abiertas:** Permite abrir, alternar y cerrar diferentes sesiones de clientes de forma concurrente desde el panel lateral izquierdo (*Abrir Ventanas*).
* **Control de Modos:** Cambio dinámico entre la vista global de búsqueda, la página central de interacción del cliente, el configurador de órdenes de trabajo y la pasarela de contratos.
* **Tema Claro / Oscuro:** Conmutador de estilos CSS incorporado para alternar entre la paleta clásica y un modo oscuro.

### 2. Módulo de Búsqueda y Contexto
* **Filtrado Local de Clientes:** Búsqueda instantánea dentro de una base de datos local en memoria por NIF, teléfono, provincia o ID de dirección.
* **Banner de Contexto Dinámico:** Actualización en tiempo real de la barra superior con los datos principales del cliente seleccionado (estado, deudas, segmento y tecnología de servicio).

### 3. Árbol Jerárquico de Servicios SaaS y Fichas Técnicas
* **Renderizado de Árbol DOM:** Estructura interactiva en árbol (carpetas y archivos) para representar productos principales, módulos CRM, integraciones, seguridad y accesos.
* **Inspección de Componentes:** Al hacer clic en cualquier nodo del árbol, se carga una ficha técnica de solo lectura con parámetros de instancia, consumo de tenants, límites y dependencias.

### 4. Configurador y Órdenes de Trabajo (OT)
* **Gestión de Líneas de Pedido:** Interfaz para tramitar altas, modificaciones, traslados o bajas de servicios SaaS con cálculo de cuotas recurrentes e impuestos.
* **Validador de Reglas de Negocio (`Cheq.`):** Funcionalidad de código que evalúa dependencias entre servicios, límites de cantidad y campos obligatorios antes de permitir el avance.
* **Asistente de Contratación (2 Pasos):** Vistas dedicadas para capturar métodos de aceptación (firma digital, SMS), datos de facturación e IBAN.

### 5. Orquestador de Provisioning y Consola de Diagnóstico
* **Simulación de Tareas Asíncronas:** Ejecución paso a paso simulada mediante `setTimeout` para los diferentes subsistemas (CRM, Catalog, Identity, Storage, Eventos, Billing, Notifier) con control de estados (*Pendiente, En curso, OK, Error, Excepción*).
* **Consola Interactiva Emulada:** Terminal integrada para las instancias de servicio con soporte para comandos simulados (`help`, `ps`, `logs`, `env`, `curl`, `restart`, `mc`, `kafka-topics`, `webhookctl`).
* **Flujo de Rollback / Anulación:** Generación automática de tareas obligatorias de desaprovisionamiento si se decide anular una orden en curso.

### 6. Módulos de Facturación, Jerarquías y Soporte
* **Listados Tabulares de Facturas:** Consulta de historiales de cobro, desglose de impuestos y estados de pago.
* **Jerarquía de Cuentas:** Interfaz para crear subcuentas de facturación y reasignar servicios contratados entre ellas.
* **Gestión de Tickets y Averías:** Creación de incidencias, cálculo dinámico de tiempos de SLA restante y ejecución de diagnósticos de red simulados.
* 
