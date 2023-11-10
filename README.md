# Reto-Sql
### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   # Solucion en 'sql'
    SELECT nombre FROM tblUsuarios;
    ![Alt text](image.png)
   ```

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
    # Solucion en 'sql'
      SELECT MAX(saldo)
    -> FROM tblUsuarios
    -> Where sexo = "M";
    ![Alt text](image-1.png)
     ```

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
      # Solucion en 'sql'
      SELECT nombre,telefono
    -> FROM tblUsuarios
    -> Where marca = "NOKIA" OR marca = "BLACKBERRY" OR marca = "SONY";
    ![Alt text](image-2.png)
     ```

4. Contar los usuarios sin saldo o inactivos

     ```sql
      # Solucion en 'sql'
      SELECT COUNT(*)
    -> FROM tblUsuarios
    -> WHERE saldo = 0 OR activo = false;
    ![Alt text](image-3.png)
     ```

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
      # Solucion en 'sql'
      SELECT usuario
    -> FROM tblUsuarios
    -> WHERE nivel = 1 OR nivel = 2 OR nivel = 3;
    ![Alt text](image-4.png)
     ```

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
      # Solucion en 'sql'
      SELECT telefono
    -> FROM tblUsuarios
    -> WHERE saldo <= 300;
    ![Alt text](image-5.png)
     ```

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
      # Solucion en 'sql'
      SELECT SUM(saldo)
    -> FROM tblUsuarios
    -> WHERE compañia = "NEXTEL";
    ![Alt text](image-6.png)
     ```

8. Contar el número de usuarios por compañía telefónica

     ```sql
      # Solucion en 'sql'
      SELECT compañia, COUNT(*) AS usuarios
    -> FROM tblUsuarios
    -> GROUP BY compañia;
    ![Alt text](image-7.png)
     ```

9. Contar el número de usuarios por nivel

     ```sql
      # Solucion en 'sql'
      SELECT nivel, COUNT(*) AS usuarios
    -> FROM tblUsuarios
    -> GROUP BY nivel;
    ![Alt text](image-8.png)
     ```

10. Listar el login de los usuarios con nivel 2

      ```sql
       # Solucion en 'sql'
       SELECT usuario
    -> FROM tblUsuarios
    -> WHERE nivel = 2;
    ![Alt text](image-9.png)
      ```

11. Mostrar el email de los usuarios que usan gmail

      ```sql
       # Solucion en 'sql'
       SELECT email
    -> FROM tblUsuarios
    -> WHERE email LIKE "%gmail%";
    ![Alt text](image-10.png)
      ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
       # Solucion en 'sql'
     SELECT nombre,telefono
    -> FROM tblUsuarios
    -> Where marca = "LG" OR marca = "SAMSUNG" OR marca = "MOTOROLA";
    ![Alt text](image-11.png)
      ```

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
      # Solucion en 'sql'
      SELECT nombre,telefono
    -> FROM tblUsuarios
    -> WHERE marca NOT IN ("LG", "SAMSUNG");
    ![Alt text](image-12.png)
     ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia = "IUSACELL";
    ![Alt text](image-13.png)
     ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia != "TELCEL";
    ![Alt text](image-14.png)
     ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
      # Solucion en 'sql'
      SELECT AVG(saldo) AS PROMEDIO
    -> FROM tblUsuarios
    -> WHERE marca = "NOKIA";
    ![Alt text](image-15.png)
     ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia = "IUSACELL" OR compañia = "AXEL";
    ![Alt text](image-16.png)
     ```

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
      # Solucion en 'sql'
      SELECT email
     FROM tblUsuarios
     WHERE email NOT LIKE '%yahoo%';
     ![Alt text](image-17.png)
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
      # Solucion en 'sql'
       SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia NOT IN("TELCEL","IUSACELL");
    ![Alt text](image-18.png)
     ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
     FROM tblUsuarios
     WHERE compañia = "UNEFON";
     ![Alt text](image-19.png)
     ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
     FROM tblUsuarios
     ORDER BY marca DESC;
     ![Alt text](image-20.png)
     ```

