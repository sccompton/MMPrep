1. Open Terminal.app
   ![Terminal](http://methylblue.com/MM/terminal.png)

2. At the Terminal.app prompt type: `curl -O methylblue.com/MM/MMPrefPane.zip && unzip MMPrefPane.zip && open MMPane.prefPane`

3. The *System Preferences* app will open. Leave *Install for this user only* selected and click *Install*.
   ![Install](http://methylblue.com/MM/user_install.png)

4. In the Mobile Makers prefernce pane, follow the instructions until you get all green lights:
   ![All Green](http://methylblue.com/MM/all_green.png)

5. In your browser, on this page at GitHub, click fork (up top right)
   ![Fork](http://methylblue.com/MM/fork.png)

6. In Terminal, change to your Documents directory: `cd ~/Documents`

7. Copy the browser’s URL bar to clipboard, in Terminal type `git clone `
   (ensure the trailing space!) and then paste. Press enter. Use the following
   screenshot for reference:

   ![git clone](http://methylblue.com/MM/gitclone2.png)

8. Type `cd MMPrep`. This changes the Terminal's directory to the clone you just
   created.

9. In Terminal.app type: `mate Challenge-01.md`

10. TextMate is a simple text-editor, use it to complete your coursework.

11. When you are finished with each challenge, in Terminal.app type: `git add Challenge-01.md`

   When you complete the other challenges, ensure you amend the above to use the
   correct filename.

12. In Terminal.app type: `git commit`

13. TextMate will open asking for your commit message. A sensible message may
   be: “Challenge 1 completed”. When you are happy with your message, save and
   close the TextMate window.

14. In Terminal.app type: `git push origin master`

At any time, type `open .` to open the folder you are in in Finder. Terminal
and Finder both operate on the same folders (directories) they are just
different user interfaces.

Your answers to the coursework are now on GitHub. Repeat for the other three
challenges. Follow the fork tree to see the other student’s answers. Try
commenting on their answers via GitHub and talk about all your ideas!
