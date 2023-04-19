# Working with SSH Keys

When connecting to an SSH Server the first time the client typically doesnt have the servers public key. This key is used to authenticate the server and prevent a meddler-in-the-middle attack. In Ansible this results in an error, but one that we can easily and securely solve. Let's dig in. 

