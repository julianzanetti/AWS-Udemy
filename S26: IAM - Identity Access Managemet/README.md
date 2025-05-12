# IAM Identify Access Management. Gestión de identidades en AWS
- Se debe dejar de trabajar con el usuario root inicial.
![image](https://github.com/user-attachments/assets/f2e65a97-3cd0-48c6-a3a9-b46702dee58e)

- IAM permite definir el acceso a los recursos de AWS:
  - **`Recurso IAM`**: Usuarios, grupos, roles, políticas, providers.
  - **`Identities`**: Identifican accesos(Usuarios, grupos y roles)
  - **`Entities`**: Objetos que usan para autenticarse (Usuarios y roles)
  - **`Principal`**:  Persona o aplicación que asume un usuario o rol. (User, role, Federated User, application)
![image](https://github.com/user-attachments/assets/eb4fa74f-6b35-40f6-9c1f-3c798f9e7165)

- Lo primero que tenemos que hacer es autenticarnos para tener la autorización (permisos). Podemos tener políticas (permisos) basadas en identidad (usuarios) o basadas en recursos o en tags u otras. Luego tenemos acciones que se pueden efectuar en los recurso que queremos acceder.
- Principal - Podemos entrar de tres formas: Usuario ROOT, Usuario IAM y AWS ROLE.

## Algunas Definiciones:
### Usuario ROOT: 
- Usuario principal con el que se crea la cuenta al que se le denomina “root user”. Es similar al usuario root de Linux.
- Se puede usar para acceder por consola o a través de código.
- Puede hacer cualquier tipo de operación.
> [!CAUTION]
> No se debería usar para las tareas diarias

### Usuario IAM:
- Es el usuario que se debe usar en el día a día.
- Representan usuario o aplicaciones que se conectarán y usarán los recursos de AWS.
- Pueden acceder desde la consola o desde un entorno CLI o SDK.
- Se les puede asignar distintos tipo de permisos para su trabajo diario.

### Grupos:
- Colección de usuario IAM que permite agrupar permisos para asignarlos a los usuarios.

### AWS ROLE:
- Se usan para dar permisos y privilegios durante un momento determinado.
- Cuando un determinado actor asume un rol, se le asigna un token temporal que le permite acceder a un determinado recurso para poder utilizarlo.
- Es similar a un usuario IAM pero en vez de estar asociado a una persona, es asumido por quien lo necesite para unas gestiones concretas.
- No tiene credenciales ni claves por tanto no tienen que ser enviadas o integradas dentro de una aplicación.
- El servicio que asigna estos Tokens se denomina “AWS Security Token Service”.

### Federación:
- Se pueden “federar” usuarios ya creados dentro de nuestro propio entorno, de esta forma se puede asumir unas credenciales temporales para el acceso a AWS.
![image](https://github.com/user-attachments/assets/70f45ed8-49f4-48ea-877e-6e6e61c4fdb2)

### Políticas y permisos:
- Para gestionar el acceso a un usuario o rol a AWS se crean políticas para luego asignarselas.
- Es un objeto AWS que al ser asignado a un usuario o recurso define sus permisos, por lo tanto identifican que se puede o no se puede hacer.
- Suelen estar hechas con un fichero JSON.

![image](https://github.com/user-attachments/assets/2c376719-508e-4bcf-9968-755e1159148f)

### Tipos de políticas:
- **`Identity policy`**: Se asocian a una entidad IAM, como usuarios, grupos o roles. Permite controlar las acciones que se pueden realizar en un recurso y bajo que condiciones. Pueden ser:
  - **`Manager`**: Políticas independientes que pueden ser asignadas a multiples usuarios, grupos o roles. Pueden ser creadas por AWS o personalizadas por nosotros. (Uso mas habitual)
  - **`Inline`**: Se integran en un usuario, grupo o rol. Son las menos adecuadas.
- **`Resource-Based Policies`**: Se asocian a un determinado recurso AWS (por ejemplo S3) y determinan las acciones que se pueden hacer sobre ese recurso.

### Access Advisor:
- Es una herramienta para poder comprobar que clases de políticas tiene un grupo o un usuario.
![image](https://github.com/user-attachments/assets/d7bd794e-f1c7-4e65-b1f8-12e30b404702)

## Consola IAM.
![image](https://github.com/user-attachments/assets/9844e0cc-52e9-4d07-ab55-ff236a1e02a2)
- **`ID de cuenta`**: Es única, la comparten root y todos los usuarios que se creen.
- **`Alias de cuenta`**: Es único para cada usuarios que se cree.
- **`URL de acceso`**: Para los usuarios IAM
