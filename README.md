# 6.3 Active Directory - Challenge 
- [6.3 Active Directory - Challenge](#63-active-directory---challenge)
  - [Necesidad de creación de unidades organizativas (OU)](#necesidad-de-creación-de-unidades-organizativas-ou)
  - [Creación de grupos](#creación-de-grupos)
  - [Equipos creados dentro de cada una de las unidades organizativas](#equipos-creados-dentro-de-cada-una-de-las-unidades-organizativas)
  - [Unir equipos al dominio](#unir-equipos-al-dominio)
  - [Usuarios creados dentro de cada una de las unidades organizativas](#usuarios-creados-dentro-de-cada-una-de-las-unidades-organizativas)
  - [Carpetas, recursos compartidos, permisos de acceso a ellos](#carpetas-recursos-compartidos-permisos-de-acceso-a-ellos)
  - [Acceso de usuarios al dominio y a recursos compartidos](#acceso-de-usuarios-al-dominio-y-a-recursos-compartidos)
  - [Perfil obligatorio para usuario](#perfil-obligatorio-para-usuario)
  - [Perfil móvil para profesor](#perfil-móvil-para-profesor)
  - [Ubuntu cliente](#ubuntu-cliente)

## Necesidad de creación de unidades organizativas (OU)
- En mi caso hice una unidad organizativa por cada ciclo (ASIR, DAW, SMR),y dentro, una por cada año del ciclo (PrimerCurso, SegundoCurso)

- In my case I made an organizational unit for each cycle (ASIR, DAW, SMR), and inside, one for each year of the cycle (First Course, Second Course)
![UO](./6.3Wserver/UO.png)
## Creación de grupos
- He creado un grupo global para alumnos llamado "Alumnos" y otro global para profesores llamado "Profesores", lo puse como grupo primario y eliminé el grupo "usuarios del dominio", para que no sean de grupos genéricos y tengan permisos específicos, no he necesitado crear más grupos por ciclo o curso porque he comprobado que no había ningún conflicto a la hora de compartir los recursos según el trabajo que se ha mandado, el usuario entraba en su propia carpeta personal y no veía nada de otros usuarios, si se hubiera requerido permisos especiales para cada curso o ciclo si lo hubiera creado, y por lo tanto me he adaptado a lo que se pedía.

- I have created a global group for students called "Students" and another global group for teachers called "Teachers", I put it as a primary group and I deleted the "domain users" group, so that they are not from generic groups and have specific permissions, I have not needed to create more groups per cycle or course because I have verified that there was no conflict when sharing resources according to the work that has been sent, the user entered his own personal folder and did not see anything from other users, if he had required special permissions for each course or cycle if I had created it, and therefore I have adapted to what was requested.
![g](./6.3Wserver/grupos.png)
![g1](./6.3Wserver/alumnosgg.png)
![g2](./6.3Wserver/profesoresgg.png)
## Equipos creados dentro de cada una de las unidades organizativas
- Se han creado 2 equipos, uno para windows llamado "ANGELW10" y otro ubuntu llamado "UBUNTU-DESK"

- 2 computers have been created, one for windows called "ANGELW10" and another for ubuntu called "UBUNTU-DESK"
![equipo](./6.3Wserver/ordenadores.png)
## Unir equipos al dominio
- Aquí se muestra la unión del equipo al dominio "angelw10.angel20.local"

- Shown here is the join of the computer to the domain "angelw10.angel20.local"
![cliente](./6.3Wserver/unirequipoaldominio.png)
## Usuarios creados dentro de cada una de las unidades organizativas
- He creado un usuario por cada curso, en total serían 6, y así tenerlos mejor organizados y saber que usuario pertenece a cada ciclo y curso, con restricción horaria, ASIR Y DAW de 16h a 22h y SMR de 8h a 15h

- I have created a user for each course, in total there would be 6, and thus have them better organized and know which user belongs to each cycle and course, with time restrictions, ASIR AND DAW from 4:00 p.m. to 10:00 p.m. and SMR from 8:00 a.m. to 3:00 p.m.
![usuarios](./6.3Wserver/UO.png)
- Su pestaña de cuenta, "el usuario no puede cambiar la contraseña" activada

- Your account tab, "user cannot change password" enabled
![u2](./6.3Wserver/UOalumnoperfil.png)
- Su horario

- Schedule
![u3](./6.3Wserver/UOalumnohora.png)
- Equipo de inicio de sesión vinculado al usuario

- Login computer linked to the user
![u4](./6.3Wserver/UOalumnoequipo.png)
- Su perfil de usuario y su carpeta particular

- Your user profile and home folder
![u5](./6.3Wserver/UOalumnoPU-CP.png)
- Usuario Profesor

- Teacher User
![profe](./6.3Wserver/grupos.png)
- Restricción horaria de 24h de Lunes a Viernes para profesor1

- Time restriction of 24 hours from Monday to Friday for teacher1
![profe1](6.3Wserver/profesor1hora.png)
- Su perfil de usuario y su carpeta particular

- Your user profile and home folder
![profe2](./6.3Wserver/profesor1PU-CP.png)
## Carpetas, recursos compartidos, permisos de acceso a ellos
- Se crean las carpetas "Asir", "Daw" y "Smr" correspondiente a cada ciclo, así cada usuario de cada ciclo tendrá su carpeta personal de forma separada y organizada, para que el administrador lo tenga accesible de forma más fácil.

- Carpeta "Asir" con quien comparto, añado el grupo alumnos y le doy permisos de lectura y escritura.

- The "Asir", "Daw" and "Smr" folders corresponding to each cycle are created, so each user of each cycle will have their personal folder separately and organized, so that the administrator has it more easily accessible.

- "Asir" folder with whom I share, I add the student group and give it read and write permissions.
![asir](./6.3Wserver/CCasir.png)
- Permisos de seguridad del grupo alumnos

- Student group security permissions
![asir1](./6.3Wserver/CCasirSeguridad.png)
- Carpeta creada de forma automáticamente como carpeta personal de "alumno1"

- Folder automatically created as personal folder of "student1"
![asir2](./6.3Wserver/CCasirAlumno1Seguridad.png)
- La carpeta "Documentacion" donde todos los alumnos puedan leer, pero sólo los profesores puedan escribir en ella.

- The "Documentation" folder where all students can read, but only teachers can write to it.
![docu](./6.3Wserver/CCdocu.png)
- Carpeta "Documentacion", pestaña seguridad, muestro los permisos del grupo alumnos

- "Documentation" folder, security tab, I show the permissions of the student group
![docu1](./6.3Wserver/CCdocuSeguridadAlumnos.png)
- Carpeta "Documentacion", pestaña seguridad, muestro los permisos del grupo profesores

- "Documentation" folder, security tab, I show the permissions of the teachers group
![docu2](./6.3Wserver/CCdocuSeguridadProfe.png)
- Prueba de que "alumno1" no puede borrar un archivo creado dentro de la carpeta "Documentación"

- Proof that "student1" cannot delete a file created inside the "Documentation" folder
![docu3](./6.3Wserver/CCdocuClienteDenegado.png)
- La carpeta "Publica"  donde todos los usuarios, puedan leer y/o modificar los ficheros y carpetas

- The "Public" folder where all users can read and/or modify files and folders
![pu](./6.3Wserver/CCpublica.png)
- Pestaña seguridad, permisos para alumnos

- Security tab, student permissions
![pu2](./6.3Wserver/CCpublicaSeguridadAlumnos.png)
- Pestaña seguridad, permisos para profesores

- Security tab, permissions for teachers
![pu3](./6.3Wserver/CCpublicaSeguridadProfe.png)
## Acceso de usuarios al dominio y a recursos compartidos
- Como vemos en esta imagen, estoy conectado con "alumno1" al servidor y se automonta las unidades compartidas con el usuario, "alumno1" como carpeta personal, y las 2 carpetas "Pública" y "Documentación"

- As we can see in this image, I am connected to "student1" to the server and the units shared with the user are automounted, "student1" as a personal folder, and the 2 folders "Public" and "Documentation"
![recursos](./6.3Wserver/Acceso%20de%20usuarios%20al%20dominio%20y%20a%20recursos%20compartidos.png)
## Perfil obligatorio para usuario
- Para generar un perfil obligatorio cuando el alumno se conencta al servidor y después se desloguea, crea esta carpeta llamada "alumno1.V6", para entrar a esta carpeta tendremos que cambiar el propietario de la carpeta al administrador en la pestaña seguridad, en ella encontramos un archivo llamado "NTUSER.DAT" que la extensión .DAT quiere decir perfil móvil, el cual lo renombraremos a "NTUSER.MAN" para hacer el perfil obligatorio

- To generate a mandatory profile when the student connects to the server and then logs out, create this folder called "student1.V6", to enter this folder we will have to change the owner of the folder to administrator in the security tab, in it we find a file called "NTUSER.DAT" that the extension .DAT stands for roaming profile, which we will rename to "NTUSER.MAN" to make the profile mandatory
![PO](./6.3Wserver/POalumno1.png)
![PO1](./6.3Wserver/POdetalles.png)
## Perfil móvil para profesor
- Haremos lo mismo con el profesor para entrar a su carpeta y veremos que por defecto está como "NTUSER.DAT"  y lod ejamos así para que sea un pèrfil movil

- We will do the same with the teacher to enter his folder and we will see that by default it is as "NTUSER.DAT" and we leave it like this so that it is a mobile profile
![PM](./6.3Wserver/PMprofesor1.png)
## Ubuntu cliente
- En esta imagen muestro el nombre de la máquina de ubuntu llamada "angel-virtualbox"

- In this image I show the name of the ubuntu machine called "angel-virtualbox"
![ubu](./6.3Wserver/ubuntuequiposerver.png)
- Y aquí una vez dentro del usuario "alumno1" desde el cliente ubuntu, y se ve como solo pertenece al grupo "alumnos"

- And here once inside the user "student1" from the ubuntu client, and it looks like it only belongs to the group "students"
![ubu1](./6.3Wserver/ubuntucliente.png)
