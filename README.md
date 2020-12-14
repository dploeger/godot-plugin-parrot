# Parrot - a simple dialog plugin

## Introduction

Parrot is a very simple and linear dialogue plugin that shows subtitles
for various characters differentiated by a specific color and plays
voice files.

It supports calculating the length of one line based on the soundfile
length or on a custom reading speed when no sound file exists.

There's also an importer to allow creating Dialog resources by reading
CSV files.

## Usage

Parrot enables a singleton called Parrot, that you can configure using

    Parrot.configure(theme)

The theme is used for the subtitle overlay.

If you don't need subtitles, just turn them off:

    Parrot.subtitles = off

To actually play a dialog, run

    Parrot.play(dialog)

The dialogs are created using DialogResource files. (see the API-Doc
for more details

Parrot emits line_finished and dialog_finished signals when a line or 
the complete dialog was finished.

## Importing

Because creating dialog resources can be tedious, Parrot includes a CSV-
importer that creates resource files based on a dialog csv file.

Use the [provided template file](addons/parrot/template.txt) for your
dialog files and import them using Project/Tools/Import Dialog.

## API-Docs

The following API-Docs are available:

* [CharacterResource](docs/CharacterResource.md)
* [DialogLineResource](docs/DialogLineResource.md)
* [DialogResource](docs/DialogResource.md)
* [Importer](docs/Importer.md)
