# THIS NEED EDIT

<div> - groups content 
<section> - groups related content 
<article> - groups independent, self-contained content
  Wrap Radio Buttons in a fieldset Element for Better Accessibility
  <form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
  
  Generate and Install a SSH Key Pair

SSH keys offer a secure manner of logging into a server without the need of a password.

In a nutshell, this depends upon you generating a public and a private SSH key pair. The private key is kept on your PC (and should be guarded carefully). The public key is copied over to the server you wish to connect to.

SSH keys are a complex subject and as such, out of the scope of this tutorial. If you’d like to find out more, I recommend looking for a dedicated tutorial (such as this one).
Generate the Keys

On *nix systems (Windows users see the next section), you can generate your key pair with the following command:

ssh-keygen -o -b 4096 -t rsa

The -o option instructs ssh-keygen to store the private key in the new OpenSSH format instead of the old (and more compatible PEM format). This is advisable, as the new OpenSSH format has an increased resistance to brute-force password cracking.

The -b option is used to set the key length to 4096 bits instead of the default 1024 bits for security reasons.

In the following dialogue you will be required to answer a couple of questions:

    Where to save the newly generated key pair
    Which passphrase to use

Here you can accept the default location and leave the passphrase blank by pressing Return.

ssh-keygen will then output a summary of what it has done:

Generating public/private rsa key pair.
Enter file in which to save the key (/home/jim/.ssh/id_rsa):
Created directory '/home/jim/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/jim/.ssh/id_rsa.
Your public key has been saved in /home/jim/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:sx5uJeVdH/cT/1+GxsSWYzmjf5hUaE33f/e57EbqBfY jim@fitz
The key's randomart image is:
+---[RSA 4096]----+
|                 |
|                o|
|               +o|
|          .  .+==|
|        So . =@oB|
|        .oo o*+BB|
|        oo  ..*EX|
|       o..   +=+=|
|       .o   ..+=+|
+----[SHA256]-----+

Copy the Public Key to the Ubuntu Server

To copy the public key to the Ubuntu server use:

ssh-copy-id -i ~/.ssh/id_rsa.pub jim@192.168.178.66

Where ~/.ssh/id_rsa.pub is the path to your public key, taken from the output above. And where jim@192.168.178.66 should be altered to reflect your details.

The command will run and you should be asked for your server password. Enter it, then attempt to log into the server like so:

ssh perror@192.168.1.101

This time you should be in without a password.
  
  thanks to https://hibbard.eu/install-ubuntu-virtual-box/
