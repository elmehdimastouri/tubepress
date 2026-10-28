# TubePress

A self-hosted video-site CMS (PHP + MySQL/MariaDB): upload, import, transcode and
stream video, with a full admin, themes, plugins, SEO, ads and multi-language support.

## Install

You can install TubePress two ways — both run the exact same setup logic:

**1. Manually, in your browser (WordPress-style).** Point your web server's document
root at `public/`, make `config/`, `storage/` and `public/uploads/` writable, then open
`https://your-site/install` and follow the wizard.

**2. Automatically, from the command line** — for scripts and AI agents, no browser
needed:

```bash
php bin/install.php --check --json          # verify the environment
php bin/install.php \
  --db-name=tubepress --db-user=tubepress \
  --admin-email=admin@example.com --site-url=https://your-site \
  --json                                    # install (a strong admin password is generated)
```

The full, machine-readable deployment contract — every option, web-server config,
background jobs, verification and security notes — is in **[AGENTS.md](AGENTS.md)**.

## Requirements

PHP ≥ 8.2 with `pdo_mysql`, `mbstring`, `fileinfo`; a MySQL/MariaDB database; and
writable `config/`, `storage/`, `public/uploads/`. Recommended: `curl`, `zip`,
`gd`/`imagick`. No Composer step required. Run `php bin/install.php --check` to confirm.

## Updates

Apply signed core/plugin/theme updates from **Admin → Updates** (or enable opt-in
auto-update). Updates preserve your config, database, plugins and uploads.

## License

See [LICENSE.txt](LICENSE.txt).
"# tubepress" 
