Formatting JSON
---------------

Calling the following in a buffer (assuming it's filled with ugly json)

    :%!python -m json.tool

will format it using python's json tool.

The underlying TIL here is the use of :%<command> which operates on the entire
buffer/selection, including external commands. Previously only ever used this
for search and replace.
