# sd

## What is `sd`?

`sd` could stand for 'swap directories' or 'sed on directories'. It's another command like `z`, `bd` and
other commands you run in your shell to change quickly a directory.

![](https://raw.github.com/TaurusOlson/sd/master/img/sd.gif)


## Installation

    $ git clone https://github.com/TaurusOlson/sd ~/.sd
    $ source ~/.sd/sd


## Usage

Suppose you have this kind of tree:

    $ tree
    .
    ├── A
    │   ├── dataset1
    │   ├── dataset2
    │   └── dataset3
    └── B
        ├── dataset1
        ├── dataset2
        └── dataset3

    $ cd A/dataset1


`sd` allows you quickly jump from one source directory to a target directory by specifying their names.

Jump from `dataset1` to `dataset2`:

    $ sd dataset1 dataset2

Or simply:

    $ sd 1 2
    # you are now in path/to/A/dataset2

Jump from `A` to `B`:

    $ sd A B
    # you are now in path/to/B/dataset2


When only one argument is provided, `sd` assumes it is the source directory is
the current directory and the target directory is the first argument:

    $ sd dataset3
    # you are now in path/to/B/dataset3
