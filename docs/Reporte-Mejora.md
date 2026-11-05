# Reporte de Mejora de Calidad (Antes vs. Después)

## 1. Comparativa de Métricas de Calidad

| Métrica de Calidad | Línea Base (Antes) | Estado Esperado (Después) | Impacto / Mejora |
| :--- | :--- | :--- | :--- |
| **Quality Gate Status** | Failed | Passed | Aprobación automática del pipeline |
| **Security Rating** | E | A / B | Eliminación de vulnerabilidades |
| **Security Issues** | 8 hallazgos | 0 - 2 hallazgos | Código más seguro |
| **Issues Totales** | 10 | < 3 | Optimización y mantenibilidad |
| **Cobertura de Código** | 0.0% | ≥ 60.0% | Incremento de confiabilidad |

## 2. Acciones de Refactorización y Configuración
1. Desactivación de *Automatic Analysis* en SonarQube Cloud para eliminar conflictos de integración.
2. Configuración de comandos de exportación LCOV en `.github/workflows/sqa-pipeline.yml`.
3. Establecimiento de reglas de protección en la rama `main` de GitHub.
