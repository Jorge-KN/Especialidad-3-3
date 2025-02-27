## Proyecto: Consultoria de Empresas 2023 - Monitoreo de Vertientes

## Descripción 
El proyecto "Monitoreo Aguas de Vertientes" se concibe como una solución tecnológica e iniciativa ambiental destinada a supervisar y analizar vertientes naturales de bajo caudal en zonas rurales, donde la ausencia y el alto costo de las estaciones hidrogeológicas limitan el acceso a información vital sobre la calidad del agua. Utilizando un conjunto de sensores, el sistema recolecta datos en tiempo real sobre diversos parámetros, como el caudal, pH, la turbidez, la conductividad, entre otros. 

Estos datos se presentan en una plataforma web accesible para las comunidades locales que se abastecen de vertientes. El proyecto facilita la participación activa de los comuneros permitiéndoles acceder a datos relevantes relacionados con el caudal y calidad del agua que consumen. Además, se busca abordar desafíos legales, como las regulaciones del código de aguas que exigen que las extracciones de vertientes sean legalmente inscritas y brindar a la comunidad herramientas técnicas y materiales para una gestión hídrica efectiva ante estas regulaciones.

##### Pasos a seguir para clonar el repo:
- Clonar el repositorio en su PC.  
`git clone https://github.com/Juanluis22/Vertientes.git`
- Creación del Entorno Virtual > Miniconda.  
`conda create -n Vertientes`  
Activación:  
`conda activate Vertientes`  
- Instalación de requerimientos.  
`pip install -r requirements.txt`  
- Comprobar Instalación.  
`pip list`  

##### Pasos a seguir para ejecutar la pagina:
- Configurar 'settings.py' con los datos de la base de datos. 

- Hacer las migraciones.
`python manage.py makemigrations`  

- Ejecutar las migraciones.
`python manage.py migrate`  

- Crear un superusuario.
`python manage.py createsuperuser`
Seguir los pasos (nombre, correo, clave, etc.)

- Añadir parametros a la BD en PostgreSQL:

una vez creada la nueva bd y las migraciones sean hechas, insertar: 

INSERT INTO auth_group VALUES(1, 'Administrador');
INSERT INTO auth_group VALUES(2, 'Usuario');
INSERT INTO user_profile VALUES(0,'No','Si',1,1)

Finalmente, activar el usuario creado mediante "`python manage.py createsuperuser`" desde PGADMIN, especificamente
en la columna "IsActive", columna Booleana que esta en FALSE por defecto, basta con dejarla en TRUE.





------------

#### Logo
#
## Screenshots
#
#### Diagrama de Sistema
# ![Logo](https://github.com/Juanluis22/Vertientes/blob/main/Imagenes/Diagrama%20de%20sistema.png)

#### Home
# 
#### Login
#
### Administrator
# 
### Create User
# 
------------


