# Email Deliverability Validation Checklist

A practical checklist to validate email configuration, authentication, and compliance.  
Use this guide to ensure reliable delivery and avoid spam filters.

---

## DNS & Authentication

- [ ] **SPF Record** → Verify existence and syntax (`v=spf1 include:... -all`).
- [ ] **DKIM Record** → Check public key in DNS and signing enabled on MTA.
- [ ] **DMARC Policy** → Ensure record exists (`p=none/quarantine/reject`) with reporting addresses.
- [ ] **Reverse DNS (PTR)** → Confirm IP resolves to mail server hostname.
- [ ] **MX Records** → Validate pointing to correct mail servers.

---

## SMTP & Server Configuration

- [ ] **SMTP Banner** → Matches domain name (avoid mismatched hostnames).
- [ ] **TLS/SSL** → Ensure STARTTLS enabled and valid certificate.
- [ ] **Authentication** → Test login with correct mechanisms (PLAIN, LOGIN, CRAM-MD5).
- [ ] **Rate Limits** → Confirm sending limits per hour/day are respected.

---

## Compliance & Reputation

- [ ] **Blacklist Check** → Verify IP/domain not listed in RBLs (Spamhaus, Barracuda, etc.).
- [ ] **Feedback Loops** → Register with major ISPs (Yahoo, AOL, Microsoft).
- [ ] **Postmaster Tools** → Configure Gmail Postmaster and Microsoft SNDS.
- [ ] **Content Compliance** → Test email headers, unsubscribe link, and GDPR/cookie compliance.

---

## Testing & Monitoring

- [ ] **Seed Tests** → Send to multiple providers (Gmail, Outlook, Yahoo, Apple Mail).
- [ ] **Spam Score** → Analyze with tools like Mail‑Tester or SpamAssassin.
- [ ] **Inbox Placement** → Validate if emails land in inbox vs. promotions/spam.
- [ ] **Reporting** → Collect DMARC aggregate reports and monitor deliverability trends.

---

**Tip:** Run this checklist before launching campaigns or onboarding new clients.  
It ensures technical compliance, protects sender reputation, and improves inbox placement.
