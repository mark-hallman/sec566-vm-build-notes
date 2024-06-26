# sec566 - ssh Keys for J01 Branch


## Generate new ssh keys for the J01 branch
```
ssh-keygen -t ed25519 -f ~auditor/.ssh/sec566_workbook_id_ed25519 -N '' -C 'auditor@sec566_win_audit_J01'
```

## Generate the known_hosts file
```
ssh-keyscan github.com >> ~/.ssh/known_hosts
```
Create the ssh config file and add the following content:

```
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/for589_workbook_id_ed25519

```
```
## Update file and folder permissions
```
chmod 700 ~/.ssh 
chmod 600 ~/.ssh/config 
chmod 600 ~/.ssh/sec566_workbook_id_rsa
chmod 644 ~/.ssh/sec566_workbook_id_rsa.pub
chmod 644 ~/.ssh/known_hosts
```

## Add the Public Key to the J01 branch in the GitHub Repo
1. Create a new file in the J01 branch, in the workbook/keys folder named `J01_ssh_authorized_keys`.  
2. `cat ~/.ssh/sec566_workbook_id_rsa.pub`to see the public key.
3. Copy and paste that content into the `J01_ssh_authorized_keys` file created above.
4. Save the file which will commit the changes and send the key to GitHub

## Test the ssh key

```
ssh github.com
```
If the key was successfully send to GitHub when you committed the key, you will see the message below.  If you get errors about permissions, then the key has not been sent to GitHub or there is some other config issue.
```
Hi sans-course-workbooks/sec566-J01-workbook! You've successfully authenticated, but GitHub does not provide shell access.
Connection to github.com closed.
```
## Clone the repo to the workbook dir
Once you can successfully `ssh github.com` without errors, the EWB can be cloned into the VM.

Remove or rename the existing `/var/www/html/workbook` dir.
```
rm -fr /var/www/html/workbook
```
```
git clone ssh://github.com/sans-course-workbooks/sec566-j01-workbook /mnt/c/SANS/workbook
```
git clone ssh://github.com/sans-course-workbooks/for578-h11-workbook /var/www/html/

Open the EWB in a browser and confirm the the correct version of the EWB is being displayed.  

git clone ssh://github.com/sans-course-workbooks/for578-h11-workbook /var/www/html/