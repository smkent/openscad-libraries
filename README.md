# Third-party libraries for OpenSCAD

A collection of third-party [OpenSCAD libraries][openscad-libraries] as
[git submodules][git-submodules].

## Installation

The easiest way to use this repository is to clone it to the OpenSCAD library
path on your system.

[OpenSCAD's library path][openscad-libraries] is operating system dependent:

| OS | Path |
|--- |--- |
| Linux | `$HOME/.local/share/OpenSCAD/libraries` |
| Mac OS X | `$HOME/Documents/OpenSCAD/libraries` |
| Windows | `My Documents\OpenSCAD\libraries` |

To install, first clone the git repository as a directory called `libraries`:

```console
git clone https://github.com/smkent/openscad-libraries libraries
```

Next, initialize all of the library submodules within the new `libraries`
directory:

```console
cd libraries
git submodule update --init
```

Finally, move the repository `libraries` directory to the OpenSCAD libraries
path for your operating system (listed above).

### Alternative methods

If you want to place libraries elsewhere or already have an existing OpenSCAD
libraries directory, you can configure OpenSCAD with alternative or additional
libraries directories. [See the OpenSCAD documentation][openscad-libraries] for
more information.

## Usage as a submodule

This repository may itself be used as a submodule. For example,
[smkent/monoscad][monoscad] uses this repository as a submodule to bundle
models with their libraries.

To use, first add this repository as a new submodule:

```console
cd your-project
git submodule add https://github.com/smkent/openscad-libraries
```

Add and commit `.gitmodules` in your repository:

```console
git add .gitmodules
git commit -m "Add openscad-libraries submodule"
```

Finally, initialize openscad-libraries along with all child submodule contents:

```console
git submodule update --init --recursive
```

The above command should also be performed in new clones of your project
repository.

## License

Third party libraries have their own licenses.


[git-submodules]: https://git-scm.com/book/en/v2/Git-Tools-Submodules
[monoscad]: https://github.com/smkent/monoscad
[openscad-libraries]: https://en.wikibooks.org/wiki/OpenSCAD_User_Manual/Libraries
