# Respuestas del Codelab: Clean Architecture en Microservicios con Spring Boot

---

## 1. ¿Cuál es el propósito principal de Clean Architecture en el desarrollo de software?

El propósito principal de Clean Architecture es lograr una separación clara de responsabilidades dentro del sistema, promoviendo independencia entre la lógica de negocio, la infraestructura y los frameworks. Esto facilita el mantenimiento, la prueba y la evolución del software sin afectar otras partes del sistema.

---

## 2. ¿Qué beneficios aporta Clean Architecture a un microservicio en Spring Boot?

- Facilita pruebas unitarias al aislar la lógica de negocio.
- Reduce el acoplamiento con tecnologías específicas (como Spring Data o frameworks de base de datos).
- Permite reemplazar fácilmente componentes externos sin modificar el dominio.
- Mejora la organización del código.
- Facilita la escalabilidad y mantenimiento del servicio.

---

## 3. ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?

1. **Entidad/Dominio**: contiene las reglas de negocio más generales y modelos puros.
2. **Casos de Uso (Aplicación)**: coordina la lógica del sistema según las reglas del dominio.
3. **Infraestructura**: tecnologías específicas como bases de datos, servicios externos, frameworks, etc.
4. **Presentación**: entrada (controllers, servicios REST) y salida (repositorios, gateways).


---

## 4. ¿Por qué se recomienda desacoplar la lógica de negocio de la infraestructura en un microservicio?

Porque la infraestructura puede cambiar (por ejemplo, pasar de PostgreSQL a MongoDB), pero la lógica de negocio debería permanecer estable. Este desacoplamiento permite modificar o reemplazar componentes técnicos sin afectar el corazón del sistema, asegurando mayor flexibilidad y robustez.

---

## 5. ¿Cuál es el rol de la capa de aplicación y qué tipo de lógica debería contener?

La capa de aplicación orquesta los flujos de la lógica de negocio mediante los casos de uso. No contiene lógica de negocio compleja, sino la coordinación de las entidades, la interacción con interfaces (repositorios, servicios externos) y la implementación de políticas del sistema.

---

## 6. ¿Qué diferencia hay entre un UseCase y un Service en Clean Architecture?

- **UseCase**: representa una acción o interacción específica del usuario o sistema, ejecutando la lógica necesaria para cumplir con ese objetivo.
- **Service (típico en Spring)**: suele usarse como contenedor de lógica de negocio, pero en Clean Architecture el término "Service" se reemplaza por `UseCase` para evitar mezclar responsabilidades y mantener el enfoque en tareas concretas.

---

## 7. ¿Por qué se recomienda definir Repositories como interfaces en la capa de dominio en lugar de usar directamente JpaRepository?

Porque así se mantiene el dominio independiente de cualquier tecnología o framework. Definir interfaces en el dominio permite que los detalles de implementación (como `JpaRepository`) vivan en la infraestructura, manteniendo el bajo acoplamiento y facilitando pruebas, simulaciones y migraciones tecnológicas.

---

## 8. ¿Cómo se implementa un UseCase en un microservicio con Spring Boot y qué ventajas tiene?

Un UseCase se implementa como una clase de servicio que ejecuta una operación específica, recibiendo interfaces (como `UserRepository`) y llamando a métodos del dominio. Se inyecta en controladores sin necesidad de conocer detalles de infraestructura.

**Ventajas:**
- Claridad en el flujo del sistema.
- Fácil de probar (sin necesidad de Spring Boot ni BD).
- Reutilizable desde otros puntos (REST, eventos, cron, etc.).
- Independencia de tecnología.

---

## 9. ¿Qué problemas podrían surgir si no aplicamos Clean Architecture en un proyecto de microservicios?

- Acoplamiento excesivo entre capas (cambios en la BD rompen la lógica).
- Dificultad para probar la lógica sin contexto completo del microservicio.
- Código desorganizado y difícil de mantener.
- Dependencia fuerte de frameworks.
- Menor reutilización y mayor duplicación.

---

## 10. ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad en un entorno basado en microservicios?

- Permite añadir nuevas funcionalidades o refactorizar sin romper lo existente.
- Aísla cambios tecnológicos (por ejemplo, cambiar motor de base de datos o sistema de colas).
- Mejora la comprensión del sistema gracias a su estructura clara.
- Facilita la evolución independiente de cada microservicio.
- Reduce la deuda técnica a largo plazo.

