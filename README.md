# places-cli

Places is a command-line tool for managing folder bookmarks and places in Linux desktop environments. These are different names for folder shortcuts shown in File Manager applications and in Save and Load dialogs.

When adding or removing the bookmarks, it is done for KDE, GTK-2, and GTK-3 at the same time to affect all applications, regardless of the desktop environment they were built for.

By Lars Ole Pontoppidan, 2026

### Usage

```text
places list
places add "TITLE" "PATH"
places remove "TITLE"
```

### Example

```text
$ places add "My Project" .
Added: 'My Project' at: '/home/lars/development/my_project' to KDE user places
Added: 'My Project' at: '/home/lars/development/my_project' to GTK-3.0 bookmarks
Added: 'My Project' at: '/home/lars/development/my_project' to GTK-4.0 bookmarks
$ places remove "My Project"
Removed: 'My Project' from KDE user places
Removed: 'My Project' from GTK-3.0 bookmarks
Removed: 'My Project' from GTK-4.0 bookmarks
```

## Installation

The Python module lxml is required. Install it system-wide with:

```bash
sudo apt install python3-lxml
```

Install the script by copying to a folder in PATH and making it executable:

```bash
git clone github.com/larspontoppidan/places-cli
cd places-cli
sudo cp places /usr/bin/
sudo chmod +x /usr/bin/places
```

## Uninstallation

```bash
sudo rm /usr/bin/places
```

