## Privesc

### ssh
If we find ourselves with write access to a users/.ssh/ directory, we can place our public key in the user's ssh directory at /home/user/.ssh/authorized_keys.

If we have read access over the .ssh directory for a specific user, we may read their private ssh keys found in /home/user/.ssh/id_rsa or /root/.ssh/id_rsa, and use it to log in to the server. If we can read the /root/.ssh/ directory and can read the id_rsa file, we can copy it to our machine and use the -i flag to log in

