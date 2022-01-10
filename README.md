1. Cree una tabla llamada CURSO con los atributos:  
Código de curso (clave primaria, entero no nulo)  
Nombre (varchar no nulo)  
Descripcion (varcha)  
Turno (varchar no nulo)  

__CREATE TABLE curso (id INT NOT NULL,nombre VARCHAR NOT NULL, descripción VARCHAR, turno VARCHAR NOT NULL, PRIMARY KEY (id))__

2. Agregue un campo “cupo” de tipo numérico

__ALTER TABLE curso ADD cupo INT__

3. Inserte datos en la tabla:  
(101, “Algoritmos”,”Algoritmos y Estructuras de Datos”,”Mañana”,35)  
(102, “Matemática Discreta”,””,”Tarde”,30)  

__INSERT INTO curso VALUES(101,'Algoritmos','Algoritmos y Estructuras de Datos','Mañana',35)__

__INSERT INTO curso VALUES(102,'Matemática Discreta',NULL,'Tarde',30)__

4. Intente ingresar un registro con el nombre nulo y verifique que no funciona.

__INSERT INTO curso VALUES(103,NULL,NULL,'Tarde',30)__ 

5. Intente ingresar un registro con la clave primaria repetida y verifique que no funciona.

__INSERT INTO curso VALUES(102,'Matemática Discreta',NULL,'Tarde',30)__

6. Actualice, para todos los cursos, el cupo en 25.

__UPDATE curso SET cupo = 25__

7. Elimine el curso Algoritmos.

__DELETE FROM curso WHERE nombre = "Algoritmos"__

---

Para listar todas las tuplas:  

__SELECT * FROM curso__
