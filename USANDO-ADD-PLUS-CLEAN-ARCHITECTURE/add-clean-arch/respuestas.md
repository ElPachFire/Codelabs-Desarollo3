# Respuestas del Codelab: ADD y Clean Architecture

---

## 1. ¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?

ADD (Attribute-Driven Design) es un método sistemático para diseñar arquitecturas de software basado en los atributos de calidad requeridos por el sistema (como rendimiento, seguridad, disponibilidad, etc.). Su propósito principal es garantizar que la arquitectura soporte explícitamente los requisitos funcionales y no funcionales desde el principio del diseño.

---

## 2. ¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?

ADD proporciona un enfoque estructurado para identificar y priorizar atributos de calidad que deben influir en las decisiones arquitectónicas. Clean Architecture, por otro lado, ofrece una organización de código basada en capas y principios de separación de responsabilidades. Usados juntos, ADD identifica las necesidades y Clean Architecture proporciona una forma de estructurar el sistema para satisfacerlas.

---

## 3. ¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?

1. Seleccionar el módulo a diseñar.
2. Identificar los requerimientos (funcionales y atributos de calidad).
3. Elegir tácticas y patrones arquitectónicos.
4. Definir estructuras y responsabilidades.
5. Documentar vistas arquitectónicas.
6. Validar decisiones.
7. Repetir de forma iterativa para cada módulo.

---

## 4. ¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?

Los atributos de calidad se identifican a través de análisis de requerimientos, entrevistas con stakeholders y escenarios de calidad. Son importantes porque definen cómo debe comportarse el sistema más allá de su funcionalidad, asegurando que cumpla con criterios como escalabilidad, seguridad o rendimiento.

---

## 5. ¿Por qué Clean Architecture complementa ADD en la implementación de una solución?

Porque Clean Architecture impone una separación clara entre capas (como dominio, aplicación, infraestructura) y depende de reglas de dependencia unidireccionales. Esto permite implementar las decisiones arquitectónicas tomadas con ADD de forma estructurada, flexible y mantenible.

---

## 6. ¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?

- Independencia del framework
- Aislamiento del dominio
- Bajo acoplamiento y alta cohesión
- Separación de responsabilidades
- Posibilidad de prueba independiente
- Cumplimiento de los atributos de calidad definidos en ADD

---

## 7. ¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?

ADD fuerza al arquitecto a alinear sus decisiones con atributos de calidad directamente relacionados con los objetivos del negocio, priorizando los que más impacto tienen y eligiendo estructuras, patrones y tecnologías que los satisfagan.

---

## 8. ¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?

- Claridad en la estructura del sistema
- Escalabilidad y mantenibilidad
- Alineación con objetivos de negocio
- Reducción del riesgo técnico
- Flexibilidad en la implementación y despliegue de servicios
- Alta cohesión por servicio y bajo acoplamiento entre ellos

---

## 9. ¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?

Mediante tácticas arquitectónicas específicas, validación con escenarios de calidad, revisiones arquitectónicas, pruebas no funcionales y retroalimentación continua durante el desarrollo iterativo.

---

## 10. ¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?

- **ATAM (Architecture Tradeoff Analysis Method)** para evaluar decisiones arquitectónicas.
- **Modelado con C4** para visualizar componentes.
- **ADR (Architecture Decision Records)** para documentar decisiones clave.
- **Herramientas de análisis estático de código**, pruebas de estrés y carga.
- **Revisiones de arquitectura** y prototipos arquitectónicos.
