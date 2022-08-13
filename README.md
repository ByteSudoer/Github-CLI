# GitHub-CLi
Shell Script as a wrapper for the GitHub CLI tool.

### Installing dependencies
- git 
- fzf
- GitHub-CLI 

To install for **Debian/Ubuntu** Based Distros: 
```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh git fzf
#### To Upgrade:
sudo apt update
sudo apt install gh
```
To install for **Arch** Based Distros: 
```bash
sudo pacman -S github-cli git fzf
```

### Setup Account
Authenticate and link GitHub-CLI with your Github Account:
```bash
gh auth login
```
And follow the instructions to complete the process

### Start Using it
Mark the script as executable and add it to your PATH
```bash
chmod +x GitCli 
ln -sf <your_current_dir>/GitCli $HOME/.local/bin
```
> $HOME/.local/bin should be created and added to your PATH by editing your .bashrc (instead of adding it to your /usr/bin as root)

#### Available Options
  ```bash
    ##########################################################
    Available Options For Script.
      -i --info       Display Infos about Repositories
      -h --help       Display Description And Options For this Script
      -l --list       List Repositories Linked to account
      -c --create     Create Repository and Clone it to current path
      -f --fuzzy      Fuzzy search for diff in current repo
      -d --delete     List Repositories Linked to account
      -s --search     Search and Output Informations about a Repository
    ##########################################################
```
Now you can start using it in your shell 👍
