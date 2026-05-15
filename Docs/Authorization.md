# Authorization

## 🔐 Authorization Model

Sensei uses RID-based group validation to avoid localization issues.

Role	RID
Domain Admins	512
Enterprise Admins	519

This ensures compatibility across:
- English domains
- German domains (e.g. Domänen-Admins)
- Any localized AD environment
