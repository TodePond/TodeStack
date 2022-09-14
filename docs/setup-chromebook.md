# Chromebook Setup
## Step 1: Linux
Get a chromebook and enable linux in the settings.

## Step 2: Coder
Install Coder:
```
curl -fsSL https://code-server.dev/install.sh | sh
```
Check it's installed by attempting to open the editor:
```
code-server --auth none --open
```
Click the 'Install code-server' button in the address bar to open the editor as a native window. You can then pin it to the taskbar.<br>
Whenever you want to use the editor, run this command, and then click on your pinned shortcut!
```
code-server --auth none
```

If you want to **sync your settings** from the cloud, follow [this guide](/docs/coder-settings-sync.md).<br>
If you want to install the **TodePond colour theme**, follow [this guide](/docs/coder-todepond-theme.md).

## Step 3: Deno
Install Deno:
```
curl -fsSL https://deno.land/x/install/install.sh | sh
```
Add Deno to your path (replace `todepond` with your linux username):
```
echo 'export DENO_INSTALL="/home/todepond/.deno"' >> ~/.bashrc
```
```
echo 'export PATH="$DENO_INSTALL/bin:$PATH"' >> ~/.bashrc
```
Check it's installed:
```
deno --version
```

## Step 4: Frogasaurus
Install Frogasaurus:
```
deno install --allow-write=. --allow-read=. https://deno.land/x/frogasaurus/frogasaurus.js
```

## Step 5: File Server
Install File Server:
```
deno install --allow-read --allow-net https://deno.land/std/http/file_server.ts
```
