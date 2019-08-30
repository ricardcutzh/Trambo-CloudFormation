# Trambo Cloud | Cloud Formation
## Ejercicio 5

Crear el ejercicio 4 pero esta vez utilizando cloudformation
Consideraciones:
 - Usar nested stacks para segregar la logica de los recursos
 - Tambien deben crear la VPC del ejercicio 3 pero esta vez sin utilizar el peering

 # main.yml

 ### Parametros
<!---->
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| Template     | Bucket de S3 donde se almacenan los templates     |   String |
| VPC     | Ingresar un nombre para la VPC     |   String |
<!---->

### Rescursos

#### Network Stack
* Stack encargado de llamar al archivo vpc.yml para la creacion de la VCP con las diferentes subredes tres publicas y tres privadas
* Definicion de Stack: vpc.yml
##### Parametros De Stack
<!---->
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCName     | Nombre de la VPC     |   String |
<!---->


#### EFSStack
* Stack encargado de la creacion del sistema de archivos EFS
* Definicion de Stack: efs.yml

##### Parametros De Stack
<!---->
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCId    | ID de la VPC Creada    |   String |
| PublicSubnet1    | ID de la subnet 1 creada en NetworkStack    |   String |
| PublicSubnet2    | ID de la subnet 2 creada en NetworkStack    |   String |
| PublicSubnet3    | ID de la subnet 3 creada en NetworkStack    |   String |
| SecurityGroupVPC    | ID del security Group creado en NetworkStack  |   String |
<!---->

#### LCAutoScaling
* Stack encargado de la creacion del Launch Configuration de las EC2 a utilizar en el Auto Scaling Group
* Definicion de Stack: lconf.yml

##### Parametros De Stack
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| SecurityGroupLC    | ID del security Group creado en NetworkStack   |   String |
| EFSVol    | ID de el volumen EFS Creado en EFSStack   |   String |

#### AutoScalingStack
* Stack encargado de la creacion del Auto Scaling Group
* Definicion de Stack: scl.yml

##### Parametros De Stack
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| LaunchConfiguration    | ID del launch configuration creado en LCAutoScaling   |   String |
| EFSVol    | ID de el volumen EFS Creado en EFSStack   |   String |
| Subnet1    | ID de la subnet 1 creada en NetworkStack    |   String |
| Subnet2    | ID de la subnet 2 creada en NetworkStack    |   String |
| Subnet3    | ID de la subnet 3 creada en NetworkStack    |   String|
| SGroup    | ID del security Group creado en NetworkStack  |   String |

## Diagrama
![Diagram](AWS.jpg)