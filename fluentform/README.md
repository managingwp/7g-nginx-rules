# Fluent Forms exclusions

This rule adds an exclusion for the Fluent Forms entries CSV export action in WordPress admin.

The rule creates an exemption for requests that match **both** of these conditions:
- The path is `/wp-admin/admin-ajax.php`.
- The querystring includes `action=fluentform-form-entries-export` as an exact parameter.

## 7g Error

```
[23/Feb/2026:14:24:11 +0000] [":bad_querystring_36:"] 32.211.206.143 domain.com "GET /wp-admin/admin-ajax.php?action=fluentform-form-entries-export&form_id=9&format=csv&entry_type=&sort_by=DESC&search=&fields_to_export=%5B%22names%22%2C%22email%22%2C%22checkbox%22%2C%22checkbox_3%22%2C%22checkbox_2%22%5D&shortcodes_to_export%5B0%5D%5Blabel%5D=Submission%20ID&shortcodes_to_export%5B0%5D%5Bvalue%5D=%7Bsubmission.id%7D&shortcodes_to_export%5B1%5D%5Blabel%5D=Submission%20Create%20Date&shortcodes_to_export%5B1%5D%5Bvalue%5D=%7Bsubmission.created_at%7D&shortcodes_to_export%5B2%5D%5Blabel%5D=Submission%20Status&shortcodes_to_export%5B2%5D%5Bvalue%5D=%7Bsubmission.status%7D&fluent_forms_admin_nonce=9755fbb050 HTTP/2.0" 403 0.000 "https://domain.com/wp-admin/admin.php?page=fluent_forms&form_id=9&route=entries" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:147.0) Gecko/20100101 Firefox/147.0"
```

## Credit

- jtrask
