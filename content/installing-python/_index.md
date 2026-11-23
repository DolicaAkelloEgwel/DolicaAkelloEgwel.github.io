+++
title = "Installing Python"
type = "chapter"
weight = 1
+++

## Reproducible Python

### Why Reproducibility Matters

When starting a new Python project, it's a good idea to think early on about the machine that will eventually run your code. A project that works perfectly on your personal laptop may be difficult or even impossible to get running on an exhibition computer. Ensuring that a project can easily be installed on different systems and behaves consistently across different systems is known as *reproducibility*.

To understand why reproducibility matters, it helps to know what *dependencies* and *environments* are. Dependencies are the external libraries your project relies on, such as `numpy`, `opencv-python`, or `pygame`. An environment is the complete collection of software needed to run your project, including the Python version and the specific versions of those dependencies. If another machine has different versions installed, or is missing a dependency entirely, your code may behave differently or fail to run at all.

Tools such as `uv` and `pixi` help solve this problem by managing dependencies and environments in a way that allows them to be reliably recreated on different systems. Spending a little time setting these tools up at the beginning of a brand new project can save a lot of headache later on.

### uv or pixi



## Installing uv

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

## Installing pixi

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