HOW TO - c9.io with Github
--------------------------

1. Create a  new repository on gihub
	...
          …or create a new repository on the command line
 
		echo "# devisemailer" >> README.md
		git init
		git add README.md
		git commit -m "first commit"
		git remote add origin https://github.com/ingafter60/devisemailer.git
		git push -u origin master

2. > create a new app on c9
   > git init
   > git add .
   > git commit -m "Initial commit"
   > git remote add origin https://github.com/ingafter60/devisemailer.git
   > cat ~/.ssh/id_rsa.pub
	  ...
          copy the ssh key

3. Got to github, create a new ssh key
   > icon user
   > settings
   > create anew

4. Push to github
   > git push -u origin master
   ...
   Username for 'https://github.com': ingafter60
   Password for 'https://ingafter60@github.com': makeitoverGithub60~`
   Counting objects: 65, done.

5. Removing the origin
   > git remote -v (checking)
   ...
   origin  https://github.com/ingafter60/devisemailer.git (fetch)
   origin  https://github.com/ingafter60/devisemailer.git (push)
   > git remote rm origin (remove origin)
   > git remote -v (checking)

6. Update your IDE with SSH access
   > git remote add origin git@github.com:ingafter60/devisemailer.git
   > git remote -v
   ...
   origin  git@github.com:ingafter60/devisemailer.git (fetch)
   origin  git@github.com:ingafter60/devisemailer.git (push)
   Testing
   > make some changes on Gemfile 
     # MAKING SOME CHANGES FOR TESTING PURPOSES
   > git add -A
   > git commit -m "Making some changes on Gemfile for git testing"
   > git push origin master
   > go to github + refresh the repository (https://github.com/ingafter60/devisemailer)
     ... 
	Gemfile 
	Making some changes on Gemfile for git testing 
	3 minutes ago 

Section 5:  App Time - Creating Public Pages

    14. Hello World So 1996
    
        Ways to start server
        
        First Way:
        > start server: rails server -p $PORT -b $IP + enter
        > click the pop up link to open the browser
        > stop server: ctrl + c 
        
        Second Way:
        > click Run Project button (on top bar menu)
        > click the pop up link to open the browser
        > stop server: click RED button (left side of the terminal)
        
        Making pages
        > keep server running
        > create new branch: git checkout -b pages 
        > craete root route 
        > refresh the server, will see error (Routing Error uninitialized constant PagesController)
        > rails g controller pages
        > refresh browser (Unknown action, The action 'index' could not be found for PagesController)
        > create index action in controller
        > create an index.html.erb file in views/pages dir
        > refresh the browser
        
    15. Git Time
        
        > git add -A
        > git commit -m "Created pages controller with index action"
        > git push origin pages 
        > git checkout master 
        
    16. Generation Control - Generating Controllers
        > rails destroy controller pages
        > rails g controller pages index contact about
        > create root route
        > About Route:
          you can make route like this for contact page: get 'hello', to: 'pages#contact'
          https://devisemailer-ing.c9users.io/hello
        > undo About Route:
        > Git time:
        > git add -A 
        > git commit -m "Created pages controller with index about and contact action"
        > git push origin pages  
        > git checkout master
        > refresh :)
   