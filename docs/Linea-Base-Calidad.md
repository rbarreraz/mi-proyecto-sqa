# Línea Base de Calidad (Diagnóstico Inicial)

## 1. Resumen Ejecutivo
Se realizó el análisis inicial del repositorio `mi-proyecto-sqa` utilizando SonarQube Cloud e integración continua con GitHub Actions. El análisis identificó el estado de calidad del código base reutilizado antes de aplicar refactorizaciones y correcciones.

## 2. Métricas Iniciales Registradas en SonarQube Cloud

| Métrica | Valor Inicial Registrado | Estado / Observación |
| :--- | :--- | :--- |
| **Líneas de Código (LOC)** | 2.8k | Evaluado |
| **Quality Gate Status** | **Failed** (1 condición fallida) | Rechazado |
| **Security Rating** | **E** | Crítico |
| **Security Issues** | 8 hallazgos (1 Alto, 6 Medios, 1 Bajo) | Alta prioridad de refactorización |
| **Code Smells / Issues Totales** | 10 | Mantenibilidad a mejorar |
| **Duplicación de Código** | 0.0% | Cumple umbral |
| **Cobertura de Código** | 0.0% | Requiere generación de reporte LCOV |

## 3. Hallazgos Principales
- **Security Rating E:** El código base reutilizado cuenta con 8 vulnerabilidades de seguridad que impiden la aprobación del Quality Gate.
- **Falta de Reporte LCOV:** La cobertura de código figura en 0% debido a la falta de exportación explícita del archivo `lcov.info` en la primera corrida del pipeline.
