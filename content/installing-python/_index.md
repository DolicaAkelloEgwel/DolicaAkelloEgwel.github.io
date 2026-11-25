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

## uv

### Installing uv

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

### Basic Usage

#### Creating a New uv Project

To create a new Python project with uv, enter the following command in your terminal:

```bash
uv init --no-package YOUR-PROJECT-NAME
```

This will then create a folder with the following structure:

```tree
- YOUR-PROJECT-NAME | folder
  - .gitignore | file
  - .python-version | file
  - main.py | fa-fw fab fa-python
  - pyproject.toml | file
  - README.md | fa-fw fab fa-markdown
```

Enter the project folder in the terminal. This can be done with the command `cd YOUR-PROJECT-NAME`.

From there, you can run the file with the following command:

```bash
uv run main.py
```

#### Adding and Removing Libraries

As an example, let's add the [emoji](https://github.com/carpedm20/emoji/) library to the project.

Now **replace** the contents of your main.py file with the following:

```py {title="main.py"}
import emoji

print(emoji.emojize("Down the :rabbit: :hole:"))
```

Now run the code with the `uv run main.py` command. You will see the following in the terminal output:

```bash
ModuleNotFoundError: No module named 'emoji'
```

This is because we haven't yet told uv that the emoji library is a dependency for our project. But now we can do this with the following command:

```bash
uv add emoji
```

Now start the file again, and the code runs.

```bash
Down the 🐇 🕳️
```

If we realise that our project no longer needs a particular library then we can get rid of it with the remove command. Here is how we can remove the emoji library:

```bash
uv remove emoji
```

## pixi

### Installing pixi

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

### Basic Usage

#### Creating a New pixi Project

To create a new Python project with pixi, enter the following into your terminal:

```bash
pixi init YOUR-PROJECT-NAME
```

This will then create a folder with the following structure:

```tree
- YOUR-PROJECT-NAME | folder
  - .gitattributes | file
  - .gitignore | file
  - pixi.toml | file
```

Enter the project folder in the terminal. This can be done with the command `cd YOUR-PROJECT-NAME`.

Unlike uv, pixi will not create a main.py for you when you use its `init` command. This is because pixi is intended to manage projects that are not restricted to Python.

To add Python as a project requirement we use the following command:

```bash
pixi add python
```

#### Adding and Removing Libraries

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