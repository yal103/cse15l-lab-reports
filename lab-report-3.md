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

### 3. -C[num] (Before and After Lines)

This `grep` command option prints the searched line and `num` before and after the result.

</br>

**Example 1:**

    $ grep -C1 "expression" ./technical/biomed/rr74.txt
            following sever hypoxia has been reported in rats [ 4, 13,
            14, 15, 16]. Less is certain about the expression of NOS in
            the murine lung following hypoxia, with previous reports [
    -- 
            determined using 18 S rRNA primers/probes (Applied
            Biosystems) and eNOS, iNOS and nNOS expression determined
            using the primer/probe sequences shown in Table 1.
    --
    ...
    
This command displays all the lines in the file `rr74.txt` located in the `./technical/biomed/` directory along with the line before and after the matching lines.
This is useful to for getting context of any particular matched line.


**Example 2:**

    * grep -C2 "creative" ./technical/911report/*.txt
    ./technical/911report/chapter-3.txt-    dedicated to trying "to evaluate the threat of a terrorist attack in the United
    ./technical/911report/chapter-3.txt-    States by the Usama bin Ladin network."107The CSG members were "urged to be as
    ./technical/911report/chapter-3.txt:    creative as possible in their thinking" about preventing a Bin Ladin attack on U.S.
    ./technical/911report/chapter-3.txt-    territory. Participants noted that while the FBI had been given additional resources
    ./technical/911report/chapter-3.txt-    for such efforts, both it and the CIA were having problems exploting leads by
    
This command displays all the lines in the .txt files located in the `./technical/911report/` directory along with two lines before and after the matching lines. In this case, only one line in the .txt files located in `./technical/911report/` contains the pattern _"creative"_.
Again, this is useful to get the context of a matched line.
</br></br>
>Source used: <https://www.geeksforgeeks.org/grep-command-in-unixlinux/> \
</br>

---

### 4. -v (Inverting Pattern Match)

This `grep` option displays the lines that do not contain the specified pattern.

</br>

**Example 1:**

    $ grep -v "a" ./technical/government/Media/Wingates_winds.txt
    
    
    
    
    BY BRAD BENNETT
    is strong enough.
    funded by Sept. 30, 2003.
    million.
    
    
    
    
    // The empty lines are actually lines in the .txt file

This command displays the lines in the file `Wingates_winds.txt` located in `./technical/government/Media" that do not contain the letter _"a"_.
This is possibly useful when you want to find lines where you don't want a certain word.


**Example 2:**

    $ grep -v "a" ./technical/biomed/rr74.txt
    
    
    
    
            Introduction
            immunohistochemistry.
            
            
            
                Mice
                
                
                Exposure environments
            ...
 
This command finds all the lines in the file `rr74.txt` lcoated in `./technical/biomed/` that do not contain the letter _"a"_.
Again, this is possibly useful when you want to find lines where you don't want a certain word or character.
</br>
</br>
ヽ(･∀･)ﾉ
