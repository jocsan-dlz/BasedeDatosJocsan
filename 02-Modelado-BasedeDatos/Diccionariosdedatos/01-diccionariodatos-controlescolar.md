# Diccionario de Datos de la Base de Datos Control Escolar 

1. Informacion General

| Elemento | valor |
| :--- | :--- |
| Proyecto | Control Escolar |
| Version | 1.0 |
| Fecha | Junio 2026 |
| Elaboro | Tec. Jocsan Diaz Luz, Programacion |
| SGBD | SQLSERVER |

2. Descripcion de la base de Datos

El Base de Datos Administra:

- carrera
- Alumno
- Profesor
- Materia
- Grupo
- Inscripcion

Permite controlar la oferta academica y la inscripion de estudiantes

3. Catalogo de Restricciones Utilizadas

| Catalogo | significado |
| :--- | :--- |
| PK| Primary key |
| FK|foreing key|
| NN|Not Null |
| UQ| Unique |
|AI|AutoIncrement oIdenty|
|CK|Check|
| DF| Default |

4. Diccionario de Datos

**Tabla:** _carrera_

**Descripcion**
Almacena las carreras ofertadas por la universidad

| Dato| Tipo |Longitud | Restricciones| Descripcion|
| :--- | :--- | :--- | :--- | :--- |
| id_carrera |INT |- |   PK, Ai, NN | Identificador de la carrera|
| Nombre  | VARCHAR | 100 | UQ, NN |        Nombre de la carrera |
| DUracion_cuatrimestre | INT | - |NN, CK (>0) | Duracion en cuatrimestre |

---

**Tabla:** _Alumno_    

**Descripcion**
Almacena la informacion de los estudiantes

|Campo|Tipo |Longitud | Restricciones| Descripcion|
| :--- | :--- | :--- | :--- | :--- |
| id_alumno |INT |- |   PK, Ai, NN | Identificador del alumno  |
| Matricula|VARCHAR | 10  | UQ, NN | Matricula institucional|
| Nombre  | VARCHAR|50|NN,| Nombre del alumno |
| Apellido_paterno |VARCHAR | 50 | NN | Apellido paterno |
| Apellido_materno |VARCHAR | 50 | NN | Apellido materno |
| Apellido_materno |VARCHAR | 50 | NN | Apellido materno |
| correo | VARCHAR | 100 | UQ, NULL | Correo Institucional |
| Fecha_nacimiento | DATE | - | NN | Fecha nacimiento
| id_carrera | INT | - | FK, NN | Carrera a la que pertenece |

---

TODO: Documentar las siguientes tablas

5. Relaciones en la base de datos

| Relacion | Cardinalidad | Descripcion |
| :--- | :--- | :--- |
| Carrera -> Alumno | 1:N | Una carrera tiene muchos alumnos |
| Carrera -> Materia | 1:N | Una carrera tiene muchas materias | 
| Profesor -> Grupo | 1:N | Un profesor puede impartir en varios grupos | 
| Materia -> Grupo | 1:N | Una Materia puede abrirse en varios grupos |
| Alumno -> inscripcion | 1:N | Un alumno puede tener varias instrucciones |
| Grupo -> Inscripcion | 1:N | Un grupo puede tener muchos alumnos |

6. Matriz de claves foraneas 

| Tabla | Campo FK | Referencia |
| :--- | :--- | :--- | 
| Alumno | id_carrera | Carrera(id_carrera) | 
| Materia |id_carrera | carrera(id_carrera) |
| Grupo | id_profesor | profesor(id_profesor) |
| Grupo | id_materia | materia(id_materia) |
| Inscripcion | id_alumno | Alumno(id_alumno) |
| Inscripcion | id_grupo | Grupo(id_grupo) |

7. Integridad referencial 

| Clave| Regla |
| :--- | :--- |
| IR-01 | No se puede registrar un alumno con una carrera inexistente |
| IR-02 | No se puede crear un grupo para una materia inexistente |
| IR-03 | No se puede crear un grupo para un profesor inexistente |

8. Reglas del negocio

| Clave| Regla |
| :--- | :--- |
| RN-01 | Un alumno pertenee a unas sola carrera |
| RN-02 | Una carrera puede tener muchos alumnos |
| RN-03 | Una carrera puede tener muchas materias|
| RN-04 | Unprofesor puede impartir varios grupos|

9. Diagrama relacional

![EjercicioRelacional](../../img/Relacional/Tabla_3.png)
