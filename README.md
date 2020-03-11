# allauth-keycloak-provider

## install

`pip install -i https://test.pypi.org/simple/ allauth-keycloak-provider-fherdom`

## configure

```python
INSTALLED_APPS = [
    ...
    'django.contrib.sites',
    ...
    #
    'allauth',
    'allauth.account',
    'allauth.socialaccount',
    'allauth_keycloak_provider',
    ...
]

AUTHENTICATION_BACKENDS = (
    'django.contrib.auth.backends.ModelBackend',
    'allauth.account.auth_backends.AuthenticationBackend',
)

SOCIALACCOUNT_PROVIDERS = {
    'keycloak': {
        'KEYCLOAK_URL': "https://sso.grafcan.es/auth/realms/demo",
    }
}
```
