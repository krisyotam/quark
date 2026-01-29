# Kris's build of quark

My build of [quark](https://tools.suckless.org/quark/), an extremely small and simple HTTP GET/HEAD-only web server for static content.

---

## About

quark is a tiny, secure HTTP server from suckless.org designed to serve static files with minimal attack surface.

---

## Features

- **Minimal**: Tiny codebase, easy to audit
- **Secure**: Privilege separation, chroot support
- **Fast**: Event-driven architecture
- **Standards**: HTTP/1.1 compliant (GET/HEAD only)
- **Virtual hosts**: Support for multiple domains
- **TLS**: Optional TLS support

---

## Usage

```bash
# Serve current directory on port 8080
quark -p 8080 -d /var/www/html

# With virtual hosts
quark -p 80 -d /var/www -v vhosts.conf

# With chroot (as root)
quark -p 80 -d /var/www -u nobody -g nogroup
```

### Options

| Flag | Description |
|------|-------------|
| `-d` | Document root directory |
| `-p` | Port to listen on |
| `-h` | Host/IP to bind to |
| `-u` | User to drop privileges to |
| `-g` | Group to drop privileges to |
| `-v` | Virtual hosts config file |
| `-l` | Enable directory listing |

---

## Installation

```bash
git clone https://github.com/krisyotam/quark
cd quark
sudo make install
```

---

## Other Suckless Repos

- [dwm](https://github.com/krisyotam/dwm) - dynamic window manager
- [st](https://github.com/krisyotam/st) - simple terminal
- [dmenu](https://github.com/krisyotam/dmenu) - dynamic menu
- [dwmblocks](https://github.com/krisyotam/dwmblocks) - modular status bar
- [scron](https://github.com/krisyotam/scron) - simple cron daemon

---

## Contact

- Kris Yotam <krisyotam@protonmail.com>
- [https://krisyotam.com](https://krisyotam.com)
