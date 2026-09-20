Dimensional Experimental Installer 

```sh
bash <(curl -fsSL https://pub-4767fdd15e6a41b6b2ce2558d71ec8d9.r2.dev/install.sh) \
  --non-interactive --mode dev --no-nix \
  --project-dir "$HOME/dim-app" --extras base,unitree --branch main
```

## DimOS Desktop

With nix:

```sh
nix profile install github:jeff-hykin/dimos-desktop
dimos-desktop-service        # boot service; serves http://127.0.0.1:1024/
```

Without nix (needs git):

```sh
curl -fsSL https://deno.land/install.sh | sh
git clone https://github.com/jeff-hykin/dimos-desktop ~/dimos-desktop
cd ~/dimos-desktop && ~/.deno/bin/deno task service
```

## Go2 controller

```sh
dim install https://github.com/jeff-hykin/dim-go2-dash
```

Then open **Go2 Dash** in the desktop and press **Scan**. On macOS the first scan pops a
"deno would like to use Bluetooth" dialog on the machine's own screen — click Allow.
