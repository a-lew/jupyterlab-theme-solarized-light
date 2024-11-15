# JupyterLab Theme Solarized Light

![License](https://img.shields.io/github/license/AllanChain/jupyterlab-theme-solarized-dark.svg)

The theme was originally created by [Joses W. Ho](https://github.com/josesho) and [Jae Hee Lee](https://github.com/dschaehi) in this [gist](https://gist.github.com/dschaehi/ff6d30e6779a683053a1f078af178cdb).

## Screenshot

<img width="960" alt="Screenshot" src="https://github.com/AllanChain/jupyterlab-theme-solarized-dark/assets/36528777/de6dd210-d92b-4015-9da9-92dd07a4a9a9">

## Requirements

- JupyterLab >= 4.1.5

Note that the toolbar text color will be illegible for JupyterLab 4.1.0 - 4.1.4.
See [this GitHub issue](https://github.com/jupyterlab/jupyterlab/issues/15786) for more details.


## Install

To install the extension, execute:

```bash
pip install git+https://github.com/a-lew/jupyterlab-theme-solarized-light.git
```

To install with pipenv, make sure to specify the package name with `#egg` identifier:

```bash
pipenv install -e git+https://github.com/a-lew/jupyterlab-theme-solarized-light.git@main#egg=jupyterlab-theme-solarized-light
```

## Uninstall

To remove the extension, execute:

```bash
pip uninstall jupyterlab_theme_solarized_light
```

Apply the theme by checking `Settings -> Jupyterlab Theme -> Jupyterlab Solarized Light`

To enable theme scrollbars, in JupyterLab, either

- navigate to `Settings -> Advanced Settings Editor -> Theme`, and add `"theme-scrollbars": true` to `User Preferences`
- OR check `Settings -> Jupyterlab Theme -> Theme Scrollbars`

## Contributing

### Development install

Note: You will need NodeJS to build the extension package.

The `jlpm` command is JupyterLab's pinned version of
[yarn](https://yarnpkg.com/) that is installed with JupyterLab. You may use
`yarn` or `npm` in lieu of `jlpm` below.

```bash
# Clone the repo to your local environment
# Change directory to the jupyterlab_theme_solarized_dark directory
# Install package in development mode
pip install -e "."
# Link your development version of the extension with JupyterLab
jupyter labextension develop --overwrite .
# Rebuild extension Typescript source after making changes
jlpm run build
```

You can watch the source directory and run JupyterLab at the same time in different terminals to watch for changes in the extension's source and automatically rebuild the extension.

```bash
# Watch the source directory in one terminal, automatically rebuilding when needed
jlpm watch
# Run JupyterLab in another terminal
jupyter lab
```

With the watch command running, every saved change will immediately be built locally and available in your running JupyterLab. Refresh JupyterLab to load the change in your browser (you may need to wait several seconds for the extension to be rebuilt).

By default, the `jlpm build` command generates the source maps for this extension to make it easier to debug using the browser dev tools. To also generate source maps for the JupyterLab core extensions, you can run the following command:

```bash
jupyter lab build --minimize=False
```

### Development uninstall

```bash
pip uninstall jupyterlab_theme_solarized_light
```

In development mode, you will also need to remove the symlink created by `jupyter labextension develop`
command. To find its location, you can run `jupyter labextension list` to figure out where the `labextensions`
folder is located. Then you can remove the symlink named `jupyterlab-theme-solarized-light` within that folder.

### Packaging the extension

See [RELEASE](RELEASE.md)
