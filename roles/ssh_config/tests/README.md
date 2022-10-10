'test.yml':

- It is looping through the 'settings' dictionary which contains the key-value pairs we want to replace.
- Searching for the key in the 'test_sshd_config' and completely removes it.

Run:
  ansible-playbook test.yml

'test_remote.yml':

- It is looping through the 'settings' dictionary which contains the key-value pairs we want to replace.
- Searching for the key in the '/etc/ssh/sshd_config' and completely removes it if it's not commented out.
- Append key-value pair to the file.
- Restarting the sshd service.

To run the test, decrypt 'key.pem' first (the aws instances were created for this demo, so it is not 'sensitive' data per se).

Decrypt:
  ansible-vault decrypt key.pem (password: the company name that this challenge is for with lowercase letters)

Run:
  ansible-playbook -i hosts test_remote.yml

