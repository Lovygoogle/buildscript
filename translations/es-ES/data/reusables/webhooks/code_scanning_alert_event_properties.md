| Clave        | Type        | Descripción                                                                                                                                                                                               |
| ------------ | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Acción`     | `secuencia` | La acción que se realizó. Este puede ser uno de entre `created`, `reopened_by_user`, `closed_by_user`, `fixed`, `appeared_in_branch`, o `reopened`.                                                       |
| `alerta`     | `objeto`    | La alerta de escaneo de código involucrada en el evento.                                                                                                                                                  |
| `ref`        | `secuencia` | La referencia de Git de la alerta de escaneo de código. Cuando la acción se muestra como `reopened_by_user` o `closed_by_user`, el evento se activó mediante el `sender` y este valor estará vacío.       |
| `commit_oid` | `secuencia` | El SHA de la confirmación de la alerta del escaneo de código. Cuando la acción se muestra como `reopened_by_user` o `closed_by_user`, el evento se activó mediante el `sender` y este valor estará vacío. |