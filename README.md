# TP1 - Programación Orientada a Objetos en Java

**Universidad Tecnológica Nacional - Facultad Regional Mendoza**
**Cátedra:** Paradigmas de Programación
**Alumno:** Nicolás Gaitán
**Legajo:** 53369

## Descripción del proyecto

Este proyecto implementa un sistema de gestión de eventos universitarios (charlas, talleres, jornadas, etc.), desarrollado de forma incremental a lo largo de los 4 ejercicios del Trabajo Práctico N°1, aplicando los fundamentos de la Programación Orientada a Objetos en Java: encapsulamiento, asociación, agregación, composición, herencia y polimorfismo.

## Estructura del proyecto

- **EventoUniversitario**: clase principal que modela un evento universitario, con atributos como id, título, costo base y si es gratuito. Mantiene una sala asignada, una lista de actividades y un contador estático de eventos creados.
- **Sala**: representa el espacio físico asignado a un evento (relación de agregación).
- **Actividad** (clase abstracta): modela una actividad dentro de un evento, con id, título y cupo máximo. Define el método final `mostrarIdentificacion()` y el método abstracto `calcularCostoMateriales()`.
- **Charla**: subclase de Actividad. Actividad gratuita (costo de materiales = 0).
- **Taller**: subclase de Actividad. Tiene costo de $5000 si requiere notebook, o $2000 si no la requiere.
- **Estudiante**: representa a un alumno inscripto, con legajo y nombre.
- **Inscripcion**: registra la fecha y el estado de la inscripción de un estudiante a una actividad.
- **App**: clase principal (main) que ejecuta el programa de punta a punta: crea estudiantes, eventos, salas, actividades e inscripciones, y muestra los resultados por consola.

## Ejercicios resueltos

1. **Ejercicio 1**: Implementación básica de la clase `EventoUniversitario`, con constructor de copia y contador estático de instancias.
2. **Ejercicio 2**: Incorporación de relaciones entre clases (Sala, Actividad, Estudiante, Inscripcion) mediante asociación, agregación y composición.
3. **Ejercicio 3**: Incorporación de herencia y polimorfismo: `Actividad` pasa a ser clase abstracta, con las subclases concretas `Charla` y `Taller`, cada una con su propio cálculo de costo.
4. **Ejercicio 4**: Elaboración de un mapa de memoria de ejecución (archivo `graficoEjercicio4`, incluido en este repositorio) que representa gráficamente los objetos creados en memoria y sus relaciones durante la ejecución del `main`.

## Cómo ejecutar el proyecto

1. Clonar el repositorio:
   ```
   git clone https://github.com/nicolasgaitan063/PP_TP1_53369.git
   ```
2. Abrir la carpeta del proyecto con **IntelliJ IDEA**.
3. Esperar a que el IDE indexe el proyecto.
4. Ejecutar la clase `App` (botón derecho sobre el archivo > Run 'App.main()').
5. La salida del programa se mostrará por consola, mostrando los eventos creados, sus actividades, las inscripciones de estudiantes y el total de eventos.

## Archivos incluidos en este repositorio

- Código fuente completo (`src/`), listo para clonar y ejecutar desde IntelliJ IDEA.
- `graficoEjercicio4`: mapa de memoria de ejecución solicitado en el Ejercicio 4.
- `capturaPrueba`: captura de la salida por consola de una ejecución del programa.
- Este archivo `README.md`.
