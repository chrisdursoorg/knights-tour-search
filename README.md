knights-tour-search
===================

Small program to search and print out chess knights tour solutions

To build simply:

>  gcc -c knight.cpp -o knight

Then print out the following with the help command as illustrated below
or you can just start a knights search without the -h option.

By starting the knight down a particular path you can have the program
explore that particular knight's tour subspace (e.g. > ./knight 0 11 58 15 
note the coordinates below).  

A bit more documentation and references are at 

http://durso.org/knights_tour/

> ./knight -h

knights [OPTIONS] [SEARCHPATH]
knights crossing program (v1.1, 12Feb12), by chris durso, ref. www.durso.org

OPTIONS

-v
--verbose       print more information
-g=#
--grid=#        use grid of size # (default 8 for 8x8). Minimum 5, Maximum 11.
                    Note no white spaces!

SEARCHPATH

The optional SEARCHPATH is a sequence of positive numbers not longer than
grid x grid in length, and thier numerical values in the range of 0 to
grid x grid and non repeating. Each number is sequence must be a legal
chess knights move from the previous number in the SEARCHPATH.

COORDINATE SYSTEM

The bottom left hand corner is noted as 0 and the increment first
goes up and wraps to the right.  The bottom left is 0, the top
left is grid -1, and the top right square is grid x grid -1.

   7  15  23  31  39  47  55  63
   6  14  22  30  38  46  54  62
   5  13  21  29  37  45  53  61
   4  12  20  28  36  44  52  60
   3  11  19  27  35  43  51  59
   2  10  18  26  34  42  50  58
   1   9  17  25  33  41  49  57
   0   8  16  24  32  40  48  56

