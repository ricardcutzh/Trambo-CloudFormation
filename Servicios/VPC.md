# vpc.yml

## Parametros
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCName     | Nombre de la VPC     |   String |
| Subnet1Name     | Nombre de la subred 1     |   String |
| Subnet2Name     | Nombre de la subred 2     |   String |
| Subnet3Name     | Nombre de la subred 3     |   String |
| Subnet4Name     | Nombre de la subred 4     |   String |
| Subnet5Name     | Nombre de la subred 5     |   String |
| Subnet6Name     | Nombre de la subred 6     |   String |
| CIDRBlock     | Bloque de direcciones que conforman la VPC    |   String |
| NetworkMask     | Definicion de la mascara de subred para la VCP    |   String |

## Recursos
### VPC
* Bloque de IP de la VPC: 192.168.0.0/24 

### Subnet 1 (Publica)
* Bloque de IP: 192.168.0.0/27
* Availability Zone: us-west-2a
* Con asignacion de IPs publicas automaticamente

### Subnet 2 (Publica)
* Bloque de IP: 192.168.0.32/27
* Availability Zone: us-west-2a
* Con asignacion de IPs publicas automaticamente

### Subnet 3 (Publica)
* Bloque de IP: 192.168.0.94/27
* Availability Zone: us-west-2a
* Con asignacion de IPs publicas automaticamente

### Subnet 4 (Privada)
* Bloque de IP: 192.168.0.126/27
* Availability Zone: us-west-2b
* Sin asignacion de IPs publicas automaticamente

### Subnet 5 (Privada)
* Bloque de IP: 192.168.0.158/27
* Availability Zone: us-west-2b
* Sin asignacion de IPs publicas automaticamente

### Subnet 6 (Privada)
* Bloque de IP: 192.168.0.190/27
* Availability Zone: us-west-2b
* Sin asignacion de IPs publicas automaticamente

### Internet Gateway
* Puerta de salida para internet que se le agregara a la VPC

### Enlace de Internet Gateway
* Recurso para enlazar el internet gateway a la VPC

### Tabla de Enrutamiento Publica
* Definicion de la tabla de enrutamiento para las subredes publicas

### Ruta a Internet
* Definicion de la ruta hacia internet para la tabla publica

### Asociacion de Subnets publicas
* Recursos que definen la asociacion de las subnets a la tabla de enrutmiento publica

### Tabla de Enrutamiento Privada
* Definicion de la tabla de enrutamiento para las subredes publicas

### Asociacion de Subnets privadas
* Recursos que definen la asociacion de las subnets a la tabla de enrutmiento publica

### Definicion de Grupo de seguridad para la VPC
* Define las reglas de entrada para la VPC

## Outputs
* VPC: Id de la VPC creada
* SubnetPublic1: Id de la subnet publica 1
* SubnetPublic2: Id de la subnet publica 2
* SubnetPublic3: Id de la subnet publica 3