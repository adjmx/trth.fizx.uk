# trth.fizx.uk

> Nostr-powered debate — submit statements, vote with sats, let the truth win.

**Live**: <https://trth.fizx.uk>

## Stack

- [Vite](https://vitejs.dev/) + React 18 + TypeScript
- Tailwind CSS
- [nostr-tools](https://github.com/nbd-wtf/nostr-tools)
- lucide-react

## Nostr

- **Login**: NIP-07 (browser extension) + NIP-55 (Amber callback URI)
- `kind:30078` — NIP-78 app-specific data — challenge / debate state (tagged `#t: truthstakes`)
- `kind:1` — replies + arguments

## Develop

```bash
npm install
npm run dev
```

## Build + deploy

```bash
npm run build
rsync -avz --delete -e "ssh -p 2121" dist/ root@88.218.206.187:/var/www/trth.fizx.uk/
```

VPS: `88.218.206.187`. Full server / nginx / SSL / DNS notes for the wider deployment live in the local `code_vibe/CLAUDE.md` (not pushed; this README is the public-facing summary).

---

_Sister repo on the other side: <https://github.com/macos-node/trth.upleb.uk>_
