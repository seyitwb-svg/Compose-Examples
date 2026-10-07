# References

- https://github.com/seyitwb-svg/qrdock
- https://seyitwb-svg.github.io/qrdock/

# Notes

QRDock is a self-hosted QR code generator where every code is a short link you control. Printed codes stay retargetable — change the destination URL anytime without reprinting. It includes per-link scan analytics, a 14-day scan chart, PNG/SVG export, an instant anonymous QR endpoint (`/qr.png?text=...`), and Pro custom colors (`?fg=`). Runs on Python + FastAPI + SQLite in ~50 MB RAM.

### Spawning up QRDock

1. Start the stack: `docker compose up -d` — the image builds from the GitHub repo on first run (~1 min).
2. Open `http://localhost:8128` (or `qrdock.example.com` with Traefik), register an account, and create your first link.
3. Print the PNG/SVG QR code; retarget its destination later from the dashboard.

> [!NOTE]
> No build context needed locally — Compose pulls the Dockerfile straight from the repo. To pin a release, replace the `build:` context with `https://github.com/seyitwb-svg/qrdock.git#v1.0.0`.
