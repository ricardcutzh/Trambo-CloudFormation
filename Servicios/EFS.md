# efs.yml

## Parameters
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCId     | Name of the VPC     |   String |
| PublicSubnet1     | Name of the public subnet 1 (id)    |   String |
| PublicSubnet2     | Name of the public subnet 2 (id)     |   String |
| PublicSubnet3     | Name of the public subnet 3 (id)    |   String |
| SecurityGroupVPC     | Id of the vpc's Security Group    |   String |

## Resources
### EFS Volume
* Resource that creates the EFS volume

### EFS's Mount Point
* The resource defines the EFS's mount point

## Outputs
* FileSystem: Id of the EFS File system
* MoutTargetEFS: Id of the EFS's mount point