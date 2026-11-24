+++
title = "Installing Python"
type = "chapter"
weight = 1
+++

## Reproducible Python

### Why Reproducibility Matters

When starting a new Python project, it's a good idea to think early on about the machine that will eventually run your code. A project that works perfectly on your personal laptop may be difficult or even impossible to get running on an exhibition computer. Ensuring that a project can easily be installed on different systems and behaves consistently across those different systems is known as *reproducibility*.

To understand why reproducibility matters, it helps to know what *dependencies* and *environments* are. Dependencies are the external libraries your project relies on, such as numpy, opencv-python, or pygame. An environment is the complete collection of software needed to run your project, including the Python version and the specific versions of those dependencies. If another machine has different versions installed, or is missing a dependency entirely, your code may behave differently or fail to run at all.

Tools such as `uv` and `pixi` help solve this problem by managing dependencies and environments in a way that allows them to be reliably recreated on different systems. Spending a little time setting these tools up at the beginning of a brand new project can save you (and us CTH technicians) from a lot of headache later on.

### uv or pixi

While both uv and pixi are excellent tools, the one that's best for you depends on the type of project you're building.

If you're using Python for AI/ML projects, or for tasks such as video generation and processing, pixi is generally the better choice. Unlike uv, pixi can manage dependencies that aren't limited to Python packages, making it well suited to projects that rely on external libraries, system packages, or specialised tooling.

For many other Python projects, uv will be more than sufficient. You may also start with uv and switch to pixi later if your project's requirements become more complex. This website includes examples configured with both uv and pixi, so if you'd like to explore all of the projects featured here, it's worth installing both.

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

## VS Code Extensions

### Python

If you use Visual Studio Code it helps to have the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) installed. One way of installing this is through the terminal with the following command:
```bash
code --install-extension ms-python.python
```

### Pixi

You may also find the [Pixi extension](https://marketplace.visualstudio.com/items?itemName=renan-r-santos.pixi-code) useful. This can also be installed with the terminal:
```bash
code --install-extension renan-r-santos.pixi-code
code --enable-proposed-api renan-r-santos.pixi-code
``` 

## Further Info

- [**uv Handbook**](https://pydevtools.com/handbook/topics/uv/) - Information on basic uv usage.
- [**Why should I use a virtual environment?**](https://pydevtools.com/handbook/explanation/why-should-i-use-a-virtual-environment/) - Explains the advantages of using Python environments.
- [**Why should I avoid using the system Python?**](https://pydevtools.com/handbook/explanation/why-should-i-avoid-system-python/) - Related to the issue of environments. Explains why using the "default" Python for your own projects should be avoided.
- [**Python package managers: uv vs pixi?**](https://jacobtomlinson.dev/posts/2025/python-package-managers-uv-vs-pixi/) - An overview of Python package managers and a comparison between uv and pixi.
- [**When should I choose pixi over uv?**](https://pydevtools.com/handbook/explanation/when-should-i-choose-pixi-over-uv/) - Another comparison that gives information to help you understand when to use pixi over uv or vice versa.