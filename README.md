# Zip

Zip

Description

People are pursuing enhancing the file compression rate for long time. Recently, someone proposed an algorithm, which only rearrange the file, not compressing file. But we can achieve much more compressoin rate than ever before after adapting the file using this algorithm. 
We define a string's head as its first character, and tail as its last character. 
Now I'll show you how this algorithm works: there is a string ,said S, consists of n characters. First we construct n strings from it, the i'th string is obtained by moving the head of the i-1'th string to its tail. Then we sort the n strings by their heads, if two strings' heads are equal, sort them by the two heads' position in S. After sort, we can obtain a new string S' consists of the tails in the sorting result strings. 
It's obvious that the length of S' is also n, and it contains all the characters in S. At last, you must output S' and the position of the first character of S in S',an integer,p. 
For example: 
S: example 

1. construct n strings 
example 
xamplee 
ampleex 
mpleexa 
pleexam 
leexamp 
eexampl 

2. Sort these string as mentioned 
ampleex 
example 
eexampl 
leexamp 
mpleexa 
pleexam 
xamplee 
3. Construct S' by the tails of sorting results and output 
xelpame               S'

7                     p

Since the occurrence of the same English words is high-frequent, we can achieve high compression rate of S'. Although this algorithm utilizes English word's occurrence characteristics, people also find this algorithm does well for most filetype's compression. 
You task is simple, it's not compressing the file. You should construct S' from S and reconstruct S from given S' and p. 

Input

The input contains only one case, the first line is a char C indicating which job you should do. 

When C is 'A' , that means you should construct S' from S. The next line is an integer n(1 <=n<=10000), the length of S. The third line is the string S. 

When C is 'B' , that means you should reconstruct S from S'. The next line is an integer n(1 <=n<=10000), the length of S'. The next line is the string S', the fourth line is an integer p. 
Output

When C is 'A' , You should output two lines, the first of which is S' and second is p. 

When C is 'B' ,You should output just one line containing the string S. 

Sample Input

Sample input 1:
A
7

example

Sample input 2:
B
7

xelpame
7

Sample Output

Sample output 1:

xelpame
7
Sample output 2:
example
