
Steps to connect Git with deepdish cluster
1. Make sure git CLI is installed
```bash
git --version

2. Initialize a git repo under your folder
```bash
cd \path\to_your_profile
git init

3. Configure Git with your github credentials
```bash
git config --global user.name "Your name on Github"
git config --global user.emal "Your sign-in email for Github"

4. Generate SSH keys on the cluster, set up paraphrase
```bash
ssh-keygen -t rsa -b 4096 -C "Your sign-in email for Github"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub

5. Add ssh key to your github
# Settings > SSH and GPG keys > New SSH key
```bash
ssh -T git@github.com

6. Initialize a repo on Github and push local work there
```bash
git remote add origin git@github.com:Komono123/HW1.repo

7. Add, commit, push, pull etc.
