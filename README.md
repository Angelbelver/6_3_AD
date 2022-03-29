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
![UO](./6.3Wserver/UO.png)
## Creación de grupos
- He creado un grupo global para alumnos llamado "Alumnos" y otro global para profesores llamado "Profesores", lo puse como grupo primario y eliminé el grupo "usuarios del dominio", para que no sean de grupos genéricos y tengan permisos específicos, no he necesitado crear más grupos por ciclo o curso porque he comprobado que no había ningún conflicto a la hora de compartir los recursos según el trabajo que se ha mandado, el usuario entraba en su propia carpeta personal y no veía nada de otros usuarios, si se hubiera requerido permisos especiales para cada curso o ciclo si lo hubiera creado, y por lo tanto me he adaptado a lo que se pedía.
![g](./6.3Wserver/grupos.png)
![g1](./6.3Wserver/alumnosgg.png)
![g2](./6.3Wserver/profesoresgg.png)
## Equipos creados dentro de cada una de las unidades organizativas
- Se han creado 2 equipos, uno para windows llamado "ANGELW10" y otro ubuntu llamado "UBUNTU-DESK"
![equipo](./6.3Wserver/ordenadores.png)
## Unir equipos al dominio
- Aquí se muestra la unión del equipo al dominio "angelw10.angel20.local"
![cliente](./6.3Wserver/unirequipoaldominio.png)
## Usuarios creados dentro de cada una de las unidades organizativas
- He creado un usuario por cada curso, en total serían 6, y así tenerlos mejor organizados y saber que usuario pertenece a cada ciclo y curso, con restricción horaria, ASIR Y DAW de 16h a 22h y SMR de 8h a 15h
![usuarios](./6.3Wserver/UO.png)
- Su pestaña de cuenta, "el usuario no puede cambiar la contraseña" activada
![u2](./6.3Wserver/UOalumnoperfil.png)
- Su horario
![u3](./6.3Wserver/UOalumnohora.png)
- Equipo de inicio de sesión vinculado al usuario
![u4](./6.3Wserver/UOalumnoequipo.png)
- Su perfil de usuario y su carpeta particular
![u5](./6.3Wserver/UOalumnoPU-CP.png)
- Usuario Profesor
![profe](./6.3Wserver/grupos.png)
- Restricción horaria de 24h de Lunes a Viernes para profesor1
![profe1](6.3Wserver/profesor1hora.png)
- Su perfil de usuario y su carpeta particular
![profe2](./6.3Wserver/profesor1PU-CP.png)
## Carpetas, recursos compartidos, permisos de acceso a ellos
- Se crean las carpetas "Asir", "Daw" y "Smr" correspondiente a cada ciclo, así cada usuario de cada ciclo tendrá su carpeta personal de forma separada y organizada, para que el administrador lo tenga accesible de forma más fácil.

- Carpeta "Asir" con quien comparto, añado el grupo alumnos y le doy permisos de lectura y escritura.
![asir](./6.3Wserver/CCasir.png)
- Permisos de seguridad del grupo alumnos
![asir1](./6.3Wserver/CCasirSeguridad.png)
- Carpeta creada de forma automáticamente como carpeta personal de "alumno1"
![asir2](./6.3Wserver/CCasirAlumno1Seguridad.png)
- La carpeta "Documentacion" donde todos los alumnos puedan leer, pero sólo los profesores puedan escribir en ella.
![docu](./6.3Wserver/CCdocu.png)
- Carpeta Documentacion, pestaña seguridad, muestro los permisos del grupo alumnos
![docu1](./6.3Wserver/CCdocuSeguridadAlumnos.png)
- Carpeta Documentacion, pestaña seguridad, muestro los permisos del grupo profesores
![docu2](./6.3Wserver/CCdocuSeguridadProfe.png)
- Prueba de que "alumno1" no puede borrar un archivo creado dentro de la carpeta "Documentación"
![docu3](./6.3Wserver/CCdocuClienteDenegado.png)
- La carpeta "Publica"  donde todos los usuarios, puedan leer y/o modificar los ficheros y carpetas
![pu](./6.3Wserver/CCpublica.png)
![pu2](./6.3Wserver/CCpublicaSeguridadAlumnos.png)
![pu3](./6.3Wserver/CCpublicaSeguridadProfe.png)
## Acceso de usuarios al dominio y a recursos compartidos
![recursos](./6.3Wserver/Acceso%20de%20usuarios%20al%20dominio%20y%20a%20recursos%20compartidos.png)
## Perfil obligatorio para usuario 
![PO](./6.3Wserver/POalumno1.png)
![PO1](./6.3Wserver/POdetalles.png)
## Perfil móvil para profesor
![PM](./6.3Wserver/PMprofesor1.png)
## Ubuntu cliente
![ubu](./6.3Wserver/ubuntuequiposerver.png)
![ubu1](./6.3Wserver/ubuntucliente.png)
