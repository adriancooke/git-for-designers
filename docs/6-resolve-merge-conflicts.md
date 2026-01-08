# 6. Resolving merge conflicts

[Git for designers](../README.md) → 6. Resolving merge conflicts

⚠️ Document status: **Draft**

## When do merge conflicts occur

In a simple case, merge conflicts can occur, when another person has made a change to a line in a file that has been merged that you have also edited and changed something different on that line in your branch. For example, the other person changed the word that you were making into a link.

Merge conflicts usually occur after you have started on a new branch and the original project branch (likely the main branch) you are trying to merge into has newer changes in it.

## Resolution options

To resolve a merge conflict you have options.

* You could create a new branch with the latest changes from the [original project branch after syncing the changes](4-sync-from-original.md) and make your changes again in that branch. This means you have to redo your work.
* You can resolve the merge conflict using GitHub's web editor to help you resolve the conflict, which we will show below. This means no redoing your work but this option is only available for simple conflicts and not for complex ones.
* You can use a local editor that has a tool to resolve merge conflicts. This means no redoing your work, you can resolve complex conflicts, but it is an advance topic.

## Resolving a simple conflict

*Task: Resolve a merge conflict in a open pull request you created in [step 3](3-open-pull-request.md).*

1. Visit the open pull request you have created.
2. Near the bottom of your pull request, confirm you see a message stating 'This branch has conflicts that must be resolved' and there appears 'Resolve conflicts' button that is not grayed out. If there is no message and no 'Resolve conflicts' button then there are no conflicts so you can skip this process.
3. If the 'Resolve conflicts' button is grayed out then the conflict is complex and cannot be resolved in GitHub's web editor but can be done locally.
4. If the 'Resolve conflicts' button is available then click on it. You will be taken to a screen where you are shown conflicting files.
5. Select a conflicting file and you will be shown the text and lines that are in conflict with conflict markers <<<<<<<, =======, >>>>>>> appearing above, between, and below respectively. Example:

    ```text
    <<<<<<< your-branch
    The quick brown fox jumps over the [lazy](https://en.wikipedia.org/wiki/The_quick_brown_fox_jumps_over_the_lazy_dog) dog
    =======
    The quick brown fox jumps over the sleepy dog
    >>>>>>> main
    ```

    You will also be given links to 'Accept current change', 'Accept incoming change', and 'Accept both changes'.

    The line under '<<<<<<<', is your changes from your branch and will be the line selected if you click 'Accept current change'. The line above '>>>>>>>' is the change in the original project branch and will be the line selected if you click 'Accept incoming change'.

6. You can resolve the conflict by the clicking the appropriate link.

    Note that clicking either of the 'Accept' options means you are going either with your change or the original change. Clicking 'Accept both changes' will add both lines to the file, one after the other. All the links will also automatically remove the conflict markers.

7. If you want to combine the changes, in our example use the new word for the link you added. Then you have to manually edit the line to make that change and then delete all the markers manually from that line. This is also if you want to change the line differently.
8. Once that conflict is resolved, use the 'Prev' and 'Next' buttons to send the cursor to the next conflict, if another one exists.
9. Once all conflicts are resolved, click 'Mark as resolved'.
10. If you have another file with a conflict, select the next file in the list of conflicting files.
11. Once you have resolved all conflicts in all files, click 'Commit merge'. If you want to cancel the changes, refresh the page or close it without clicking 'Commit merge'.
12. Navigate back to the pull request to verify that your changes are still valid and that there are no other conflicts. Then proceed to merge the pull request like in [step 3](3-open-pull-request.md).

## Complex conflicts

Complex conflicts are editing files that have been renamed/deleted, changing files like images, and more. Recommend to check out ['About merge conflicts topic in GitHub documentation to learn more'](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/about-merge-conflicts).

## Topic navigation

*	This topic: **6. Resolving merge conflicts**
*	Previous topic: [5. Working with media](5-working-with-media.md)
