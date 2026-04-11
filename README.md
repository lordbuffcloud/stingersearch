# StingerSearch

Bee-themed Google dorking interface with visual query builder and 200+ pre-built dork templates.

Built by [CK42X](https://ck42x.com).

## Features

- **Visual Query Builder**: Click operators to assemble dorks, or type raw queries
- **19 Google Operators**: site, inurl, intitle, intext, filetype, ext, cache, related, info, allinurl, allintitle, allintext, AROUND(), before, after, OR, minus, exact phrase, wildcard
- **200+ Pre-built Templates** across 11 categories:
  - Files & Documents (SQL dumps, env files, SSH keys, backups)
  - Login Pages (WordPress, phpMyAdmin, VPN, Jenkins, Grafana)
  - Directory Listings (open dirs, FTP, git repos, uploads)
  - Configurations (wp-config, .htaccess, AWS creds, Firebase)
  - Databases (MySQL, MongoDB, Elasticsearch, Redis, CouchDB)
  - Cloud Storage (S3, Azure Blob, GCP, Firebase, Trello)
  - Cameras & IoT (Hikvision, Axis, RTSP, SCADA, printers)
  - Admin Panels (Django, Swagger, Docker, Kubernetes, Tomcat)
  - Error Pages (PHP, ASP.NET, Java, Django, Laravel)
  - Juicy Info (emails, financials, pentest reports, API keys)
  - Vulnerable Tech (Struts, IIS, phpinfo, SharePoint, JBoss)
- **Target Domain Binding**: Set a target and all templates auto-prepend `site:target`
- **Search History**: Saved to localStorage with timestamps
- **One-click Export**: Download filtered templates or history as text
- **Keyboard Shortcut**: Ctrl+Enter to execute search
- **Operator Tooltips**: Hover any operator for description + example
- **CK42X Branding**: Honey amber on matte black, Geist fonts

## Usage

Open `index.html` in any browser. No server required.

Or serve with any static file server:

```bash
npx serve .
```

## Security Notice

StingerSearch is a tool for **authorized security testing and OSINT research** only. Google dorking can reveal sensitive information. Use responsibly and only for legitimate purposes.

## License

MIT
