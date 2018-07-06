# bash-scripts
My collection of bash scripts and aliases for automating server commands.

## Replace the Spaces and Return Characters of any sh or bash Files
``sed $'s/\r$//' ./bash_filename.sh > ./bash_filename.unix.sh && source ./bash_filename.unix.sh``

## Sample Aliases
``alias tlr-setup="cd /ebs/www/laravel-project/ && sudo chown -R user setup.unix.sh && sudo chmod -R 777 setup.unix.sh && ./setup.unix.sh user lr-worker:*"``

## [Rewrite Git History]: <https://help.github.com/articles/changing-author-info/>
* Create a fresh, bare clone of your repository:
	``
	git clone --bare https://github.com/user/repo.git 
	cd repo.git
	``
* Copy and paste the script, replacing the following variables based on the information you gathered:
	``
	OLD_EMAIL
	CORRECT_NAME
	CORRECT_EMAIL
	``
* Save and Run the script: ./git-author-rewrite.sh
* Push the corrected history to GitHub: ``git push --force --tags origin 'refs/heads/*'``
* Clean up the temporary clone:
	``
	cd ..
	rm -rf repo.git
	``