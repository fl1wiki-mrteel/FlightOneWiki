# FlightOneWiki - Contribute to this Wiki

## Todo list

Check out the Todo list -> [TodoList](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/Contribute/Todolist.md) <-


## Using Git as an user (Non Admin)

1. Start by creating a Github account
2. browse to https://github.com/fl1wiki-mrteel/FlightOneWiki and press the "Fork"-button on the top right side of the page
3. Install Git (<a href='https://git-scm.com/downloads' target='_BLANK'>https://git-scm.com/downloads</a>)
4. Install a text editor with GIT support, like Visual Studio Code (<a href='https://code.visualstudio.com/download' target='_BLANK'>https://code.visualstudio.com/download</a>)
5. Create a folder on your drive, lets call it "FlightOneWiki"
6. Open the folder and right-click "Git Bash Here"
![Image of gitbash](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/gitbash.PNG)
7. write "git clone https://github.com/your github alias/FlightOneWiki" and press enter
![Image of gitclone](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/gitclone.PNG)
8. Now you should have the whole FlightOneWiki downloaded
9. Open your text editor and open the "FlightOneWiki" folder
10. Now you should be able to edit and commit changes to your forked Github repo.
11. Create a Pull request and merge your fork with the primary repo

[How to Fork and submit a pull request](https://jarv.is/notes/how-to-pull-request-fork-github/)

## Using web browser as an Collaborator

1. Start by creating a Github account
2. Ask us about getting collaborator rights (Admin)
3. Navigate to the page you want to edit
4. Press the "pencil" on the top right corner of the wiki page
5. Do your editing and save


## Using Git as an Collaborator

1. Start by creating a Github account
2. Ask us about getting collaborator rights (Admin)
3. Install Git (<a href='https://git-scm.com/downloads' target='_BLANK'>https://git-scm.com/downloads</a>)
4. Install a text editor with GIT support, like Visual Studio Code (<a href='https://code.visualstudio.com/download' target='_BLANK'>https://code.visualstudio.com/download</a>)
5. Create a folder on your drive, lets call it "FlightOneWiki"
6. Open the folder and right-click "Git Bash Here"
![Image of gitbash](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/gitbash.PNG)
7. write "git clone https://github.com/fl1wiki-mrteel/FlightOneWiki" and press enter
![Image of gitclone](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/gitclone.PNG)
8. Now you should have the whole FlightOneWiki downloaded
9. Open your text editor and open the "FlightOneWiki" folder
10. Now you should be able to edit and commit changes to the Github repo.

## Using Git with fork

Install Git (<a href='https://git-scm.com/downloads' target='_BLANK'>https://git-scm.com/downloads</a>)
```
#Once you have forked the main repo and changes has accured to the main repo. You will have to fetch the changes done in the master/main repo and merge before doing a pull request

git remote -v
git remote add upstream https://github.com/fl1wiki-mrteel/FlightOneWiki
git fetch upstream
git merge upstream/main // or // git merge upstream/master
#Push changes to your fork
git push origin main // or // git push origin master

```

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/GITHUB_FETCH.JPG)
![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/GITHUB_MERGE.JPG)

### Now you can do your changes and create a pull request from github web

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/GITHUB_PULLREQ.JPG)
![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/GITHUB_PULLREQ_002.JPG)
![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/GITHUB_PULLREQ_003.JPG)



# External links
- [How to use Github (Youtube)](https://www.youtube.com/watch?v=iv8rSLsi1xo)
- [How to fetch changes in master repo](https://www.youtube.com/watch?v=-zvHQXnBO6c)
- [Markdown/Formatting text](https://guides.github.com/features/mastering-markdown/)
- [How to Fork and submit a pull request](https://jarv.is/notes/how-to-pull-request-fork-github/)

