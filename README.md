# Yali-Red
Yali-Red/
├─ yali_red/
│  ├─ __init__.py
│  ├─ cli.py                # CLI entrypoint (click/argparse)
│  ├─ config.py             # central config (targets, api keys, couchdb)
│  ├─ db.py                 # CouchDB wrapper
│  ├─ discovery/
│  │  ├─ subdomain.py       # subdomain enumeration + metadata (IP,status,title)
│  │  ├─ endpoints.py       # endpoints discovery & parameter extraction
│  │  └─ js_extract.py      # JavaScript extraction helpers
│  ├─ scanners/
│  │  ├─ portscan.py        # nmap wrapper
│  │  ├─ nuclei_runner.py   # runs nuclei templates
│  │  ├─ ffuf_runner.py     # fuzzing wrapper (custom wordlists)
│  │  ├─ takeover.py        # subdomain takeover checks
│  │  └─ vulnscan.py        # CVE scanning wrapper (e.g. vuln scanners)
│  ├─ enrich/
│  │  ├─ favicon.py         # favicon hash logic
│  │  ├─ cors_crlf.py       # CORS & CRLF checks
│  │  └─ shodan.py          # shodan queries
│  ├─ utils/
│  │  ├─ http.py            # requests wrappers, title extraction
│  │  ├─ parser.py          # extract parameters, endpoints, secrets
│  │  └─ wordlist_gen.py    # generate custom target-based wordlists
│  └─ monitor/
│     ├─ monitor.py         # scheduler + 24/7 monitors for subdomains & JS
│     └─ watchers.py        # specific watchers (subdomains, js files)
├─ examples/
│  └─ run_demo.py
├─ requirements.txt
├─ pyproject.toml
└─ .devcontainer/...

