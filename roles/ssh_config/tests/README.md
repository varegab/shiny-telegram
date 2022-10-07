This test does the following:

- It is looping through the 'settings' dictionary which contains the key-value pairs we want to replace.
- Searching for the key in the 'test_sshd_config' and replacing its whole line with the key and the value (only if it is not commented out).

Run:
  ansible-playbook test.yml