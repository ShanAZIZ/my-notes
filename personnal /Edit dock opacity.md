# Adjusting the transparency of the dock

## -- Method 1: using dconf

The setting is available, but not exposed to the user. You can see a range of system settings in a utility 'dconf', which you need to install first:
```
sudo apt install dconf-editor
```
After installation, run dconf by searching "dconf". It has become a little bit more complicated than it used to be, because first, you need to enable changing your opacity. For this, navigate to org.gnome.shell.extensions.dash-to-dock and change the setting transparency-mode to 'FIXED'

The setting that controls opacity is background-opacity. Click on the setting to change it to a value between 1 (full opacity) and 0 (no opacity). Thus, set to 0.2 for 80% transparency.

## -- Method 2: terminal

As a faster and safer way, you may also change that setting using a terminal command. First enable custom colors:

```
gsettings set org.gnome.shell.extensions.dash-to-dock transparency-mode 'FIXED'
```

Then, to set transparency to 80%, issue the command

```
gsettings set org.gnome.shell.extensions.dash-to-dock background-opacity 0.2
```

Change 0.0 to any number between 0 and 1.

To reset to the default setting:

```
gsettings reset org.gnome.shell.extensions.dash-to-dock background-opacity
gsettings reset org.gnome.shell.extensions.dash-to-dock background-opacity
```

## -- Method 3: through Dash-to-dock settings

For completeness sake, you could also install the Gnome Shell extension Dash-todock. That extension exposes all its settings. Ubuntu dock, which is based on that same extension, uses the same settings and will be affected by your changes. Remember to disable one of the two extensions, or you will be running two docs.

Adjusting the transparency of the top bar

For this, you can, as before, use the Gnome Shell extension Dynamic Panel Transparency. Using the extension's options, you can tweak the transparency and transition speed to match that of your doc.