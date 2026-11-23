+++
title = "Installing Python"
type = "chapter"
weight = 1
+++

## Environments and Portable Python

## Installing `uv`

{{< tabs >}}
{{% tab title="macOS / Linux" %}}
Enter the following in the terminal to install with `curl`:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
Enter the following into the terminal to install with `wget`:
```bash
wget -qO- https://astral.sh/uv/install.sh | sh
```
{{% /tab %}}
{{% tab title="Windows" %}}
uv may be installed in the terminal with [Scoop](https://scoop.sh/):
```pwsh
scoop install main/uv
```
{{% /tab %}}
{{< /tabs >}}

## Installing `pixi`

## Further Info