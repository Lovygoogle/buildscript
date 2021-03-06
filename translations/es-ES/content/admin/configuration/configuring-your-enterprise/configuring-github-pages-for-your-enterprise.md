---
title: Configurar GitHub Pages para tu empresa
intro: 'Puedes habilitar o inhabilitar {% data variables.product.prodname_pages %} para tu empresa y elegir si quieres hacer los sitios accesibles para el público en general.'
redirect_from:
  - /enterprise/admin/guides/installation/disabling-github-enterprise-pages/
  - /enterprise/admin/guides/installation/configuring-github-enterprise-pages/
  - /enterprise/admin/installation/configuring-github-pages-on-your-appliance
  - /enterprise/admin/configuration/configuring-github-pages-on-your-appliance
  - /admin/configuration/configuring-github-pages-on-your-appliance
  - /enterprise/admin/guides/installation/configuring-github-pages-for-your-enterprise/
  - /admin/configuration/configuring-github-pages-for-your-enterprise
versions:
  ghes: '*'
  ghae: '*'
type: how_to
topics:
  - Enterprise
  - Pages
shortTitle: Configurar GitHub Pages
---

## Habilitar los sitios públicos para {% data variables.product.prodname_pages %}

{% ifversion ghes %}Si se habilita el modo privado en tu empresa, el{% else %}El {% endif %}público en general no podrá acceder a los sitios de {% data variables.product.prodname_pages %} que se hospeden en tu empresa a menos de que habilites los sitios públicos.

{% warning %}

**Advertencia:** Si habilitas los sitios públicos para {% data variables.product.prodname_pages %}, cada sitio en cada repositorio de tu empresa será accesible para el público en general.

{% endwarning %}

{% ifversion ghes %}
{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
{% data reusables.enterprise_management_console.pages-tab %}
4. Selecciona **Public Pages** (Páginas públicas). ![Casilla de verificación para habilitar páginas públicas](/assets/images/enterprise/management-console/public-pages-checkbox.png)
{% data reusables.enterprise_management_console.save-settings %}
{% elsif ghae %}
{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.pages-tab %}
5. Debajo de "Políticas de las páginas", selecciona **{% data variables.product.prodname_pages %} públicas**. ![Casilla de verificación para habilitar las {% data variables.product.prodname_pages %} públicas](/assets/images/enterprise/business-accounts/public-github-pages-checkbox.png)
{% data reusables.enterprise-accounts.pages-policies-save %}
{% endif %}

## Inhabilitar {% data variables.product.prodname_pages %} para tu empresa

{% ifversion ghes %}
Si el aislamiento de subdominios está inhabilitado en tu empresa, también debes inhabilitar las {% data variables.product.prodname_pages %} para protegerte de vulnerabilidades de seguridad potenciales. Para obtener más información, consulta la sección "[Enabling subdomain isolation](/admin/configuration/enabling-subdomain-isolation)".
{% endif %}

{% ifversion ghes %}
{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
{% data reusables.enterprise_management_console.pages-tab %}
4. Anula la selección de **Enable Pages** (Habilitar páginas). ![Casilla de verificación para inhabilitar {% data variables.product.prodname_pages %}](/assets/images/enterprise/management-console/pages-select-button.png)
{% data reusables.enterprise_management_console.save-settings %}
{% elsif ghae %}
{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.pages-tab %}
5. Debajo de "Políticas de las páginas", deselecciona **Habilitar {% data variables.product.prodname_pages %}**. ![Casilla de verificación para inhabilitar {% data variables.product.prodname_pages %}](/assets/images/enterprise/business-accounts/enable-github-pages-checkbox.png)
{% data reusables.enterprise-accounts.pages-policies-save %}
{% endif %}

{% ifversion ghes %}
## Leer más

- "[Habilitar el modo privado](/admin/configuration/enabling-private-mode)"
{% endif %}
