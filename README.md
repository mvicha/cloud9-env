# cloud9-env
Parameters to specify:
  De la lista que se especifica, el parámetro que se debe revisar es el del ID de la subred donde ejecutar el entorno.
  C9NameParam:
    Description: Cloud9 Environment name
  C9DescParam:
    Description: Cloud9 Environment Description
  InstanceTypeParam:
    Default: t2.micro
    AllowedValues:
      - t2.micro
    Description: Enter the instance type value. Only t2.micro is allowed
  ImageIdParam:
    Default: amazonlinux-2-x86_64
    Description: Amazon AMI to use for Cloud9 instance
  * SubnetIdParam:
    Type: String
    Default: subnet-92fe8cf4
    Description: VPC where to run Cloud9 instance

Ejecución:
  Desde el sitio de AWS subimos nuestro archivo y esperamos a que se despliegue el entorno.
  Una vez que el entorno esté desplegado podemos entrar al mismo desde el apartado Cloud9 en la consola de AWS.
  Cuando ingresemos por primera vez podemos clonar este repositorio y ejecutar el archivo setup.sh incluído aquí.

Extras:
  Se incluye un archivo resize_disk.sh para aumentar el tamaño del disco de la VM, ya que es muy probable que el espacio
  No alcance. Para su ejecución sólo debemos ejecutar
    resize_disk.sh <tamaño desdeado>

  Por ejemplo, para cambiar el espacio de disco a 40Gb debemos ejecutar:
    resize_disk.sh 40

