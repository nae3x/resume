# Resume

Personal resume site, deployed via GitHub Pages at <https://nae3x.github.io/resume/>.

## Local development (hot reload)

Start the live-reload server on port 8080:

```sh
npx live-server --no-browser --port=8080
```

Open <http://127.0.0.1:8080> in a browser. Edits to `index.html` reload automatically.

### Stop

If running in the foreground, press `Ctrl+C` in that terminal.

If you launched it in the background and lost the terminal, kill it by port or name:

```sh
pkill -f live-server
# or, find and kill the PID using port 8080:
lsof -i :8080
```

## Deploy

Pushes to `main` rebuild GitHub Pages automatically:

```sh
git add <files>
git commit -m "..."
git push
```

Check build status:

```sh
gh api /repos/nae3x/resume/pages/builds/latest --jq '.status'
```
