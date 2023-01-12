# Some very basic things to do in bash
Syntax: command_name -options argument

Separated by **space** - make sure to correctly place them

Command usually ends with a new line or semicolon

Here, you will see `code` with grey background - you can try this on the command line.

## simple navigation on the command line
`cd data` - change directory

`cd ..` - go one directory upwards

`ls` - list files

`mkdir newd` - make directory

`cp fileA.txt fileB.txt` - copy file

Caution: files are irreversibly overwritten if they already exist!

`mv fileA.txt fileC.txt` - move file

`rm fileC.txt` - remove file

`pwd` - print working directory



## Tricks
The wildcard: \* - The asterisk can be used instead of everything

`ls file*`

Autocomplete: use the TAB key to autocomplete unique stuff

Quotation marks need to be plain text quotation marks: \' or \"

Avoid things such as “ or ´ - uninterpretable!

Store information in objects:

`stuff="weird random stuff"` - an object with the letters is created, can be called with dollar sign: $

now try `$stuff` and a command called `echo`: `echo $stuff`



## Looking at files
`less fileA.txt` – look at file 

`cat fileA.txt` – concatenate = print file line by line to the command line

`wc fileA.txt` – word count of file 

`wc -l fileA.txt` – line count of file

`head fileA.txt` – print first 10 lines of file

`head -n 3 fileA.txt` – print first 3 lines

`tail fileA.txt` – print last 10 lines of file

`tail -n 3 fileA.txt` – print last 3 lines of file



## Now we grep and cut and sort and pipe some things
We grab/grep:

`grep "apple" fileA.txt`

`grep -v "apple" fileA.txt`

`grep -c "apple" fileA.txt`

What is happening?

We cut:

`cut -f2-3 fileA.txt`

`cut -f2-3 -d " " fileA.txt`

And here?

`grep -v "apple" fileA.txt | cut -f2-3 > fileE.txt`

And what is this?

We sort:

`sort fileA.txt`

`sort -n fileA.txt`

`uniq fileA.txt`

`sort fileA.txt | uniq`

What is happening there?

Finally, we can define input and output. Not always required, but sometimes necessary:

`cat fileA.txt | grep -v "apple" - - 2> error.txt | cut -f2-3 > fileE.txt`

Standard input: the input a program takes (from the pipe? or a file?)

Standard output: where to put the output (into the command line? to a file?)

Standard error: where to put any error messages (usually, on the command line)

![image.png](attachment:f965a0c8-8fa2-423f-9577-289bef36dea4.png)



## Loops 
`for num in 1 2 3; do echo $num; done`

If you have the same task more than once, you loop!

## Regular expressions
Sequence of characters to specify search pattern

For example, in grep (but also other tools)

Common types

`|` = or (note: not a pipe here!!)

`.` = any character

`^` = starting position

`$` = end position

`[ ]` = defined ranges, e.g. any digit \[0-9\], some letters \[acde\]

Examples

`grep -E "apple|pear" fileA.txt` = any line with “apple“ or “pear“

`grep -E "[aoi]pple" fileA.txt` = any line with “apple“ or “opple“ or “ipple“

`grep -E ".pple" fileA.txt` = any line with any character followed by “pple“

`grep -E "^3" fileA.txt` = any line starting with “3“


## Compression
Important for large files. But it means you often cannot just run the same commands.

Cryptic parameters:

`tar -zxvf files.tar.gz`

![image.png](attachment:8bb20fab-b7dd-47a5-8918-07e32b2e1326.png)


## More of this stuff: awk
A small programming language that is useful for filtering data, even complex and line by line. For example, genotype data where each line is one position in the genome.

We only get the third column here:
`awk '{ print $3 }' fileA.txt`

More complex:

`awk '$2=="apple" { print $3 }' fileA.txt`

`awk 'length($2)==4 { print $2,$3 }' fileA.txt`



