# Manual Técnico de la Arquitectura CI/CD

## 1. Arquitectura del Pipeline SQA
El flujo CI/CD está implementado mediante **GitHub Actions** en el archivo `.github/workflows/sqa-pipeline.yml` y consta de 4 etapas automatizadas:

1. **Build:** Descarga del código fuente (`actions/checkout@v4`), configuración de Node.js v20 e instalación de dependencias con `npm install`.
2. **Test:** Ejecución del suite de pruebas con Jest y generación del reporte de cobertura `coverage/lcov.info`.
3. **Analyze:** Escaneo estático de código fuente con `SonarSource/sonarqube-scan-action@v3` utilizando la variable de entorno `SONAR_TOKEN`.
4. **Report:** Transmisión de métricas y evaluación de políticas de calidad (Quality Gate) en SonarQube Cloud.

## 2. Archivos Clave de Configuración
- `.github/workflows/sqa-pipeline.yml`: Definición del flujo CI/CD.
- `sonar-project.properties`: Propiedades del proyecto en SonarQube (Organization, ProjectKey y rutas de exclusión/cobertura).

## 3. Guía de Mantenimiento
- Para añadir nuevas pruebas, agregue archivos con extensión `.test.js` o `.spec.js`.
- Para actualizar secretos, diríjase en GitHub a **Settings -> Secrets and variables -> Actions**.
