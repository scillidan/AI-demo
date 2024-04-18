## Vercel

Just use [Vercel](https://vercel.com/).

## Localhost

```sh
pnpm install
pnpm build
```

Edit `package.json`:

```json
  "scripts": {
	...
    "start": "next start -p 4321",
    ...
  },
```

```sh
pnpm start
```

## PM2 (Error)

```sh
pm2 start "C:/Users/YourName/AppData/Roaming/pnpm/global/5/node_modules/next/dist/bin/next" --interpreter "C:/Users/YourName/AppData/Roaming/fnm/node-versions/v18.19.1/installation/node.exe" -n lobe-chat -- dev -p 8030
```