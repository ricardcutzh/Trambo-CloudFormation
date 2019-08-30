# lconf.yml

## Parametros
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| SecurityGroupLC     | Id del grupo de Seguridad creado  |   String |
| PublicSubnet1     |  Id del Volumen de Sistema de archivos  |   String |


## Recursos

### LConfiguration
* Configuracion de plantilla para las EC2 que se despliegan en la VPC

### Punto de Montaje de EFS
* Punto de montaje del sistema de archivos

## Outputs
* LConf: id o nombre de la configuracion creada para las EC2
