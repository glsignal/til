# Opening vim with multiple buffers preloaded

There are several options for opening vim with multiple files already loaded:

    $ vim file1 file2     # opens buffers that can be navigated through by using :next and :prev
    $ vim -p file1 file2  # opens buffers in separate tabs that can be navigated through by using :tabnext and :tabprev
    $ vim -O file1 file2  # opens buffers in side by side (use -o for stacked) split mode

This can be useful for a variety of things, e.g. if you need to open a subset of the files in your current directory:

    $ vim -O $(ls *.md)
