Find And Replace
====

### Unix Commands
    find . -type f -exec sed -e 's/Test_Dbv3/TestDbv3/g'  '{}' +

The aptly named find command finds files. Here, we're finding files in the current working directory (.) that are files (-type f). Using these files, we're going to -exec a command: sed. + indicates the end of the command and that we'd like to replace {} with as many files as the operating system will allow.

sed will go file-by-file, line-by-line, executing commands we specify. The command we're giving it is s/Test_Dbv3/TestDbv3/g, which translates to “substitute matches of the regular expression Test_Dbv3 with the text TestDbv3, allowing multiple substitutions per line”. The -i.bak means to replace the original file with the result, saving the unmodified version with the filename suffixed with .bak.

Can replace `'` with `"` in the sed statement `'s/FIND_STRING/REPLACE_STRING/g' => "s/FIND_STRING/REPLACE_STRING/g"`
source: [stackoverflow](http://stackoverflow.com/questions/17119685/unix-command-to-replace-all-instances-of-a-string-in-every-file-in-a-folder)
