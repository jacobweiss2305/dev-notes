# Local setup for multiple github repositories

1. Create keys
   ```
   ssh-keygen
   ```
2. Add keys to github accounts as ssh key
3. Activate ssh-agent
   ```
   eval ssh-agent -s
   ```
4. Add private keys to ssh-agent
   ```
   ssh-add ~/.ssh/key
   ```
5. Create a config file
   ```
   cd ~/.ssh/ && touch config
   ```
6. Add to config file
   ```
    # Personal account, - the default config
    Host github.com
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa
        
    # Work account-1
    Host github.com-work_user1    
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa_work_user1
   ```