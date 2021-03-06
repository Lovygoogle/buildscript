---
title: Habilitar los GitHub Packages con MinIO
intro: 'Configura el {% data variables.product.prodname_registry %} con MinIO como tu almacenamiento externo.'
versions:
  ghes: '*'
type: tutorial
topics:
  - Enterprise
  - Packages
  - Storage
shortTitle: Habilitar los paquetes con MinIO
---

{% warning %}

**Advertencias:**
- Es crítico que configures las políticas de acceso restrictivo que necesites para tu bucket de almacenamiento, ya que {% data variables.product.company_short %} no aplica permisos de objeto específicos o listas de control de acceso adicionales (ACLs) a tu configuración de bucket de almacenamiento. Por ejemplo, si haces a tu bucket público, el público general en la internet podrá acceder a ellos.
- Te recomendamos utilizar un bucket dedicado para {% data variables.product.prodname_registry %}, separado de aquél que utilices para almacenar {% data variables.product.prodname_actions %}.
- Asegúrate de configurar el bucket que quieres utilizar en el futuro. No te recomendamos cambiar tu almacenamiento después de que comienzas a utilizar {% data variables.product.prodname_registry %}.

{% endwarning %}
## Prerrequisitos
Antes de que puedas habilitar y configurar el {% data variables.product.prodname_registry %} en {% data variables.product.product_location_enterprise %}, necesitas preparar tu bucket de almacenamiento de MinIO. Para ayudarte a configurar el bucket de MinIO rápidamente y navegar a las opciones de personalización de MinIO, consulta la [Guía de inicio rápido para configurar tu bucket de almacenamiento de MinIO para el {% data variables.product.prodname_registry %}](/admin/packages/quickstart-for-configuring-your-minio-storage-bucket-for-github-packages)".

Asegúrate que tu ID de clave de acceso y secreto de almacenamiento externo de MinIO tenga estos permisos:
  - `s3:PutObject`
  - `s3:GetObject`
  - `s3:ListBucketMultipartUploads`
  - `s3:ListMultipartUploadParts`
  - `s3:AbortMultipartUpload`
  - `s3:DeleteObject`
  - `s3:ListBucket`

## Habilitar el {% data variables.product.prodname_registry %} con el almacenamiento externo de MinIO

Although MinIO does not currently appear in the user interface under "Package Storage", MinIO is still  supported by {% data variables.product.prodname_registry %} on {% data variables.product.prodname_enterprise %}. También debes tomar en cuenta que el almacenamiento de objetos de MinIO es compatible con la API de S3 y puedes ingresar los detalles del bucket de MinIO en vez de aquellos de AWS S3.

{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
{% data reusables.enterprise_site_admin_settings.packages-tab %}
{% data reusables.package_registry.enable-enterprise-github-packages %}

{% ifversion ghes %}
1. Debajo de "Almacenamiento de Paquetes", selecciona **Amazon S3**.
1. Ingresa tus detalles de bucket de almacenamiento de MinIO en la configuración de almacenamiento de AWS.
    - **AWS Service URL:** La URL de hospedaje para tu bucket de MinIO.
    - **AWS S3 Bucket:** El nombre de tu bucket de MinIO compatible con S3 dedicado para el {% data variables.product.prodname_registry %}.
    - **AWS S3 Access Key** y **AWS S3 Secret Key**: Ingresa la ID de clave de acceso y clave secreta de MinIO para acceder a tu bucket.

    ![Cajas de entrada para los detalles de tu bucket de AWS S3](/assets/images/help/package-registry/s3-aws-storage-bucket-details.png)
{% endif %}
{% data reusables.enterprise_management_console.save-settings %}

## Pasos siguientes

{% data reusables.package_registry.next-steps-for-packages-enterprise-setup %}
