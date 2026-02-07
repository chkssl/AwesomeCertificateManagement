# Awesome Certificate Management [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, libraries, and resources for Certificate Lifecycle Management (CLM), SSL/TLS monitoring, and automated trust.

In 2026, the industry officially shifted to a **200-day maximum certificate lifespan**. By 2029, we are looking at **47-day** validity periods. In this new reality, manual tracking is technical debt, and "set-and-forget" automation is a single point of failure. This list focuses on the ecosystem required to maintain 100% uptime in the era of short-lived certificates.

## Contents

- [Monitoring & Observability](#monitoring--observability)
- [Automation & Issuance](#automation--issuance)
- [Discovery & Inventory](#discovery--inventory)
- [CLI Tools](#cli-tools)
- [Developer Libraries](#developer-libraries)
- [Compliance & Policy](#compliance--policy)
- [Articles & Trends](#articles--trends)

---

## Monitoring & Observability
*External verification tools to ensure your internal automation didn't silently fail.*

* [chkssl.com](https://chkssl.com) - Resilient, multi-region SSL monitoring designed for the high-velocity 47-day certificate era.
* [Checkly](https://www.checklyhq.com/) - Synthetic monitoring that includes SSL expiry and chain validation.
* [Blackbox Exporter](https://github.com/prometheus/blackbox_exporter) - The standard for Probing endpoints via HTTP, DNS, TCP, and ICMP, including SSL/TLS metrics for Prometheus.
* [SSL Labs Server Test](https://www.ssllabs.com/ssltest/) - Deep analysis of the configuration of any SSL web server.

## Automation & Issuance
*Tools to handle the high-frequency rotation of short-lived certificates.*

* [cert-manager](https://cert-manager.io/) - Native Kubernetes certificate management controller. It can help with issuing certificates from a variety of sources.
* [Lego](https://github.com/go-acme/lego) - A Let's Encrypt client and ACME library written in Go.
* [acme.sh](https://github.com/acmesh-official/acme.sh) - A pure Unix shell script implementing ACME client protocol.
* [Step-ca](https://github.com/smallstep/certificates) - A private CA and PKI toolset for internal service-to-service encryption (mTLS).

## Discovery & Inventory
*Find the "shadow" certificates and forgotten subdomains across your infrastructure.*

* [crt.sh](https://crt.sh) - A web interface for searching Certificate Transparency (CT) logs.
* [Censys](https://censys.io/) - Attack surface management that continuously maps public-facing certificates.
* [Cloudflare SSL/TLS Recommender](https://www.cloudflare.com/ssl-overview/) - Tooling to discover and optimize encryption settings across managed domains.

## CLI Tools
* [testssl.sh](https://testssl.sh/) - A free command line tool which checks a server's service on any port for support of TLS/SSL ciphers and vulnerabilities.
* [OpenSSL](https://www.openssl.org/) - The industry-standard open-source toolkit for the TLS and SSL protocols.
* [CFSSL](https://github.com/cloudflare/cfssl) - Cloudflare's PKI and TLS toolkit.

## Developer Libraries
*Build your own monitoring or issuance logic.*

* [Go crypto/tls](https://pkg.go.dev/crypto/tls) - The standard Go package for TLS 1.2 and 1.3.
* [Rustls](https://github.com/rustls/rustls) - A modern, safe, and fast TLS library written in Rust.
* [PyOpenSSL](https://github.com/pyca/pyopenssl) - Python wrapper around the OpenSSL library.

## Compliance & Policy
* [ZLint](https://github.com/zmap/zlint) - A Go-based X.509 certificate linter that checks for consistency with standards (RFC 5280) and CA/Browser Forum Baseline Requirements.
* [Mozilla SSL Configuration Generator](https://ssl-config.mozilla.org/) - An interactive tool to help you generate secure TLS configurations for common servers.

## Articles & Trends
*Reading material on the shifting landscape of PKI and CLM.*

* [Certificate Life Cycle Management: Trends to Watch in 2026](https://securityboulevard.com/2026/01/certificate-life-cycle-management-emerging-trends-to-watch-in-2026/) - Why 2026 is the turning point for automated visibility.
* [Moving Forward, Together (Google Chromium)](https://www.chromium.org/Home/chromium-security/root-ca-policy/moving-forward-together/) - The roadmap for 90-day (and eventually shorter) certificate validity.
* [The 47-Day SSL/TLS Validity Roadmap](https://certera.com/blog/ca-b-approved-47-day-ssl-tls-validity-by-2029/) - A technical breakdown of the upcoming CA/B Forum changes.

---

## Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingResource`)
3. Commit your Changes (`git commit -m 'Add some AmazingResource'`)
4. Push to the Branch (`git push origin feature/AmazingResource`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.