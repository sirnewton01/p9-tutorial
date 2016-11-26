Document Editing
===

Last time, we learned about how to navigate between documents using hyperlinks. Text documents can serve a variety of purposes in Plan 9. They can be used for written documents like this one. They can be generated from the result of running a command or showing a directory listing. You can even write a document as a log of the commands that you ran during a session as a history or log of what you were doing. Any text shown in a window can be edited, even if it is output from a command. This makes Plan 9 quite unique.

Run this command to create a new file. It echos text and redirect the output to the file sample.txt

    echo 'SAMPLE CONTENTS' > sample.txt

Navigate to your new file using this hyperlink.

    sample.txt

You can add whatever contents you want in this file. Try adding a hyperlink back to this document using the file name document-editing.md. Whenever a panel is modified, the resize box on the top-left is filled in with a blue colour indicating that there are unsaved changes. Run the put command to save the file.

Try adding some misspelled words to your files and save it. You can run a spell check on the file running this command:

    spell < sample.txt

The spell command will print out words that it could not find in the dictionary in a new window. See spell(1) for more details. Now that we know which words are misspelled. Let's find them in your document. There is that one line at the top of the window. Try typing a space and then one of the misspelled words at the top of the window for your document. Now, right-click on that word.

Notice that it highlights an instance of the word within the document and moves the mouse cursor there as well. You can right click again to find another instance. This is really useful when you want to navigate through all instances of a selected text in a document. Since spell only reports one entry for all instances of the same misspelled word this will help us to find and correct all of them.

You may have noticed that this line at the top of the window is customizable! You can add additional commands at the top so that you can middle click to run them easily. You can put snippets of text there to easily find instances. You can do the same thing inside your document but then it would get saved with the rest of the text and you would need to scroll to find the command/snippet.

If you want to rename your file you can also edit the file name/path at the top, and run put to save it under a new location. Note that this doesn't delete the original. You could even do this to a command output if you want to save the output of the command to a file. Try running this command and save its output window to a file. Edit the file path to at the top of the window to /tmp/output.txt. Write in the Put command after Look and then middle click it to save.

	seq 1 50

In this section you have seen how to create new documents using either a command or from the output of a command. Right-clicking on a selected snippet of text will find the next occurrence of that snippet in the current file if there are any. You can easily save a copy of the contents of a window under a different file name by modifying the path at the top of the window and running the put command on it. Commands and snippets of text can be put at the top of the window so that you don't modify the document and they are always easily accessible.

To learn more about acme you can check the manual page acme(1).

The next section will focus on the Plan 9 filesystem.

[Plan 9 Filesystem]( filesys.md )