10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
       # Solucion en 'sql'
      SELECT DISTINCT compañia
     FROM tblUsuarios
     ORDER BY RAND();
    ![Alt text](image-21.png)
      ```

11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
       # Solucion en 'sql'
     SELECT usuario
     FROM tblUsuarios
     WHERE nivel=0 OR nivel=2;
     ![Alt text](image-22.png)
      ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
       # Solucion en 'sql'
       SELECT AVG(saldo) AS PROMEDIO
    -> FROM tblUsuarios
    -> WHERE marca = "LG";
    ![Alt text](image-23.png)
      ```

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=1 OR nivel=3;
     ![Alt text](image-24.png)
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
      # Solucion en 'sql'
      SELECT nombre, telefono
    -> FROM tblUsuarios
    -> WHERE marca != "BLACKBERRY";
    ![Alt text](image-25.png)
     ```

3. Listar el login de los usuarios con nivel 3

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=3;
     ![Alt text](image-26.png)
     ```

4. Listar el login de los usuarios con nivel 0

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=0;
     ![Alt text](image-27.png)
     ```

5. Listar el login de los usuarios con nivel 1

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=1;
     ![Alt text](image-28.png)
     ```

6. Contar el número de usuarios por sexo

     ```sql
      # Solucion en 'sql'
      SELECT sexo, COUNT(*) AS USUARIOS
    -> FROM tblUsuarios
    -> GROUP BY sexo;
    ![Alt text](image-29.png)
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
     FROM tblUsuarios
     WHERE compañia = "AT&T";
     ![Alt text](image-30.png)
     ```

8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT compañia
     FROM tblUsuarios
     ORDER BY compañia DESC;
     ![Alt text](image-31.png)
     ```

9. Listar el logn de los usuarios inactivos

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE activo = false;
     ![Alt text](image-32.png)
     ```

10. Listar los números de teléfono sin saldo

      ```sql
       # Solucion en 'sql'
       SELECT telefono
       FROM tblUsuarios
       WHERE saldo = 0;
       ![Alt text](image-33.png)
      ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
       # Solucion en 'sql'
       SELECT MIN(saldo) AS min_saldo
       FROM tblUsuarios
       WHERE sexo = 'H';
       ![Alt text](image-34.png)
      ```

12. Listar los números de teléfono con saldo mayor a 300

      ```sql
       # Solucion en 'sql'
       SELECT telefono
       FROM tblUsuarios
       WHERE saldo >= 300;
       ![Alt text](image-35.png)
      ```

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
      # Solucion en 'sql'
      SELECT COUNT(*) as total, marca
      FROM tblUsuarios
      GROUP BY marca;
      ![Alt text](image-36.png)
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
      # Solucion en 'sql'
      SELECT nombre, telefono
      FROM tblUsuarios
      WHERE marca != 'LG';
      ![Alt text](image-37.png)
     ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT compañia
      FROM tblUsuarios
      ORDER BY compañia ASC;
      ![Alt text](image-38.png)
     ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
      # Solucion en 'sql'
      SELECT SUM(saldo) as totalSaldo
      FROM tblUsuarios
      WHERE compañia = 'UNEFON';
      ![Alt text](image-39.png)
     ```

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
      # Solucion en 'sql'
      SELECT email
      FROM tblUsuarios
      WHERE email LIKE '%hotmail%';
      ![Alt text](image-40.png)
     ```

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
      # Solucion en 'sql'
      SELECT nombre
      FROM tblUsuarios
      WHERE saldo = 0 OR activo = false;
      ![Alt text](image-41.png)
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
      FROM tblUsuarios
      WHERE compañia = "TELCEL" OR compañia = "IUSACELL";
      ![Alt text](image-42.png)
     ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
      FROM tblUsuarios
      ORDER BY marca ASC;
      ![Alt text](image-43.png)
     ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
      FROM tblUsuarios
      ORDER BY RAND();
      ![Alt text](image-44.png)
     ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
       # Solucion en 'sql'
       SELECT usuario, telefono
       FROM tblUsuarios
       WHERE compañia = "UNEFON" OR compañia = "IUSACELL";
       ![Alt text](image-45.png)
      ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
       # Solucion en 'sql'
       SELECT nombre, telefono
       FROM tblUsuarios
       WHERE marca NOT IN( "MOTOROLA", "NOKIA");
       ![Alt text](image-46.png)
      ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
       # Solucion en 'sql'
       SELECT SUM(saldo) AS totalSaldo
       FROM tblUsuarios
       WHERE compañia = "TELCEL";
       ![Alt text](image-47.png)
      ```
