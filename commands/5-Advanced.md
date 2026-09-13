# Level 19
./bandit20-do <command>

# Execute a command with the privileges of bandit20.


# Level 20
nc -l -p 1234

# Listen on a specific port.

nc localhost 1234

# Connect to a local port.


# Level 21
# Cron-related commands/concepts
cat /etc/cron.d/<job>
# Inspect a cron job configuration.


# Level 22
# Cron script analysis
cat /etc/cron.d/<job>
cat <script>

# Read and analyze the cron job and its script.


# Level 23
# Create a temporary directory
mktemp -d

# Create a temporary directory.

# Execute a script
bash <script>

# Run a shell script.


# Level 24
# Network connection
nc localhost 30002

# Connect to a service on a specific port.


# Level 25
ssh -i <private_key> -p 2220 <user>@<host>

# SSH using a private key.


# Level 26
stty rows 5

# Change terminal row size.

more <file>

# Open a file using the "more" pager.

v

# Open the current file in Vim from "more".

:!<command>

# Execute a Linux command from inside Vim.


# Level 27
git clone <repository>

# Clone a Git repository.

git clone ssh://<user>@<host>:2220/<path>

# Clone a Git repository using SSH.


# Level 28
git log

# View Git commit history.

git log --oneline

# View compact commit history.

git show <commit>

# View details of a specific commit.

git branch -a

# View all local and remote branches.

git checkout <branch>

# Switch to another branch.

git remote -v

# View remote repository information.
