# Lab Report 5
## Using the `less` command

1. `less -n fileName` This opens the file with a margin that shows line numbers.  
`less -N HistoryIndia.txt` would produce:  
![](https://i.imgur.com/1HYvjgd.png)
Another example is:  
`less -N HistoryDublin.txt`  
![](https://i.imgur.com/eqOS5xR.png)  
This is useful because it helps figure out where things are, for example, you're looking for something in line 14, you don't have to count all 14 lines.
2. `/(word)` While in the `less` window typing in `/(phrase)` will highlight the word or phrase that is being looked for.  
`less HistoryIndia.txt` followed by `/India` would produce:  
![](https://i.imgur.com/36nN7dn.png)  
Another example is:  
`less IntroMadeira.txt` followed by `/15th century`  
![](https://i.imgur.com/OAHQeLC.png)  
This is useful because it helps find words that you're looking for, which saves time.
3. `less --use-color -D[part of text][color] file` This opens a file and highlights a part of the text in a different color.  
`less --use-color -DSMc HistoryHawaii.txt` would produce:  
![]()  
Another example is:
`less --use-color -DuBc HistoryIndia.txt`  
![]()  
This is useful because it helps bold things, it makes it easier to look at.
4. `m[mark name]` When you open a `less` file you can type in the command `m[mark name]` so that you can mark a line.  
Typing in `less -J HistoryDublin.txt` and then `mA` would set a mark, like so  
![]()
You can go back to the mark by using `'A`
Another neat example is that you can have them with different colors and backgrounds like so  
`less --use-color -J -DMGw`
![]()
This is useful because marking a certain line will allow you go to back to the line again in the future without having to search for it manually.

## I used these two sites to find my information https://www.man7.org/linux/man-pages/man1/less.1.html and https://linuxhandbook.com/less-command/
