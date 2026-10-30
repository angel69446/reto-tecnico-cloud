# Reto Técnico — Ingeniero Cloud

Este repositorio contiene la resolución del reto técnico para la posición de **Ingeniero Cloud**.

## Contenido del Repositorio

* **`Reto_Tecnico_Ingeniero_Cloud_Angel_Ortega.pdf`**: Documento principal con las respuestas teóricas y la justificación de diseño del caso práctico.
* **`arquitectura_cloud_native_azure.drawio`**: Archivo editable generado en [diagrams.net](https://app.diagrams.net/) con las dos vistas de arquitectura (Topología de Red y Flujo Operativo CI/CD + IaC).
* **`diagrama_1_arquitectura_azure.png`**: Vista general de la infraestructura y aislamiento de red (VNet).
* **`diagrama_2_flujo_operativo.png`**: Flujo de peticiones en tiempo de ejecución y pipeline de despliegue automatizado.

---

## Resumen de la Arquitectura Propuesta (Microsoft Azure)

| Capa | Servicio Seleccionado | Función Principal |
| :--- | :--- | :--- |
| **Entrada y Seguridad** | Azure Front Door + Azure WAF | Balanceo global HTTPS, CDN y protección OWASP / DDoS. |
| **Frontend** | Azure App Service | Hospedaje PaaS para la aplicación web con autoescalado. |
| **Backend** | Azure Container Apps / AKS | Microservicios en contenedores Docker dentro de subred privada. |
| **Base de Datos** | Azure Database for PostgreSQL / SQL | Base de datos relacional Multi-AZ con acceso vía Private Endpoint. |
| **Almacenamiento** | Azure Blob Storage | Gestión de imágenes y contenido estático (acceso público bloqueado). |
| **Seguridad y Monitoreo** | Entra ID, Key Vault y Azure Monitor | Identidades administradas (Managed Identity), secretos y observabilidad. |

---
**Autor:** Angel Ortega
