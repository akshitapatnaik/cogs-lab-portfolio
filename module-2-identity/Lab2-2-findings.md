# Lab 2-2 Findings – My Contribution

## Attribute Mapper Configuration

I configured SAML attribute mappers in Keycloak to send user information from the Identity Provider (IdP) to the Service Provider (SP).

Configured attributes:

- **email:** Sends the user's email address to the Service Provider.
- **groups:** Sends the user's group membership information.
- **Role:** Sends role information that can help the Service Provider identify user permissions.

These attributes help the Service Provider identify authenticated users and support access control.

## SAML SSO Configuration and Troubleshooting

During the implementation, I configured the SAML client in the `instasafe-lab` realm and connected it with the Flask Service Provider.

I downloaded the Keycloak IdP metadata XML file and configured the Service Provider settings, including the Entity ID and Assertion Consumer Service (ACS) URL.

During testing, I encountered a SAML validation error caused by duplicate `Role` attributes in the SAML response. I resolved this issue by enabling **Single Role Attribute** in the Keycloak Role List mapper.

I also checked connectivity between the E2E instance and Keycloak and resolved the connection issue by using the Keycloak server's private IP address and updating the required security group rule.

## Final Result

Successfully tested SAML Single Sign-On authentication between Keycloak and the Flask application.

After entering the test user's credentials, Keycloak authenticated the user and redirected the response back to the Flask Service Provider.

**Successful output:**

`Welcome! You are logged in. User: testuser`

This confirms that the SAML authentication flow between the Identity Provider and Service Provider is working successfully.
