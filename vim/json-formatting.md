Formatting JSON
---------------

Calling the following in a buffer (assuming it's filled with ugly json)

    :%!jq

will format it better.

The underlying TIL here is the use of :%<command> which operates on the entire
buffer/selection, including external commands. Previously only ever used this
for search and replace.
