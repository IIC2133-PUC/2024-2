# IIC2133 - Estructuras de Datos y Algoritmos

## 2024-2

Bienvenido al sitio web del curso de Estructuras de Datos y Algoritmos. En esta página podrás encontrar la información administrativa del curso. En el repositorio podrás encontrar código ya preparado por tus ayudantes, junto con los eventuales enunciados de las tareas y las diapositivas de clases.

## Tabla de contenidos

- [Organización de este repositorio y syllabus](#organización-de-este-repositorio-y-syllabus)
- [Equipo](#equipo)
  - [Profesores](#profesores)
  - [Ayudantes](#ayudantes)
- [Evaluaciones](#evaluaciones)
  - [Evaluaciones Escritas](#evaluaciones-escritas)
  - [Tareas](#tareas)
- [Política de Atrasos](#política-de-atrasos)
- [Política de integridad académica](#política-de-integridad-académica)
  - [Consideraciones Previas](#consideraciones-previas)
  - [Declaración de integridad académica](#declaración-de-integridad-académica)

## Organización de este repositorio y syllabus

- Las fechas y ponderaciones de las evaluaciones estarán disponibles en la [sección de evaluaciones](#evaluaciones). Otro material administrativo, como el programa, se encontrará en la carpeta [Administrativo](./Administrativo).
- Las clases serán subidas a [Clases](./Clases), y las ayudantías a [Ayudantías](./Ayudantías), los enunciados de las tareas a [Tareas](./Tareas), y las pautas de las interrogaciones a [Pautas](./Pautas).
- Está subido y se podrá subir a lo largo del semestre [Material Complementario](#material-complementario), además de [Guías](./Guías), [Libros](./Libros), y [Código](./Código) de apoyo.
- Podrán además encontrar material de semestres anteriores en [Semestres Anteriores](./Semestres%20Anteriores) y en [Pautas Anteriores](./Pautas%20Anteriores).
- El medio oficial para preguntas del curso es [GitHub Discussions](https://github.com/IIC2133-PUC/2024-1/discussions). Puedes ahí escribir preguntas de materia, tareas, u otras cosas relacionadas al curso.

## Equipo

### Profesores

| Nombre           | Sección | Email                 |
| :--------------- | :------ | :-------------------- |
|Yadran Eterovic   | 1       | yadran@uc.cl |
| Mario Droguett   | 2       | mario@uc.cl           |
| Eduardo Bustos   | 3       | eb@uc.cl              |


### Ayudantes
| Rol                  | Nombre                           | Correo                   |
|----------------------|----------------------------------|--------------------------|
| Coordinadora         | Cata Alamos                       |  catalina.alamos@uc.cl          |
| Coordinadora Cátedra | Isabella Cherubini               | isabella.cherubini@uc.cl    |
| Coordinador Tareas   | Sebastián Carrasco                   | sebacarrascop@uc.cl      |
| Bienestar            |    Rodrigo Jesús De La Fuente De La Fuente | rodridelafuente@uc.cl           |
|                      | Antonia Cáceres                  | antoniacaceres@uc.cl     |
|                      | Bárbara Alfaro                   | bcalfaro@uc.cl      
## Evaluaciones

El curso consta de una parte teórica, evaluada mediante evaluaciones escritas (interrogaciones), y una parte práctica, evaluada mediante tareas de programación en C.

### Evaluaciones Escritas

Habrá 3 interrogaciones, donde se evaluarán los aspectos más teóricos del contenido.

| Evaluación | Fecha                     |
| :--------- | :------------------------ |
| I1         | miércoles de 2 octubre, 17:30 |
| I2         | lunes 18 de noviembre, 17:30 |
| Examen     | miércoles 11 de diciembre, 8:20|

### Tareas

Habrá 4 tareas de programación en C, donde deberán resolver un problema complejo y analizarlo en un informe escrito.

| Evaluación | Fecha Publicación     | Fecha Entrega         |
| :--------- | :-------------------- | :-------------------- |
| Tarea 0    | lunes 12 de agosto    | lunes 26 de agosto |
| Tarea 1    | lunes 2 de septiembre | jueves 26 de septiembre |
| Tarea 2    | lunes 14 de octubre   | lunes 28 de octubre    |
| Tarea 3    | lunes 4 de noviembre  | lunes 25 de noviembre   |

La nota final del curso se calcula de la siguiente manera:

```c++
double nota_final() {
  /* La nota de cada tarea */
  double T0, T1, T2, T3;
  /* La nota de cada interrogación*/
  double I1, I2, Examen;

  /* Promedio de tareas */
  double NT = min(0.20 * T0 + 0.30 * T1 + 0.25 * T2 + 0.25 * T3, 7.0);
  /* Promedio de interrogaciones */
  double NI = min(0.3 * I1 + 0.3 * I2 +  0.4 * Examen, 7.0);

  /* Nota final */
  double NF = (NT + NI) / 2;

  /* Es necesario tener sobre 3.7 en las evaluaciones escritas y las tareas por separado para aprobar el curso */
  if (NI < 3.7 || NT < 3.7) {
    return min(3.9, NF);
  } else {
    return min(NF, 7);
  }
}
```

## Política de Cupones y Atrasos

**Luego del fin del plazo oficial de la tarea, no se asegura el apoyo del equipo docente para resolver dudas**.

Se puede optar por **2 cupones de días adicionales de plazo** en el semestre, y
en la T0 no se podrá usar cupones.
No se aplicarán automáticamente, deben ser solicitados en un formulario que se enviará luego de la publicación de la tarea, cuyo plazo de edición, es el plaxo máximo que se puede optar.

Además, existe un **descuento incremental** por atraso a la nota inicial obtenida, desde la hora de entrega más los días de los cupones empleados, de la siguiente manera:

- 5 décimas menos si se entrega con a lo más 3 horas de atraso.
- 2 puntos menos si se entrega con a lo más 24 horas de atraso.

Si la tarea se entrega con más de 24 horas de atraso, la nota final será 1.
La nota final de la tarea sería $T_f = \max(1, T_i - d)$, donde $T_i$ es la nota inicial obtenida sin considerar atraso.
El descuento es directo a la nota obtenida, y no a la nota máxima.
Por ejemplo, si se obtiene 6 en la tarea como nota inicial, pero con atraso de 7 horas (entre 3 y 24), la nota final sería $6 - 2 = 4$.

> Estas comodidades están en mente para que puedan planificar bien su trabajo a lo largo del semestre,
> y las fechas de las tareas buscan tener el mejor balance de carga a lo largo del semestre.
>
> Por esto, recomendamos planificar bien el uso de cupones, tener en mente la política de atraso,
> leer los enunciados lo antes posible, y realizar las preguntas con anticipación.
>
> No se dará plazo adicional, a menos en casos excepcionales.
> **Cualquier cosa contactar a coordinación o a bienestar.**

## Política de integridad académica

Este curso se adscribe a la política de integridad académica de la Escuela de Ingeniería y el Departamento de Computación.

### Consideraciones Previas

- **Uso de IAs**: El uso de herramientas que utilicen modelos de inteligencias artificiales no esta sancionado, pero no esta recomendado más allá de sintaxis de código o detalles pequeños. Normalmente el uso de estas herramientas genera código que no resuelve correctamente la tarea y requiere tiempo adicional de depuración.
  - Además, en caso de utilizar **se debe citar**. En caso de no citar el uso de las herramientas podria detectarse similitud entre tareas de distintos alumnos y se considerara un caso de copia.
- **Uso de código de terceros**: Se puede utilizar codigo extraido desde la internet siempre y cuando sea citado correctamente en la tarea. En caso de no citar el uso de las herramientas podria detectarse similitud entre tareas de distintos alumnos y se considerara un caso de copia.
- **Compartir ideas o algoritmos utiles**: El curso permite compartir ideas sobre como resolver una tarea, pero no se permite compartir código. Solo ideas.

### Declaración de integridad académica

Los alumnos de la Escuela de Ingeniería de la Pontificia Universidad Católica de Chile deben mantener un comportamiento acorde a la Declaración de Principios de la Universidad. En particular, se espera que **mantengan altos estándares de honestidad académica**. Cualquier acto deshonesto o fraude académico está prohibido; los alumnos que incurran en este tipo de acciones se exponen a un Procedimiento Sumario. Es responsabilidad de cada alumno conocer y respetar el documento sobre Integridad Académica publicado por la Dirección de Docencia de la Escuela de Ingeniería (disponible en SIDING).

Específicamente, para los cursos del Departamento de Ciencia de la Computación, rige obligatoriamente la siguiente política de integridad académica. Todo trabajo presentado por un alumno para los efectos de la evaluación de un curso debe ser hecho individualmente por el alumno, sin apoyo en material de terceros. Por “trabajo” se entiende en general las interrogaciones escritas, las tareas de programación u otras, los trabajos de laboratorio, los proyectos, el examen, entre otros.

**En particular, si un alumno copia un trabajo, o si a un alumno se le prueba que compró o intentó comprar un trabajo, obtendrá nota final 1.1 en el curso y se solicitará a la Dirección de Docencia de la Escuela de Ingeniería que no le permita retirar el curso de la carga académica semestral.**

Por “copia” se entiende incluir en el trabajo presentado como propio, partes hechas por otra persona. **En caso que corresponda a “copia” a otros alumnos, la sanción anterior se aplicará a todos los involucrados**. En todos los casos, se informará a la Dirección de Docencia de la Escuela de Ingeniería para que tome sanciones adicionales si lo estima conveniente. Obviamente, está permitido usar material disponible públicamente, por ejemplo, libros o contenidos tomados de Internet, siempre y cuando se incluya la referencia correspondiente y sea autorizado por los ayudantes.

Lo anterior se entiende como complemento al Reglamento del Alumno de la Pontificia Universidad Católica de
Chile<sup><a name="pucCLBack">[1](#pucCL)</a></sup>. Por ello, es posible pedir a la Universidad la aplicación de sanciones adicionales especificadas en dicho reglamento.

<sub>**<a name="pucCL">[1](#pucCL)</a>**: Reglamento del Alumno de la Pontificia Universidad Católica de Chile disponible en: http://admisionyregistros.uc.cl/alumnos/informacion-academica/reglamentos-estudiantiles [&#8593;](#pucCLBack)</sub>
