# 🚀 Pipeline CI/CD con Aseguramiento de Calidad Integrado (SQA)

[![CI/CD Pipeline SQA](https://github.com/rbarreraz/mi-proyecto-sqa/actions/workflows/sqa-pipeline.yml/badge.svg)](https://github.com/rbarreraz/mi-proyecto-sqa/actions)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=rbarreraz_mi-proyecto-sqa&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=rbarreraz_mi-proyecto-sqa)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=rbarreraz_mi-proyecto-sqa&metric=coverage)](https://sonarcloud.io/summary/new_code?id=rbarreraz_mi-proyecto-sqa)

## 📌 Descripción del Proyecto
Este repositorio alberga la aplicación backend/frontend `mi-proyecto-sqa` integrada con un pipeline de **Integración Continua (CI/CD)** en **GitHub Actions** y **SonarQube Cloud**. El objetivo del proyecto es aplicar controles automatizados de aseguramiento de calidad de software (SQA) que garanticen la ejecucion de pruebas, analisis estatico, medicion de cobertura y cumplimiento de Quality Gates antes de integrar codigo a la rama principal.

---

## 🛠️ Stack Tecnológico
- **Lenguaje / Entorno:** JavaScript / Node.js
- **Framework Web:** Express.js
- **Control de Versiones & CI/CD:** Git, GitHub, GitHub Actions
- **Análisis Estático & SQA:** SonarQube Cloud, ESLint
- **Pruebas Automatizadas:** Jest, Supertest
- **Reporte de Cobertura:** LCOV / Istanbul

---

## ⚙️ Arquitectura del Pipeline CI/CD
El pipeline esta definido en `.github/workflows/sqa-pipeline.yml` y ejecuta 4 etapas automatizadas en cada push o Pull Request:

1. **Build:** Instalacion limpia de dependencias mediante `npm install`.
2. **Test:** Ejecucion de pruebas automatizadas con Jest y generacion del reporte de cobertura `lcov.info`.
3. **Analyze:** Escaneo estatico de codigo fuente con SonarQube Cloud.
4. **Report:** Evaluacion de politicas de calidad (Quality Gate) y reporte del estado en el commit/PR.

---

## 🛡️ Protección de Ramas y GitFlow
- La rama `main` esta protegida.
- Es obligatorio abrir un **Pull Request (PR)** para cualquier modificacion.
- Se requiere que el pipeline CI/CD finalice en **exitoso (checks en verde)** para permitir el merge.

---

## 📂 Documentación Oficial SQA
Toda la documentacion del proyecto se encuentra en la carpeta `/docs`:
- [`SQA-Plan.md`](./docs/SQA-Plan.md): Plan de Aseguramiento de la Calidad.
- [`Linea-Base-Calidad.md`](./docs/Linea-Base-Calidad.md): Diagnostico inicial antes de las mejoras.
- [`Matriz-Pruebas.md`](./docs/Matriz-Pruebas.md): Matriz de casos de prueba diseñados.
- [`Reporte-Mejora.md`](./docs/Reporte-Mejora.md): Comparativa de metricas antes vs. despues.
- [`Manual-Tecnico.md`](./docs/Manual-Tecnico.md): Guia tecnica de arquitectura y mantenimiento del pipeline.

---

## 💻 Instrucciones de Instalación Local

```bash
# 1. Clonar el repositorio
git clone [https://github.com/rbarreraz/mi-proyecto-sqa.git](https://github.com/rbarreraz/mi-proyecto-sqa.git)

# 2. Entrar al directorio
cd mi-proyecto-sqa

# 3. Instalar dependencias
npm install

# 4. Ejecutar pruebas con reporte de cobertura
npm test -- --coverage
