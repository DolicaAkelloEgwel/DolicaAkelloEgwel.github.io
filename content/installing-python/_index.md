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

Now open a new terminal, and check that the install was successful by entering the following command:
```bash
uv --version
```

## Installing `pixi`

{{< tabs >}}
{{% tab title="macOS / Linux" %}}
Enter the following in the terminal to install with `curl`:
```bash
curl -fsSL https://pixi.sh/install.sh | sh
```
Enter the following into the terminal to install with `wget`:
```bash
curl -fsSL https://pixi.sh/install.sh | sh
```
{{% /tab %}}
{{% tab title="Windows" %}}
pixi may be installed in the terminal with [Scoop](https://scoop.sh/):
```pwsh
scoop install main/pixi
```
{{% /tab %}}
{{< /tabs >}}

Now open a new terminal, and check that the install was successful by entering the following command:
```bash
pixi --version
```

## Further Info