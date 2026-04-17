# StingerSearch

Bee-themed Google dorking interface with visual query builder, 220+ pre-built dork templates with per-dork explanations, and an AI-powered custom dork generator.

Built by [CK42X](https://ck42x.com).

## Features

- **Visual Query Builder**: Click operators to assemble dorks, or type raw queries
- **19 Google Operators**: site, inurl, intitle, intext, filetype, ext, cache, related, info, allinurl, allintitle, allintext, AROUND(), before, after, OR, minus, exact phrase, wildcard
- **220+ Pre-built Templates** across 15 categories:
  - Files & Documents (env files, SSH keys, AWS creds, GCP service accounts, keystores, Postman collections)
  - Login Pages (WordPress, phpMyAdmin, VPN, Jenkins, Grafana, ServiceNow, Okta, vCenter, FortiGate)
  - Directory Listings (open dirs, FTP, git repos, node_modules, composer vendor, build output)
  - Configurations (wp-config, .htaccess, Firebase, AWS, GitLab CI, CircleCI, Jenkinsfile, netlify.toml)
  - Databases (MySQL, MongoDB, Elasticsearch, Redis, InfluxDB, Neo4j, Supabase anon keys)
  - Cloud Storage (S3, Azure Blob, GCP, Firebase, Cloudflare R2, Backblaze, Lambda URLs, ngrok)
  - Cameras & IoT (Hikvision, Axis, Dahua, Home Assistant, Octoprint, SCADA/ICS)
  - Admin Panels (Django, Swagger, Docker, Kubernetes, Tomcat, Vault, Consul, Rundeck, Harbor, Gitea)
  - Error Pages (PHP, ASP.NET, Java, Django, Laravel, Rails, Go, Python, Node)
  - Juicy Info (emails, financials, pentest reports, API keys, Zoom recordings, Slack exports)
  - Vulnerable Tech (Log4Shell, Spring4Shell, ProxyShell, Ivanti, F5 iControl, Jira RCE, ColdFusion)
  - OSINT / Recon (LinkedIn by role, GitHub by company, public resumes, court records, tenders)
  - Bug Bounty (subdomain enumeration, staging domains, GraphQL, sourcemaps, Lambda endpoints)
  - CVE Fingerprints (Confluence, MOVEit, Fortinet, Citrix Bleed, Exchange, ScreenConnect)
  - Gov / Edu (.gov FOUO, .edu dumps, .mil publics, RFP/RFQ, emergency plans)
- **Per-Dork Explanations**: Every template has a "Learn more" toggle explaining how the operators work, what you'll find, risk notes, and defender tips
- **AI Dork Generator**: Describe what you're hunting for in plain English. Claude Haiku (or Sonnet) drafts a Google dork using standard operators, with a full explanation. BYO Anthropic API key, stored locally in your browser only. Refuses obviously unethical requests (targeting specific people, breaking into named systems).
- **Custom Template Library**: Save AI-generated dorks to a local "Custom" category for reuse
- **Target Domain Binding**: Set a target and all templates auto-prepend `site:target`
- **Search History**: Saved to localStorage with timestamps
- **One-click Export**: Download filtered templates (with explanations) or history as text
- **Keyboard Shortcut**: Ctrl+Enter to execute search, Escape to close modals
- **Operator Tooltips**: Hover any operator for description + example
- **CK42X Branding**: Honey amber on matte black, Geist fonts

## AI Dork Generator Setup

1. Get an Anthropic API key: https://console.anthropic.com/settings/keys
2. Click the gear icon in the top-right of StingerSearch.
3. Paste your key. It is stored in browser localStorage only, scoped to this origin. No backend.
4. Click "✨ AI Dork" to open the generator. Type a plain-English hunt (e.g. "find exposed prometheus metrics on .edu" or "Firebase databases with public read access") and hit Generate.
5. The model returns a name, the dork itself, a one-line description, and an explanation of how the operators work and what results look like. Click "Use this dork" to load it into the query builder or "Save to Custom" to keep it.

Safety: the system prompt forbids person-targeting and unauthorized-system breaking. Treat the output as a suggestion, not a blanket license. Run only within authorized scope.

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
