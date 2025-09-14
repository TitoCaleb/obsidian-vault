
# Estructura de las políticas IAM
--- start-multi-column: ID_stqo
```column-settings
Number of Columns: 2
Largest Column: standard
Column Width: Full
```

- Consta de:
	- Versión: versión de lenguaje de la política, siempre incluye "2012-10-17"
	- Id: un identificador para la politica (opcional)
	- Statement: una o mas declaraciones individuales (obligatorio)
- Los statements constan de:
	- Sid: un identificador para la declaración (opcional)
	- Effect: si la sentencia permite o deniega el acceso (Allow, Deny)
	- Principal: cuenta/usuario/rol al que se aplica la politica
	- Action: lista de acciones que esta politica permite o deniega
	- Resource: lista de recursos a los que le aplican las acciones
	- Condition: condiciones para cuando esta politica está en efecto (opcional)

--- column-break ---

```json
{
	"Version": "2012-10-17",
	"Id": "S3-Account-Permissions",
	"Statement": [
		{
			"Sid": "1",
			"Effect": "Allow",
			"Principal": {
				"AWS": ["arn:aws:iam::123456789012:root"]
			},
			"Action": [
				"s3:GetObject",
				"s3:PutObject"
			],
			"Resource": ["arn:aws:s3::mybucket/*"]
		}
	]
}
```

--- end-multi-column

