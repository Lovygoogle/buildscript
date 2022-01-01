Se você estiver usando um domínio apex como seu domínio personalizado, recomendamos também configurar um subdomínio `www`. Se você configurar os registros corretos para cada tipo de domínio através do seu provedor DNS, {% data variables.product.prodname_pages %} irá automaticamente criar redirecionamentos entre os domínios. Por exemplo, se você configurar `www.example.com` como domínio personalizado do seu site, e você tiver registros de DNS de {% data variables.product.prodname_pages %} configurados para os domínios apex e `www`, `example. om` irá redirecionar para `www.example.com`. Note que redirecionamentos automáticos só se aplicam ao subdomínio `www`. Redirecionamentos automáticos não se aplicam a nenhum outro subdomínio, como o `blogue`.