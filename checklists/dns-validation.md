# DNS Validation Checklist

A practical checklist to validate DNS configuration for websites, email deliverability, and security.

---

## Basic Records

- [ ] A Record → Points domain to correct server IP.  
- [ ] AAAA Record → IPv6 address configured if required.  
- [ ] CNAME Record → Aliases resolve correctly (e.g., www → root domain).  
- [ ] MX Records → Point to correct mail servers with proper priority.  

---

## Email Authentication

- [ ] SPF Record → Syntax valid, includes authorized senders, ends with `-all` or `~all`.  
- [ ] DKIM Record → Public key published in DNS, signing enabled on mail server.  
- [ ] DMARC Record → Policy set (`none`, `quarantine`, or `reject`) with reporting addresses.  
- [ ] PTR Record → Reverse DNS resolves to mail server hostname.  

---

## Security & Compliance

- [ ] DNSSEC → Enabled and validated for domain.  
- [ ] TLSA Record → Configured if using DANE for email security.  
- [ ] CAA Record → Restricts which Certificate Authorities can issue SSL/TLS certificates.  

---

## Performance & Redundancy

- [ ] Multiple NS Records → At least two authoritative name servers configured.  
- [ ] Geo‑distribution → Name servers spread across regions for resilience.  
- [ ] TTL Values → Optimized for balance between caching and flexibility.  

---

## Monitoring & Maintenance

- [ ] Regular Audits → Review DNS records at least quarterly.  
- [ ] Change Logs → Document updates for traceability.  
- [ ] Alerts → Monitor for unauthorized changes or propagation issues.  

---

**Tip:** Run this checklist during new deployments, migrations, or email onboarding to ensure DNS integrity and reliable service.
