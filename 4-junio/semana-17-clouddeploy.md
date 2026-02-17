# ☁️ Semana 17 — CloudDeploy

> **Despliegue serverless en AWS con Lambda, API Gateway e Infraestructura como Código**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 27-28 de junio 2026      |
| 🏷️ Categoría       | DevOps & Cloud           |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

CloudDeploy es un proyecto enfocado en desplegar una aplicación serverless en AWS. Usa AWS Lambda para compute, API Gateway para routing HTTP, DynamoDB o RDS para datos, y define toda la infraestructura como código con SAM o Serverless Framework. El resultado: una API deployada en la nube, escalable y de bajo costo.

---

## ✨ Features

### Lambda Functions

- [ ] CRUD de recursos como Lambda functions
- [ ] Layers para dependencias compartidas
- [ ] Handler thin → lógica en módulos separados
- [ ] Manejo de errores con responses estructurados
- [ ] Cold start optimizado

### API Gateway

- [ ] Rutas HTTP mapeadas a Lambdas
- [ ] Autorización por API Key o Lambda authorizer
- [ ] CORS configurado
- [ ] Throttling y quotas

### Infraestructura como Código

- [ ] Template SAM / serverless.yml
- [ ] Variables de entorno por stage (dev/prod)
- [ ] Deploy con un solo comando
- [ ] Output de URLs y recursos creados

### Monitoreo

- [ ] CloudWatch Logs
- [ ] Métricas básicas (invocaciones, errores, duración)
- [ ] Alarmas CloudWatch simples

---

## 🛠️ Stack técnico

| Tecnología      | Propósito                   |
| --------------- | --------------------------- |
| **AWS Lambda**  | Compute serverless          |
| **API Gateway** | HTTP routing                |
| **DynamoDB**    | Base de datos NoSQL         |
| **AWS SAM**     | Infraestructura como código |
| **Python**      | Runtime de Lambda           |
| **CloudWatch**  | Monitoreo y logs            |
| **pytest**      | Testing local               |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                   |
| -------------- | ------------------------------------------- |
| 🌅 9:00-10:30  | Setup: AWS CLI, SAM CLI, cuenta AWS         |
| 🌅 10:30-12:00 | Primera Lambda function + API Gateway       |
| 🌞 12:00-13:00 | DynamoDB table + operaciones CRUD           |
| 🌞 14:00-16:00 | Template SAM completo (todas las funciones) |
| 🌆 16:00-18:00 | Deploy a AWS + testing remoto               |

### Domingo

| Hora           | Actividad                             |
| -------------- | ------------------------------------- |
| 🌅 9:00-10:30  | Authorizer (API Key o Lambda)         |
| 🌅 10:30-12:00 | Variables de entorno + stages         |
| 🌞 13:00-14:30 | CloudWatch: logs y métricas           |
| 🌞 14:30-16:00 | Tests locales con SAM local           |
| 🌆 16:00-17:00 | README con diagrama y URLs del deploy |

---

## ✅ Definición de "hecho"

- [ ] Al menos 3 Lambda functions desplegadas
- [ ] API Gateway con rutas funcionales
- [ ] DynamoDB con operaciones CRUD
- [ ] Template IaC completo y re-desplegable
- [ ] Autorizacion configurada
- [ ] Tests locales
- [ ] README con URLs del deploy y diagrama

---

## 💼 Lo que demuestra al reclutador

| Habilidad  | Evidencia                          |
| ---------- | ---------------------------------- |
| AWS        | Lambda, API Gateway, DynamoDB      |
| Serverless | Arquitectura event-driven          |
| IaC        | SAM templates, deploy reproducible |
| Cloud      | Deploy real en la nube             |
