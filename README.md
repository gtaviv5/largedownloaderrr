Downloader
=========
A simple downloader to download large files.

![Downloader](cover.png)

<p align="center">
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square" alt="Software License" />
  </a>
  <a href="https://github.com/znck/downloader/releases">
    <img src="https://img.shields.io/github/release/downloader/plug.svg?style=flat-square" alt="Latest Version" />
  </a>

  <a href="https://github.com/znck/downloader/issues">
    <img src="https://img.shields.io/github/issues/znck/downloader.svg?style=flat-square" alt="Issues" />
  </a>
</p>


## How to install?

Run this in your terminal to get the latest Downloader version:
```bash
curl -sS https://raw.githubusercontent.com/znck/downloader/master/install.sh | sudo -E bash
```

## How to use?

Downloader has simple command line interface.

```bash
downloader <url> [<chunk size>] [<filename>]
```

Default chunk size is 128mb but you can change it by a line to your `.bashrc` file

```bash
echo "export downloader_chunk_size=10" > "$HOME/.bashrc" # This will set chunk size to 10mb.
```
Default output directory is `~/Downloads` and you change this too.

```bash
echo "export downloader_output_dir=$HOME/Documents" > "$HOME/.bashrc"
```

## Proxy settings
Downloader uses cURL to fetch chunks and cURL respects environment proxy variables.

```bash
echo "export http_proxy=http://<proxy_server>:<proxy_port>" > "$HOME/.bashrc"
echo "export https_proxy=https://<proxy_server>:<proxy_port>" > "$HOME/.bashrc"

# For authenticated proxies
echo "export http_proxy=http://<username>:<password>@<proxy_server>:<proxy_port>" > "$HOME/.bashrc"
echo "export https_proxy=https://<username>:<password>@<proxy_server>:<proxy_port>" > "$HOME/.bashrc"
```
