# efs.yml

## Parametros
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCId     | Nombre de la VPC     |   String |
| PublicSubnet1     | Nombre de la subred 1     |   String |
| PublicSubnet2     | Nombre de la subred 2     |   String |
| PublicSubnet3     | Nombre de la subred 3     |   String |
| SecurityGroupVPC     | Grupo de seguridad para la VPC     |   String |

## Recursos
### Volumen de EFS
* Recurso para crear el sistema de archivos
### Punto de Montaje de EFS
* Punto de montaje del sistema de archivos

## Outputs
* FileSystem: Id del sistema de archivos
* MoutTargetEFS: Id del punto de montaje del sistema de archivos