# Plan de Aseguramiento de la Calidad de Software (SQA Plan)

## 1. Propósito y Alcance
El propósito de este plan es establecer los estándares, procesos y herramientas para garantizar la calidad del software en la aplicación e-commerce (`mi-proyecto-sqa`). Aplica a todo el código fuente del backend (Node.js/Express) y frontend, abarcando pruebas automatizadas, análisis estático y despliegue continuo mediante GitHub Actions y SonarQube Cloud.

## 2. Estándares y Normativas
- **Estándar SQA:** Basado en las dimensiones de mantenibilidad y seguridad de la norma ISO/IEC 25010.
- **Formato de Código:** Convenciones estándar de JavaScript (ESLint).
- **Control de Versiones:** GitFlow simplificado con rama principal protegida `main` y Pull Requests obligatorios.

## 3. Herramientas de SQA
- **Control de Código:** GitHub (`rbarreraz/mi-proyecto-sqa`)
- **CI/CD:** GitHub Actions (Workflows automatizados)
- **Pruebas Automatizadas:** Jest / Supertest
- **Análisis Estático de Código:** SonarQube Cloud
- **Cobertura de Código:** Istanbul / Jest LCOV

## 4. Métricas de Calidad y Umbrales (Quality Gates)
| Métrica | Umbral Mínimo Requerido |
| :--- | :--- |
| Cobertura de Código | ≥ 60% |
| Vulnerabilidades / Bugs Críticos | 0 |
| Duplicación de Código | < 3% |
| Estado de Quality Gate | Passed |

## 5. Gestión de Riesgos
- **Riesgo:** Conflicto entre análisis automático y ejecución por CI/CD.
  - *Mitigación:* Desactivación del "Automatic Analysis" en SonarQube Cloud para canalizar la ejecución vía GitHub Actions.
- **Riesgo:** Inclusión de vulnerabilidades en dependencias y código base.
  - *Mitigación:* Análisis de seguridad automatizado en cada push/PR.
