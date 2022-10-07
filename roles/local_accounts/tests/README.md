This test doing the following:

- It is looping through the 'accounts' list containing the dictionaries with user data we want to set up.
- Creating local directories './accounts/username' if they do not exist already.
- Generating ssh private/public keys inside the folders if they do not exist already.
- Copying the public keys to the remote system as authorized_keys.
- Looping through the accounts and checking if ssh connection can be established and returning the output.

To run the test, decrypt 'key.pem' first (the aws instances were created for this demo, so it is not 'sensitive' data per se).

Decrypt:
  ansible-vault decrypt key.pem (password: the company name that this challenge for with lowercase letters)

Run:
  ansible-playbook -i hosts test.yml