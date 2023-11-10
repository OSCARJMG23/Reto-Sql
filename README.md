# Reto-Sql
### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   # Solucion en 'sql'
    SELECT nombre FROM tblUsuarios;
   ```
   ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/b99a2266-3a12-44a9-8d8f-fd6922b5599c)


2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
    # Solucion en 'sql'
      SELECT MAX(saldo)
    -> FROM tblUsuarios
    -> Where sexo = "M";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/e8201e12-f897-4bea-8256-69fe32a0f521)

     

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
      # Solucion en 'sql'
      SELECT nombre,telefono
    -> FROM tblUsuarios
    -> Where marca = "NOKIA" OR marca = "BLACKBERRY" OR marca = "SONY";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/887448a3-c14d-4e1d-9fc9-cdc4401b39a9)


4. Contar los usuarios sin saldo o inactivos

     ```sql
      # Solucion en 'sql'
      SELECT COUNT(*)
    -> FROM tblUsuarios
    -> WHERE saldo = 0 OR activo = false;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/7bbafd00-5fad-4dc8-b7e4-49d43ba01e22)

     

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
      # Solucion en 'sql'
      SELECT usuario
    -> FROM tblUsuarios
    -> WHERE nivel = 1 OR nivel = 2 OR nivel = 3;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/239d1156-4778-40ef-95f0-80a90a1a4030)

     

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
      # Solucion en 'sql'
      SELECT telefono
    -> FROM tblUsuarios
    -> WHERE saldo <= 300;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/c799df8d-6967-40c8-88a7-cd92d41aa09a)


7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
      # Solucion en 'sql'
      SELECT SUM(saldo)
    -> FROM tblUsuarios
    -> WHERE compañia = "NEXTEL";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/44a33600-8cb0-4ac2-848e-f769f6a364fd)


8. Contar el número de usuarios por compañía telefónica

     ```sql
      # Solucion en 'sql'
      SELECT compañia, COUNT(*) AS usuarios
    -> FROM tblUsuarios
    -> GROUP BY compañia;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/072e91ac-d9cb-4e55-ae04-8dcd4096d6c2)


9. Contar el número de usuarios por nivel

     ```sql
      # Solucion en 'sql'
      SELECT nivel, COUNT(*) AS usuarios
    -> FROM tblUsuarios
    -> GROUP BY nivel;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/6b1d5446-44cd-48a0-8e41-db4952856111)

     

10. Listar el login de los usuarios con nivel 2

      ```sql
       # Solucion en 'sql'
       SELECT usuario
    -> FROM tblUsuarios
    -> WHERE nivel = 2;
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/1b3115f4-33e9-4804-9769-26f78d0bb437)


11. Mostrar el email de los usuarios que usan gmail

      ```sql
       # Solucion en 'sql'
       SELECT email
    -> FROM tblUsuarios
    -> WHERE email LIKE "%gmail%";
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/079c8a38-03d4-476a-a559-a198f7549c7a)


12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
       # Solucion en 'sql'
     SELECT nombre,telefono
    -> FROM tblUsuarios
    -> Where marca = "LG" OR marca = "SAMSUNG" OR marca = "MOTOROLA";
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/38dcf4a4-1c1f-4eae-858d-779c8971e2fd)


------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
      # Solucion en 'sql'
      SELECT nombre,telefono
    -> FROM tblUsuarios
    -> WHERE marca NOT IN ("LG", "SAMSUNG");
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/94916750-6e47-47a8-bc77-aac1fe18d612)


2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia = "IUSACELL";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/7a2760b4-0d13-40e6-bcd8-e5a27f0bb5e4)


3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia != "TELCEL";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/a8a9ee07-fdbd-433e-b290-dc3b1db78f08)


4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
      # Solucion en 'sql'
      SELECT AVG(saldo) AS PROMEDIO
    -> FROM tblUsuarios
    -> WHERE marca = "NOKIA";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/2c70b5f8-c9ab-4f25-8d4c-7115845e17da)


5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia = "IUSACELL" OR compañia = "AXEL";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/0dba6f21-8382-4ea5-b571-38d414ae6f9b)


6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
      # Solucion en 'sql'
      SELECT email
     FROM tblUsuarios
     WHERE email NOT LIKE '%yahoo%';
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/c3236045-ec0d-494d-a141-ff438352fc87)


7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
      # Solucion en 'sql'
       SELECT usuario, telefono
    -> FROM tblUsuarios
    -> WHERE compañia NOT IN("TELCEL","IUSACELL");
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/ae8b87ac-df13-41b7-9cb2-5fa1d7cef6d3)

     

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
     FROM tblUsuarios
     WHERE compañia = "UNEFON";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/164d7b36-b214-4e48-972b-8bde63de31a8)


9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
     FROM tblUsuarios
     ORDER BY marca DESC;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/69e92cff-45ec-4ea2-9218-b77701da689a)


10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
       # Solucion en 'sql'
      SELECT DISTINCT compañia
     FROM tblUsuarios
     ORDER BY RAND();
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/52f8af66-b69a-4fbc-97ef-023fe94ba15e)


11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
       # Solucion en 'sql'
     SELECT usuario
     FROM tblUsuarios
     WHERE nivel=0 OR nivel=2;
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/aa008cdf-1fe3-4f1a-9767-130ade73a701)


