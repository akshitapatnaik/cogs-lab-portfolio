# Lab 1.2 Findings

## Objective

Configured HTTPS on an Nginx web server using a self-signed TLS certificate and verified secure communication.

## Steps Performed

- Installed and configured Nginx.
- Created a custom web page.
- Configured firewall access for ports **22**, **80**, and **443**.
- Generated a self-signed TLS certificate using OpenSSL.
- Configured Nginx for HTTPS using TLS 1.2 and TLS 1.3.
- Verified HTTPS using `curl` and `openssl`.

## Certificate Analysis

- **Type:** Self-Signed X.509
- **Subject/CN:** 15.134.223.31
- **Issuer:** Self-Signed (InstaSafe Lab)
- **Validity:** 08 Nov 2026 – 08 Nov 2027
- **Public Key:** RSA 2048-bit
- **Signature Algorithm:** SHA256 with RSA

## Observations

- HTTP and HTTPS were working successfully.
- HTTPS used a self-signed certificate.
- `curl` without `-k` showed a certificate warning because the certificate was not issued by a trusted Certificate Authority (CA).
- `curl -k` successfully accessed the HTTPS webpage by skipping certificate verification.
- TLS 1.1 was disabled (`no protocols available`), while TLS 1.2 and TLS 1.3 were configured in Nginx.

## Why Does curl Without -k Fail?

- The certificate is self-signed and not issued by a trusted Certificate Authority (CA).
- Curl cannot verify the certificate against its trusted CA list.
- The `-k` option skips certificate verification and allows the connection.
- To make it succeed without `-k`, we need a certificate issued by a trusted CA, or explicitly configure the client to trust our self-signed certificate.

## Conclusion

Successfully configured HTTPS on an Nginx web server using a self-signed TLS certificate. Verified secure communication and inspected certificate details using `curl` and `openssl`. Learned how TLS certificates establish server identity and why trusted certificates are important for secure communication.
