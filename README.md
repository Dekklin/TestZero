# Instructions

## Hello World

### Creating Git Repo
1) Head to your page on Git, if you need directions getting there...
    * top right profile icon drop down menu
    * 'Your Repositories'
2) Green button 'NEW'
3) For right now I named my Repo TestZero, I made mine public, I added a readme for no particular reason, just good practice.

### Connecting PC to Git (Cloning)
1) Head over to the repo you just created; Green button again should say Code
2) Copy the link to get ready to clone your repo
3) Once you have the link copied, open bash on your pc
4) using bash commands, direct yourself to a location in your pc you would like this repo to exist
    * If you create a folder named 'TestZero' then clone inside it, it will create another folder called TestZero where the repo will actually live (I prefer this way no reason for it)
    * Commands used : **ls** (lists files/folders) :: **cd ..** (backs out to parent folder) ::  **cd *filename*** (ex: cd TestZero) **mkdir** (makes a folder/directory)
5) type 'git clone *hyperlink*
    * Essentially you created a project on git, and now you're connecting that specific location on your computer to github; meaning if you accidently move a photo  of an embarassing picture of you in a bubble bath in this folder, and then git add; commit; push; ......  the internet now has that photo. Thanks.
6) Great you just downloaded an empty project! Now its time you create useful files, and  upload them to Git!

### Creating Useful Files
1) First thing GITIGNORE
    * A .gitignore essentially tells your **git add** to not add files that is in EVERY C# program.... files that contain the 1's and 0's on strings and int's and what makes VSC do stuff.... Its like 20mb of stuff and can get way bigger the more programs you add. It also makes **Git push** like 10 seconds faster so theres that.
2) So I'm a little not too sure about what pushpinder wants us to do here but I'm just going to combine my goto with her methods and see how she likes it
3) So in bash make your way to that folder, you should see a Readme and the .gitignore
4) In Bash type 'dotnet new console'
    * This tells bash to install files that are mandatory for a C# project to work within a console/terminal
    * By the way I like to think of bash as like a terminal thats connected with the internet, VERY COOL!! (dont answer that in an interview)
5) Now pushpinder is doing something odd, I think.... I believe she's setting up a solution, which is used for building multiple programs in one project. But right now it looks like we're only going to have one project in the sln (solution) to me thats like making a folder to hold 1 file.
6) In Bash type *dotnet new sln
    * optional for visual purposes type **ls** in bash
7) In Bash type 'dotnet sln File_Name.sln add File_Name.csproj'
    * this attaches that specific project to the solution
    * NOT EXACTLY SURE IF IT DOES THIS BUT I BELIEVE THIS ALLOWS YOU TO USE 'USING obj' AT THE TOP OF A CLASS FROM OTHER PROJECTS
8) Seems like pushpinder also wants us to seperate our files so make directories (mkdir) called 

### Last Touches to Hello World
1) In bash I like to change my directory so I see the folder everything is in
2) In bash type 'Code FOLDER_NAME'
    * this should open VSC and on the left have all the files you just created
3) Time to fill that gitignore before we upload a bunch of none-sense
4) Juniper showed us this site [gitignore.io](https://www.toptal.com/developers/gitignore)
    * I add CSharp, VisualStudioCode, and DotnetCore (we have hardly used DotnetCore but why not build the habit?)
    * The Link i got [click me](https://www.toptal.com/developers/gitignore/api/csharp,visualstudiocode,dotnetcore)
5) Copy the entire page of spaced out hooplah and paste it in the gitignore on VSC
6) Save, and move on to your Program.cs
    * SOMEONE CORRECT ME, I swear she had a way to automatically populate this with the basic Main method but I don't remember, I added it myself. Simply Look at an old repo and copy that, make sure to add 'using System'
    * I like to add a Console.WriteLine("Hello World"); in my Program.cs Main method and run my project at least once to get a hello world in the console to confirm it works           **dotnet run FILE_NAME.csproj**
7) In bash **'dotnet build FILE_NAME.sln'**

### Upload to github
1) In bash direct yourself to your base solution folder
2) In bash type 'git status'
    * this tells you anything that is different from the last time you git pull'd or cloned or updated your local git bash with github : this means if some other coworker uploaded code in the branch you were working in and you try to upload bash is gonna yell at you.
3) In bash type your favorite 3 commands **git add .**    **git commit -m "heartfelt  message about why you're uploading this code"**     **git push**
4) When you come back to work, make sure you work in a DIFFERENT BRANCH THAN MAIN. The only reason I did this is because all we're doing is a hello world. If it doesnt work its not really a program to begin with.
    * **'git checkout -b testBranch'**
