First we need to configure our ssh_key in github.

## Generating a new SSH key

**1.- Copy & Paste the text below, substituting in your GitHub email address** in the console.

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

This creates a new ssh key, using the provided email as a label.
```
Generating public/private rsa key pair.
```

**2.- When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.**
```
Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
```

**4.- At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases"**
```
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
```

## Adding your SSH key to the ssh-agent

**1.- Ensure the ssh-agent is running:**

`eval $(ssh-agent -s)`{{execute}}

**2.- Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.**
`ssh-add ~/.ssh/id_rsa`{{execute}}

## Add a new SSH key to your GitHub account

**1.- Copy the SSH key to your clipboard.**
`cat /root/.ssh/id_rsa.pub`{{execute}}

It would be something like follow.
```
ssh-rsa AAA...== your_email@example.com
```
Select it and copy to the clipboard.

## Add the ssh key to github

Open this link in a new tab [https://github.com/settings/keys](https://github.com/settings/keys)

Then clic in `New SSH key`

There put a Title, I call it `Katacoda SSH`

And paste the id_rsa.pub content **Previously copied to the clipboard** into **Key**

To finish it clic in `Add SSH Key`