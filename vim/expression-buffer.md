_Very_ satisfying vim trick to perform simple calculations in the file you're working on (in this case calculating the GST).

```
Given a line
some_value="10.0"

(in normal i.e. not insert mode)
vi"      //to select the thing you're wanting to use for the calculation
c        //change it; i.e. delete and enter insert mode
Ctrl-R = //begin entering the calculation into the expression register (your command input area should show something like `=` and allow you to type)
Ctrl-R " //dump the value that was deleted just before (command area should show `=10.0`)
//add *0.15 to the end of the expression (making it look like `=10.0*0.15`)
//Hit enter and you're golden
```

Then put all of this into a macro using `q` and that's some easy-mode transforms you can apply without leaving vim.

Now with handy screencast link: http://vimcasts.org/episodes/simple-calculations-with-vims-expression-register/
