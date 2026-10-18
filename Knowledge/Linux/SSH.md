### Create an SSH key
#### Generate a key
`ssh-keygen -t ed25519 -C "your_email@example.com"`

#### Copy the key contents from teh console
`cat ~/.ssh/id_rsa.pub`(or the specific filename if you used a custom name)

#### Connect with ssh
`ssh name@address`