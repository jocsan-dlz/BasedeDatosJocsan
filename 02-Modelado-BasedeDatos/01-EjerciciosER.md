# Ejercicios del modelo E-R

## Ejercicio 1.

un hospital registra informacion de sus pacientes: 

>De cada paciente que almacena:
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



![Ejercicio1](..//img/ER/Diagrama%201.drawio.png)

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

![Ejercicio2](..//img/ER/Diagrama%201.drawio.png)

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

![Ejercicio2](..//img/ER/Diagrama%201.drawio.png)

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














