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
### Usuario ROOT: 
- Usuario principal con el que se crea la cuenta al que se le denomina “root user”. Es similar al usuario root de Linux.
- Se puede usar para acceder por consola o a través de código.
- Puede hacer cualquier tipo de operación.
> [!CAUTION]
> No se debería usar para las tareas diarias