12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
       # Solucion en 'sql'
       SELECT AVG(saldo) AS PROMEDIO
    -> FROM tblUsuarios
    -> WHERE marca = "LG";
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/32198663-c333-46f8-87d7-d9129b47687a)


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
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/f4e10b7b-3dfb-4e52-a0e9-7221734c85fa)


2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
      # Solucion en 'sql'
      SELECT nombre, telefono
    -> FROM tblUsuarios
    -> WHERE marca != "BLACKBERRY";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/e5fad4eb-6e53-4aa6-99c1-d52e1e30d895)


3. Listar el login de los usuarios con nivel 3

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=3;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/02d6c709-3097-4e03-8931-b86e3f0b60bf)


4. Listar el login de los usuarios con nivel 0

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=0;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/3bb561e0-5df5-4aa7-9f14-e527b7652c35)


5. Listar el login de los usuarios con nivel 1

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE nivel=1;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/2fd78f4b-2c56-4a82-ab19-3840119172ad)


6. Contar el número de usuarios por sexo

     ```sql
      # Solucion en 'sql'
      SELECT sexo, COUNT(*) AS USUARIOS
    -> FROM tblUsuarios
    -> GROUP BY sexo;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/ce7fc479-8e3b-4f4b-806b-3c7e3b22fe0e)


7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
     FROM tblUsuarios
     WHERE compañia = "AT&T";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/afb98b90-2de7-4ef4-bb6c-3b3ae757e98e)


8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT compañia
     FROM tblUsuarios
     ORDER BY compañia DESC;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/f7613b60-9498-44d5-b975-d2f27dd1e642)


9. Listar el logn de los usuarios inactivos

     ```sql
      # Solucion en 'sql'
      SELECT usuario
     FROM tblUsuarios
     WHERE activo = false;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/a13e111f-b84a-4df0-bcaf-2bf9c744822a)


10. Listar los números de teléfono sin saldo

      ```sql
       # Solucion en 'sql'
       SELECT telefono
       FROM tblUsuarios
       WHERE saldo = 0;
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/f8cadc4d-d471-49bc-a11c-09a37f4df26d)


11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
       # Solucion en 'sql'
       SELECT MIN(saldo) AS min_saldo
       FROM tblUsuarios
       WHERE sexo = 'H';
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/45fbd3bb-1094-490d-9804-eb72c9447a8d)


12. Listar los números de teléfono con saldo mayor a 300

      ```sql
       # Solucion en 'sql'
       SELECT telefono
       FROM tblUsuarios
       WHERE saldo >= 300;
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/63f90ef4-49f4-4cea-9f55-46d1db3ce8c2)


------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
      # Solucion en 'sql'
      SELECT COUNT(*) as total, marca
      FROM tblUsuarios
      GROUP BY marca;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/fc957b23-d41d-4927-90f9-d1dab3c6240e)


2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
      # Solucion en 'sql'
      SELECT nombre, telefono
      FROM tblUsuarios
      WHERE marca != 'LG';
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/b952eb6a-1d8f-4d23-b700-f0688a942d00)


3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT compañia
      FROM tblUsuarios
      ORDER BY compañia ASC;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/9452cfc3-f006-4a8c-9275-b3e338e62da2)


4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
      # Solucion en 'sql'
      SELECT SUM(saldo) as totalSaldo
      FROM tblUsuarios
      WHERE compañia = 'UNEFON';
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/02485b12-22e1-489f-ab05-37823d39199e)


5. Mostrar el email de los usuarios que usan hotmail

     ```sql
      # Solucion en 'sql'
      SELECT email
      FROM tblUsuarios
      WHERE email LIKE '%hotmail%';
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/a85fa361-15ba-49c6-a229-72414a2ff584)


6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
      # Solucion en 'sql'
      SELECT nombre
      FROM tblUsuarios
      WHERE saldo = 0 OR activo = false;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/17ea2218-3a69-4a04-b39c-f4ef145d8961)


7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

     ```sql
      # Solucion en 'sql'
      SELECT usuario, telefono
      FROM tblUsuarios
      WHERE compañia = "TELCEL" OR compañia = "IUSACELL";
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/437ba02f-ddff-4c3b-ad4f-a95b3e5a171c)


8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
      FROM tblUsuarios
      ORDER BY marca ASC;
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/12006c4b-3fbd-4064-a406-1dba9bbc686d)

     

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
      # Solucion en 'sql'
      SELECT DISTINCT marca
      FROM tblUsuarios
      ORDER BY RAND();
     ```
     ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/c7399328-186b-4603-95e3-334405a3b873)


10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
       # Solucion en 'sql'
       SELECT usuario, telefono
       FROM tblUsuarios
       WHERE compañia = "UNEFON" OR compañia = "IUSACELL";
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/d3380441-961f-43dd-8280-2f2de968d47d)


11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
       # Solucion en 'sql'
       SELECT nombre, telefono
       FROM tblUsuarios
       WHERE marca NOT IN( "MOTOROLA", "NOKIA");
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/de368b2f-b52e-4b0c-830d-3e3973ad30ad)


12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
       # Solucion en 'sql'
       SELECT SUM(saldo) AS totalSaldo
       FROM tblUsuarios
       WHERE compañia = "TELCEL";
      ```
      ![image](https://github.com/OSCARJMG23/Reto-Sql/assets/133609079/baefddb7-db3c-413c-b709-410c68c6d111)

