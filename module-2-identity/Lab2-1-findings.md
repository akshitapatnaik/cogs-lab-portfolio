# Lab 2.1 – OpenLDAP Fundamentals

## Objective
The main objective of this lab was to install OpenLDAP, create users and test user authentication.

## Environment
- OS: Ubuntu on AWS
- LDAP Domain: `lab.instasafe.local`

## LDAP Concepts and InstaSafe AD Sync

| LDAP Concept | My Lab Example | InstaSafe Equivalent |
|---|---|---|
| Base DN | `dc=lab,dc=instasafe,dc=local` | Starting location to search users |
| Bind DN | `cn=admin,dc=lab,dc=instasafe,dc=local` | Account used to connect to LDAP/AD |
| User DN | Alice's full LDAP address | Identifies a user in the directory |
| Attributes | `cn`, `uid`, `mail` | User details that can be synchronized |

## What I Did in This Lab

1. First, I installed OpenLDAP and LDAP utilities on Ubuntu.
2. Then, I configured the LDAP domain and organization name.
3. I created two users, Alice and Bob, and organized them under the People OU.
4. I used `ldapadd` to add users to the LDAP directory.
5. I used `ldapsearch` to check whether both users were created successfully.
6. Finally, I used `ldapwhoami` to test authentication with the correct and incorrect passwords.

## Validation

- `ldapsearch` successfully displayed both Alice and Bob.
- When I used Alice's correct password, LDAP authentication was successful.
- When I used the wrong password, LDAP showed Error 49 (Invalid credentials).

## Conclusion

Through this lab, I learned how OpenLDAP stores user information and checks user credentials. I also understood how InstaSafe can connect with an organization's LDAP or Active Directory to search and synchronize users and groups. This helps in managing user identity and access.
