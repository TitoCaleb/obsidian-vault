IAM es un servicio global
La cuenta que se crea al registrarse en AWS se conoce como cuenta ROOT o RAIZ
Los usuarios son personas dentro de la organización , y pueden ser agrupados
Los grupos contienen usuarios, no otros grupos
Los usuarios no tienen porque pertenecer a un grupo y también pueden pertenecer a varios grupos.

![[Pasted image 20240326210645.png]]

## PERMISOS

- A los **usuarios** o **grupos** se pueden asignar documentos JSON llamados políticas.
- Estas políticas definen los permisos del usuario.
- En AWS se aplica el principio de mínimo privilegio: no dar más permisos de los que un usuario necesita.
Ejemplo:
```json
{
	"Version": "2012-10-17",
	"Statement" : [
		{
			"Effect": "Allow",
			"Action": "ec2:Describe",
			"Resource": "*"
		},
		{
			"Effect": "Allow",
			"Action": "elasticloadbalancing:Describe*",
			"Resource": "*"
		},
		{
			"Effect": "Allow",
			"Action": [
				"cloudwatch:ListMetrics",
				"cloudwatch:GetMetricStatistics",
				"cloudwatch:Describe"
			],
			"Resource": "*"
		},
	]
}
```

