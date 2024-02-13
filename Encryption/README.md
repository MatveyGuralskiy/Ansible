# 🔒 Encryption files and how to use it

## 👨🏻‍💻 Ansible Vault

To create encrypt file:                  

ansible-vault create (FILE NAME).txt


To view the file like 'cat' command:     

ansible-vault view (FILE NAME).txt


To edit him:

ansible-vault edit (FILE NAME).txt


To reset your password:

ansible-vault rekey (FILE NAME).txt


To encrypt some file:

ansible-vault encrypt (FILE NAME).txt


To decrypt him:

ansible-vault decrypt (FILE NAME).txt


To run encrypt playbook:

ansible-playbook (PLAYBOOK NAME).yml --ask-vault-pass


To run encrypt playbook without asking the password (Use from some txt file with your password inside):

ansible-playbook (PLAYBOOK NAME).yml --vault-password-file (FILE NAME).txt


To encrypt variable inside playbook:

for example you have inside playbook variable 'password' with secret password inside him

copy the secret password and enter to this command to encrypt them

echo -n "(YOUR PASSWORD)" | ansible-vault encrypt_string

now copy all message, from vault and cut to your playbook variable 'password'


Now you can run the playbook with encrypt variable:

ansible-playbook (PLAYBOOK NAME).yml --ask-vault-pass


## 📁 All files inside directory Files
