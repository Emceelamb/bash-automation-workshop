# Adding your scripts to your path

The `PATH` is an important concept when working on the command line. It is a list of driectories which tell your operating system where to look for programs. When calling scripts typically you have to give the exact path location such has `/home/<usr>/bin/scriptname` but if you add the entire path to the folder to your `PATH` you can call the script from anywhere with just `scriptname`.
## Mac OS X

1. Open the `.bash_profile` file in your home directory (for example, `/Users/your-user-name/.bash_profile`) in a text editor.
2. Add export `PATH="your-dir:$PATH"` to the last line of the file, where your-dir is the directory you want to add.
3. Save the `.bash_profile` file.
4. Restart your terminal.

## Linux

1. Open the .bashrc file in your home directory (for example, `/home/your-user-name/.bashrc`) in a text editor.
2. Add export `PATH="your-dir:$PATH"` to the last line of the file, where your-dir is the directory you want to add.
3. Save the `.bashrc` file.
4. Restart your terminal.

* Pro tip: you can hot reload your .bashrc with `source ~/.bashrc`

