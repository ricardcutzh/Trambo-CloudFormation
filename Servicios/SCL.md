# scl.yml

## Parametros
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| LaunchConfiguration     | Configuracion para las EC2     |   String |
| Subnet1     | Nombre de la subred 1     |   String |
| Subnet2     | Nombre de la subred 2     |   String |
| Subnet3     | Nombre de la subred 3     |   String |
| SGroup     | Grupo de seguridad para la VPC     |   String |

## Recursos
### Balanceador de Carga Clasico
* Recurso para la definicion del balanceador de carga clasico para la aplicacion

### Grupo Auto Escalable
* Recurso que define el grupo auto escalable que utiliza la configuracion de lanzamiento dentro del balanceador de carga

