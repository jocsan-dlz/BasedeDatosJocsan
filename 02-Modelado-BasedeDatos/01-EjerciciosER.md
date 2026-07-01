# Ejercicios del modelo E-R

## Ejercicio 1.

un hospital registra informacion de sus pacientes: 

> De cada paciente que almacena:
- numero de paciente que lo identifica
- Nombre
- Fecha de Nacimiento

> De cada expediente medico se almacena:
- Numero de expediente 
- Fecha de apertura
- Tipo de sangre

> Reglas del negocio
1. Cada Paciente debe de tener exactamente un espediente medico
2. Cada expediente medico pertenece a un unico paciente
3. No puede existir un expediente sin paciente
4. No puede existir un paciente sin expediente

> Que se debe ralizar:

- identificar las entidades
- Identificar atributos 
- Dibujar las relaciones
- Determinar la cardinalidad 
- Determinar la participacion de cada entidad 



![Ejercicio1](..//img/ER/Diagrama%201.1.drawio.png)

## Ejercicio 2

Una Universidad administra profesores y cursos
> De cada profesor se alamcena

- El numero de profesor o Id
- Nombre
- Especialidad

> De cada **Curso** se almacena: 

- numero de curso 
- Nombre del curso
- Creditos (Cuanto vale esa materia)

> Reglas del negocio 

1. Un profesor puede impartir varios cursos
2. un curso solamente puede ser impartido por un profesor.
3. Puede existir un profesor que actualmente no imparta cursos
4. Todo curso debe estatar asignado a un profesor

![Ejercicio2](..//img/ER/Diagrama%202.drawio.png)

## Ejercicio 3

Una escuela administra alumnos y materias

> De cada **Alumno** se almacena:

- Matricula 
- Nombre
- Semestre

> De cada **Materia** se alamacena:

- Clave de la materia
- Nombre de la materia
- Creditos 

> Reglas del negocio

1. Un alumno puede inscribirse en varias materias
2. Una materia puede tener muchos alumnos inscritos
3. Puede existir una materia sin alumnos inscritos 
4. Todo alumno debe estar inscrito en al menos una materia
5. De cada inscripcion se desea almacenar:
    - Fecha de inscripcion
    - Calificacion final
Nota: a la relacion nombrarla **INSCRIBE**

![Ejercicio3](..//img/ER/Diagrama%203.drawio.png)

## Ejercicio 4
 
 Una empresa dedicada a las ventas al por mayor necesita registrar lo siguiente:
 
 > Para los clientes:

 - Numero de Cliente
 - Nombre (el cual es una persona moral)
 
 > Pedidos

 - Numero de pedido
 - Fecha de pedido

 > Productos:

 - Numero de producto
 - Nombre
 - Precio

 > Reglas del negocio
 
 1. Un cliente puede realizar muchos pedidos
 2. Cada pedido pertenece a un solo cliente
 3. Un pedido contiene varios prooductos
 4. Un producto puede aparecer en muchos pedidos
 5. un pedido debe contener al menos un producto
 6. Un producto puede no haber sido vendido
 7. El detalle del pedido no existe sin pedido
 8. El detalle del pedido no esiste sin producto
 9. El detalle almacena la cantidad vendida y el precio de venta

![Ejercicio4](..//img/ER/Diagrama%204.drawio.png)

## Ejercicio 5
1. The company is organized into departments. Each department has a unique name, a unique number, and a particular employee who manages the department. We keep track of the start date when that employee began managing the department. A department may have several locations.
2. A department controls a number of projects, each of which has a unique name, a unique number, and a single location.
3. We store each employee's name, Social Security number, address, salary, sex (gender), and birth date. An employee is assigned to one department, but may work on several projects, which are not necessarily controlled by the same department. We keep track of the current number of hours per week that an employee works on each project. We also keep track of the direct supervisor of each employee (who is another employee).
4. We want to keep track of the dependents of each employee for insurance purposes. We keep each dependent's first name, sex, birth date, and relationship to the employee.

![Ejercicio5](..//img/ER/Diagrama%206.jpeg)










