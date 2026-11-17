# CicloHub

![UMU](https://img.shields.io/badge/Universidad_de_Murcia-MISum-red?style=flat-square)
![Estado](https://img.shields.io/badge/Estado-Inicialización_/_MVP-blue?style=flat-square)
![Arquitectura](https://img.shields.io/badge/Arquitectura-Microservicios_%7C_DDD_%7C_Hexagonal-informational?style=flat-square)
![Stack](https://img.shields.io/badge/Stack-NestJS_%7C_React_%7C_Next.js_%7C_React_Native-success?style=flat-square)

Plataforma **Software as a Service (SaaS)** para la gestión integral de sistemas de préstamo de bicicletas en municipios, barrios y entidades urbanísticas, orientada a fomentar la movilidad sostenible.

> **Contexto Académico:** Proyecto común desarrollado en el marco del **Máster Universitario en Ingeniería del Software (MISum)** de la Facultad de Informática de la **Universidad de Murcia**.

---

## Descripción del Proyecto

**CicloHub** permite a distintos organismos gestores (Ayuntamientos, entidades urbanísticas, etc.) administrar de forma totalmente independiente y aislada (*multi-tenant*) sus estaciones de préstamo, flota de bicicletas, usuarios, alquileres, reservas e incidencias de mantenimiento bajo diferentes modalidades de suscripción (**Plan Básico** y **Plan Premium**).

### Actores del Sistema

* **Gestores:** Administran la instancia de su municipio (altas/bajas de estaciones, bicicletas y operarios, validación de solicitudes de alta de usuarios, reactivación de cuentas bloqueadas y supervisión de incidencias).
* **Usuarios:** Consultan estaciones cercanas, reservan bicicletas, realizan alquileres respetando los límites diarios/semanales, reportan desperfectos y consultan sus estadísticas de uso.
* **Operarios:** Gestionan el mantenimiento preventivo y correctivo, atienden incidencias en bicicletas o puntos de anclaje y realizan el rebalanceo/traslado de bicicletas entre estaciones.

### Requisitos Clave y Calidad (NFR)

* **Disponibilidad y Accesibilidad:** Operación 24x7 y conformidad con el nivel **AA de las WCAG 2.2**.
* **Internacionalización:** Soporte multi-idioma desde la primera versión (Español e Inglés).
* **Seguridad y Privacidad:** Desarrollo alineado con **OWASP Top 10**, autenticación mediante **OAuth2 / JWT** y cumplimiento normativo de **LOPD** y **GDPR**.

---

## Arquitectura y Stack Tecnológico Previsto

El desarrollo del Producto Mínimo Viable (MVP) sigue un enfoque evolutivo e incremental:

* **Backend:**
  * **Runtime & Framework:** Node.js con NestJS.
  * **Diseño y Arquitectura:** Arquitectura Limpia / Hexagonal, Domain-Driven Design (DDD), microservicios orientados a eventos y aplicación de patrones **CQRS** y **Event Sourcing**.
  * **APIs:** API Gateway bajo especificación **OpenAPI** y módulo de consultas mediante **GraphQL**.
* **Frontend & Movilidad:**
  * **Web:** Evolución desde arquitectura MVC hacia componentes con **React** y **Next.js**, incorporando capacidades de **PWA** (*Progressive Web App*).
  * **Móvil:** Aplicación híbrida desarrollada con **React Native** (iOS y Android).
* **Arquitectura de Datos:**
  * Persistencia políglota combinando bases de datos **Relacionales** y **NoSQL** adaptadas a los patrones de acceso y consistencia del dominio.
* **Calidad y Pruebas (QA):**
  * **Análisis estático:** ESLint (guía de estilo de Airbnb) y SonarQube.
  * **Testing:** Jest (pruebas unitarias de caja blanca), Stryker (pruebas de mutación), `jest-dom`, Supertest + ficheros `.rest`, Cypress (E2E) y JMeter (rendimiento / métricas APDEX).
* **Prácticas Continuas (DevOps):**
  * Automatización mediante pipelines de Integración Continua (CI) y Despliegue Continuo (CD) en entorno Cloud.

---

## Asignaturas Integradoras del Proyecto

Este repositorio centraliza los artefactos, documentación y código derivados de las asignaturas obligatorias del máster:

| Asignatura | Enfoque en CicloHub |
| :--- | :--- |
| **Gestión Ágil de Proyectos** | Definición de visión, *roadmap*, especificación del MVP, planificación de iteraciones (Scrum/Lean) y gestión de riesgos. |
| **Desarrollo Full-Stack** | Implementación del MVP (Backend NestJS, Microservicios, APIs, Frontend Web/PWA y App React Native). |
| **Arquitectura de Datos** | Modelado conceptual, análisis de patrones de acceso y despliegue de persistencia híbrida (SQL + NoSQL). |
| **Control de Calidad y Pruebas** | Plan de pruebas ágil, análisis con SonarQube, testing unitario, mutación, integración, E2E, rendimiento y regresión. |
| **Prácticas Continuas** | Diseño e implementación de pipelines de CI/CD y arquitectura de despliegue y monitorización en la nube. |

---

## Estructura Inicial del Repositorio

```text
ciclohub/
├── .github/                # Workflows de CI/CD y plantillas del repositorio
├── docs/                   # Documentación de arquitectura, modelo de datos, planes de prueba y gestión ágil
├── request/                # Ficheros .rest para pruebas manuales de endpoints
├── services/               # Microservicios del backend (NestJS)
├── frontend/               # Aplicación web (MVC -> Next.js / PWA)
├── mobile/                 # Aplicación móvil (React Native)
└── README.md               # Documentación principal del proyecto
```

---

## Primeros Pasos (Setup Inicial)

*Repositorio recién inicializado. Las instrucciones de despliegue local con Docker/Node y configuración de variables de entorno se añadirán conforme avance la Iteración 1.*

---

## Equipo de Desarrollo

* **Francisco José Gil Gil** *<fj.gilgil@um.es>*
* **Jiahui Lin** *<jiahui.lin@um.es>*
* **Washington Jesús Sánchez Pardo** *<wjesus.sanchez@um.es>*
* **Inmaculada Álvarez Donaire** *<inmaculada.alvarez@um.es>*
