# Github_Keeping_Streak
Guide &amp; code to keep streak in github

This code with make a commit at 00:00 UTC every day for your streak to count on github. All green gardener 🧑‍🌾  
In the `daily-commit.yml` provided you have to change:
* `git config --global user.name "Your_name"` with your actual name
* `git config --global user.email "Your_email"` with your actual email
* `git push https://x-access-token:${{ secrets.PAT_TOKEN }}@github.com/Your_username/Your_repository_name.git` with your actual repository url

The use of the private token is in case you make the repository private; you need a Personal Access Token (PAT) to run Github Actions on a private repository.

To make a private token you have to go to your repository settings -> Developer settings -> Personal access tokens -> tokens (classic)

When selecting the Scopes, select the `repo` and `workflow`, the expiration you can set it to 90 days (just general good practice, just in case it gets leaked)

Once you have the PAT go to your repository settings -> Secrets & variables -> Actions -> Secrets -> New repository secret, name it PAT_TOKEN and paste it

Finally, make sure under the Actions -> General -> Workflow permissions, the `Read and Write permissions` is activated. 

Just clone this repository and do all this changes and you will have it working. 

And voilà you have an automated streak in github with no warnings as of September 2024. If you have any questions, feel free to ask me. 

⭐ Star this repository if you found it useful 


