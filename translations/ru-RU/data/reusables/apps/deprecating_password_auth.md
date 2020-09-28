{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.19" %}
{% warning %}

**Deprecation Notice:** {{ site.data.variables.product.prodname_dotcom }} will discontinue password authentication to the API.  You must now authenticate to the {{ site.data.variables.product.prodname_dotcom }} API with an API token, such as an OAuth access token, GitHub App installation access token, or personal access token, depending on what you need to do with the token.{% if currentVersion == "free-pro-team@latest" %} Password authentication to the API will be removed on November 13, 2020.{% endif %} For more information,{% if currentVersion == "free-pro-team@latest" %} including scheduled brownouts,{% endif %} see the [blog post](https://developer.github.com/changes/2020-02-14-deprecating-password-auth/).

{% if currentVersion != "free-pro-team@latest" %} Authenticating to the API using a password is currently available and not yet deprecated in {{ site.data.variables.product.prodname_ghe_server }}. {{ site.data.variables.product.prodname_dotcom }} will announce the deprecation and provide advanced notice before removing support for this feature.{% endif %}

{% endwarning %}
{% endif %}