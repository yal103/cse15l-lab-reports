# Lab Report 3 - Researching Commands
**Yangyang Liu \
CSE 15L Section B02 \
PID: A17360266**

## Researching Commands
I have chosen do research on the `grep` command.
> I will be using the files and directories in `./technical` to show my examples. It is found [here](https://github.com/ucsd-cse15l-s23/stringsearch-data).

</br>

---

### 1. -i (Case-insensitive Search)

This `grep` command option allows you to make a search for a pattern, regardless of the letter case.

</br>

**Example 1:**

    $ grep -i "CrEaTiVe" ./technical/911report/*.txt
    ./technical/911report/chapter-3.txt: creative as possible in their thinking" about preventing a Bin Ladin attack on U.S.

This command searches for the text "CrEaTiVe" in all .txt files in `./technical/911report/`,ignoring the case of each letter. \
It is useful when searching for words that have inconsistent capitalization. 


**Example 2:**

    $ grep -i "ERROR" ./technical/plos/journal.pbio.0020047.txt
          painful is the fact that this book is filled with factual errors, glib and misleading
          accurately later in the book, but that is a weak excuse for this early error.
          
This command searches for the text "ERROR" in `./technical/plos/journal.pbio.0020047.txt`, ignoring the case of each letter. \
Again, it's useful if you want to found a keyword that may be capitalized differently throughout the files.
</br></br>
>Source used: <https://www.geeksforgeeks.org/grep-command-in-unixlinux/> \
</br>

---

### 2. -c (Display Match Count)

This `grep` command option allows you to search for the number of lines that matches the pattern.

</br>

**Example 1:**

    $ grep -c "file" ./technical/911report/*.txt
    ./technical/911report/chapter-1.txt:1
    ./technical/911report/chapter-10.txt:1
    ./technical/911report/chapter-11.txt:0
    ./technical/911report/chapter-12.txt:2
    ./technical/911report/chapter-13.1.txt:0
    ./technical/911report/chapter-13.2.txt:50
    ./technical/911report/chapter-13.3.txt:12
    ./technical/911report/chapter-13.4.txt:15
    ./technical/911report/chapter-13.5.txt:15
    ./technical/911report/chapter-2.txt:0
    ./technical/911report/chapter-3.txt:4
    ./technical/911report/chapter-5.txt:1
    ./technical/911report/chapter-6.txt:1
    ./technical/911report/chapter-7.txt:1
    ./technical/911report/chapter-8.txt:2
    ./technical/911report/chapter-9.txt:1
    ./technical/911report/preface.txt:0
    
This command displays the number of lines in each .txt file in the `./technical/911report/` that contains the pattern _"file"_.\
This is useful if you want to get a quick overview of how many matches are found. 


**Example 2:**

    $ grep -c "report" ./technical/biomed/rr74.txt
    14

This command displays the number of lines in `rr74.txt` located in the `./technical/biomed/` directory.
Again, this is useful if you want to know how many lines in a file contain the word you are looking for.
</br></br>
>Source used: <https://www.geeksforgeeks.org/grep-command-in-unixlinux/> \
</br>

---
