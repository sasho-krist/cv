# CV — Aleksander Keremidarov

Single-page CV (Claude Design export bundle) served at
<https://sasho-dev.com/CV/>.

- `index.php` — the whole page (self-contained design bundle).
- `ask-cv.php` — small PHP proxy for the "Ask this CV" widget. **Not in git**
  (it must never contain a key). Copy `ask-cv.php.example` to `ask-cv.php` on the
  server and set `ANTHROPIC_API_KEY` in the server environment.

## Deploy

```bash
cd ~/public_html/CV
git pull
```

First-time setup on the server:

```bash
cd ~/public_html/CV
git init -b main
git remote add origin https://github.com/sasho-krist/cv.git
git fetch origin
git reset --hard origin/main   # untracked ask-cv.php is left untouched
```
