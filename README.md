# Okteto + Keycloak to enable SAML authentication

This  is an experiment on how to use KeyCloak to enable SAML 2.0 authentication in Okteto

## How to?
1. Install Okteto Self-Hosted in your Kubernetes cluster
2. Install Keycloak on your cluster (you can use docker-compose + the okteto CLI to deploy it in your cluster ;) )
3. Create a Keycloak client of type Open ID 2.0 Connect
4. [Configure your Okteto instance to use Keycloak as the Open ID 2.0 Connect auth provider](https://www.okteto.com/docs/self-hosted/install/auth/openid-connect/)
5. Connect your SAML 2.0 authentication provider with Keycloak ([I followed this guide to use Okta](https://ultimatesecurity.pro/post/okta-saml/))
6. Log in to Okteto

When you log in to Okteto, Oketo will pop up the Keycloak authentication UI. There, you can click on "Or Log in with XXX" button to log in with your SAML provider. If everything is configured correctly, the flow will end with you logged into the Okteto UI.
