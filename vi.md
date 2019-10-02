# vi tutorial

It's necessary to learn at least one text-based editor well. The `nano` editor is one of the simplest for basic editing (opening, editing, saving, searching). However, for the power user in a text terminal, there is no substitute for Vim (`vi`), the hard-to-learn but venerable, fast, and full-featured editor. Many people also use the classic Emacs, particularly for larger editing tasks. (Of course, any modern software developer working on an extensive project is unlikely to use only a pure text-based editor and should also be familiar with modern graphical IDEs and tools.)

## start

![Image of vi](/images/vi.png)


## Quitting Vim
This is the very first thing I had to learn while using Vim. There are plenty of times when I screwed up. Learning how to quit Vim saved me countless times.

Type `:q` and hit Enter.

![Image of quite](/images/quite_vim.png)

*Note: Vim won’t let you out without this method. **Ctrl + C** doesn’t work.*
 
## Navigating the file

Vim offers a really complicated set of ways you can use to navigate the text file.


The easiest way to navigate through the file is by using the arrow keys.

Vim allows using other keys to navigate the file like the arrow keys.

**h** – One character to the left

**l** – One character to the right

**k** – Go up

**j** – Go down

**w** – One word to the right

**b** – One word to the left

**0** (zero) – Beginning of the current line

**$** – End of the current line

*Note: Be careful about the case of the keys.*

## Editing the file

Navigate to your desired place on the text and hit “i”. This will tell Vim to enter the “Insert mode”.

![Image of insert](/images/insert.png)

Once you’ve done your necessary edits, you can exit the “Insert” mode by pressing **Ctrl + C** or **Esc**. 

## Saving the file
Before saving the file, it’s necessary to understand how Vim handles the work.

When you’ve opened a text file with Vim, you’re actually accessing a temporary copy of the original file. If you’re satisfied with your changes and decide to save, only then Vim will write the edited file over the original file.

There are benefits to this approach. It prevents the original file from unwanted corruption. Vim allows multiple users to edit the same file at the same time, so using a temporary file helps to avoid conflicts. Vim saves the temp file so that you can recover your work if there happen to be some interruptions.

To write the buffer to the file, enter **:w**.

![Image of w](/images/w.png)

It’s also possible to combine the write command with quit.

**wq**

![Image of wq](/images/wq.png)


This will write the buffer to the file and exit the editor.

Another interesting feature Vim offers is writing the current buffer at the end of another file. In short, you can append the current edit to another file.

`:w >> <filepath>`

This command can also be paired with the quit command.

`:wq >> <filepath>`

Sometimes, you might just want to discard the current buffer and start from scratch. I screwed up the sudoers multiple times, especially with Vim. This method just saved me a lot of headaches. Tell Vim to exit without writing the buffer to the file.

`:q!`

## Searching

As a legendary piece of software, it would be a shame if there would be no search functions! Using Vim, it’s easy to find out where your target phrase is. This is the structure that Vim requires to perform the search function.

`?<search_string>`

![Image of search](/images/search.png)

Notice that there’s no gap in-between the question mark and the search string. After typing the search term, hit Enter.

*I search for 'vi' here*

Now, when you run this, you’re stuck with the only search result. Is that acceptable? No! Tell Vim to navigate to previous/next search matches!

`n` – Find the next match
`N` – Find the previous match

## Replacing content
Vim is not limited to basic search features. Vim allows sed-like command for performing the replace operation.

The syntax of the command goes something like this:

`:%s/<search_string>/<replace_string>/<replacement_behavior>`

As of the replacement behavior, these 2 ones are quite common.

`g` – Perform the replacement on every occurrence of the search string.

`gc` – Same as “g” but will ask for confirmation before making the change.

## Occurrence count
Just like the previous example, it’s also possible to only highlight and count the occurrence of the search string instead of replacing it. This is a better one than the classic search function.

The syntax for the operation would be

`:%s/<search_string//gn`

![Image of count](/images/count.png)

![Image of count_result](/images/count_result.png)

Notice the `gn` part? It’s responsible for overriding the substitute behavior.

## Final thoughts

Vi is very powerful, google it for more!