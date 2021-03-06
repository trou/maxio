# Collection of tools for the reMarkable paper tablet

## rM2svg

Convert a .lines file to an svg file

    usage: rM2svn [-h] -i FILENAME -o NAME

    optional arguments:
      -h, --help                      show this help message and exit
      -i FILENAME, --input FILENAME   .lines input file
      -o NAME, --output NAME          prefix for output file
      --version                       show program's version number and exit

## exportNotebook

Convert a Notebook to a PDF file: Searches for the most recent Notebook whose visible name contains NAME, and export it as PDF file.

    usage: exportNotebook NAME

    $ exportNotebook Jour
    Exporting notebook "Journal" (4 pages)
    Journal.pdf

### SSH configuration

The `exportNotebook` script assumes a USB connection. If you are connected via
WiFi, you can add an entry to your `~/.ssh/config`:

    host remarkable
           Hostname 10.11.99.1 # or any other IP
           User root
           ForwardX11 no
           ForwardAgent no
