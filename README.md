# Dash to Dock Enhanced
![screenshot](https://github.com/micheleg/dash-to-dock/raw/master/media/screenshot.jpg)

## A dock for GNOME Shell with window previews
This extension is based on the popular Dash to Dock extension and keeps the same idea of moving the dash out of the overview and turning it into a dock.

## Screenshot
![Window previews screenshot](https://raw.githubusercontent.com/thiagoneo/dash-to-dock-enhanced/main/media/Screenshot.png)

The screenshot above demonstrates the enhanced window preview popup when hovering over an application icon.

The main enhancement in this version is support for window previews/popups, showing thumbnails and window details when hovering over icons.

For more information about the original Dash to Dock, visit [https://micheleg.github.io/dash-to-dock/](https://micheleg.github.io/dash-to-dock/).

## Installation from source

The extension can be installed directly from source, either for testing the latest development version or for local development.

### Build Dependencies

To compile the stylesheet, you need a SASS implementation. This extension supports `dart-sass` (`sass`), `sassc`, and `ruby-sass`.

We recommend using `dart-sass` (`sass`) or `sassc`, since `ruby-sass` is deprecated.

By default, the build tries to use `sassc`. To change this behavior, set the `SASS` environment variable to `dart` or `ruby`.

```bash
export SASS=dart
# or...
export SASS=ruby
```

### Building and installing

Clone the repository or download the desired branch. A simple Makefile is included.

Then use `make` to install the extension into your home directory. A shell reload is required with <kbd>Alt</kbd> + <kbd>F2</kbd> <kbd>r</kbd> <kbd>Enter</kbd> on Xorg; on Wayland you may need to log out and log back in.

The extension must be enabled with the *gnome-extensions-app* (GNOME Extensions) or via *dconf*.

```bash
git clone https://github.com/micheleg/dash-to-dock.git
make -C dash-to-dock install
```

If `msgfmt` is not available on your system, you will see an error like the following:

```bash
make: msgfmt: No such file or directory
```

In that case, install the `gettext` package from your distribution's repository.

## Bug reporting

Bugs should be reported to the GitHub issue tracker: [https://github.com/micheleg/dash-to-dock/issues](https://github.com/micheleg/dash-to-dock/issues).

## License
This GNOME Shell extension is distributed under the terms of the GNU General Public License,
version 2 or later. See the `COPYING` file for details.
