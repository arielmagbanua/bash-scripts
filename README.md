# bash-scripts
My collection of bash scripts and aliases for automating server commands.

## Replace the Spaces and Return Characters of any sh or bash Files
``sed $'s/\r$//' ./bash_filename.sh > ./bash_filename.unix.sh && source ./bash_filename.unix.sh``
