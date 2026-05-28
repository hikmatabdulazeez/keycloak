cat > README.md <<'EOF'
# Implementing TLS, SSO, and Vault with Keycloak

**Business College Helsinki— May 2026**

## Overview
A hands-on lab implementing a production-grade IAM stack on Ubuntu using:
- Keycloak 26.3.4 (Identity Provider)
- MicroK8s + Kubernetes Dashboard
- HashiCorp Vault (Secrets Management)
- OpenID Connect (OIDC) for SSO

## What Was Implemented
1. Keycloak installed and verified
2. Self-signed TLS certificate with SAN generated via OpenSSL
3. HTTPS enforced on port 8443, HTTP disabled
4. Keycloak started in dev mode
5. Keycloak accessible at https://localhost:8443
6. SSO realm (HikkySSO), users, and OIDC client created
7. MicroK8s and Kubernetes Dashboard deployed
8. Kubernetes API server configured to trust Keycloak (OIDC)
9. Dashboard patched to authenticate via Keycloak
10. OIDC authentication confirmed
11. Kubernetes Dashboard tested in Firefox
12. HashiCorp Vault installed and integrated with Keycloak via OIDC

## Tools Used
- Ubuntu 24.04 (VMware Workstation)
- Keycloak 26.3.4
- OpenSSL
- MicroK8s v1.30
- HashiCorp Vault
- Firefox
- Bash / Terminal

## Architecture
Keycloak acts as the central identity provider. The Kubernetes API server and HashiCorp Vault both delegate authentication to Keycloak via OIDC, creating a single sign-on experience across all services.
EOF# keycloak
