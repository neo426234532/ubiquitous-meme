# CF Optimizer → Phone Fixer

Simple client-side tool that takes the output from [arastey.github.io/cf-optimizor](https://arastey.github.io/cf-optimizor/) and makes it compatible with phone clients (Streisand, V2Box, etc.).

## Problem it solves

The Aras CF Optimizer sometimes adds these rules:

```
ext:geoip-only-cn-private.dat:private
ext:geoip-only-cn-private.dat:cn
```

Phone clients don't ship with `geoip-only-cn-private.dat`, so you get:

```
failed to open geoip-only-cn-private.dat → no such file or directory
```

This tool automatically replaces them with the standard tags every client has:

```
geoip:private
geoip:cn
```

## Usage

1. Open the live page (GitHub Pages link)
2. Paste the JSON from Aras Optimizer
3. Click **Fix for Phone**
4. Copy / download the result and import on your phone

Everything runs 100% in your browser. Nothing is uploaded.

## Live Demo

After you enable GitHub Pages, the link will be:

```
https://YOUR_USERNAME.github.io/REPO_NAME/
```

## License

MIT
