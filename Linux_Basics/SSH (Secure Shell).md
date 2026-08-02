SSH (Secure Shell) is a secure protocol that lets you log in to and control a remote computer over the internet using an encrypted connection.

## Real Example

You create an EC2 instance with the IP address:

```
54.210.100.25
```

Then, from your laptop, you run:

```
ssh -i mykey.pem ubuntu@54.210.100.25
```

- `ssh` → Start a secure connection.
- `-i mykey.pem` → Use your private key for authentication.
- `ubuntu` → Username on the remote Linux machine.
- `54.210.100.25` → IP address of the EC2 instance.


Your Laptop
      │
      │ SSH Connection 🔐
      ▼
+------------------------+
|   Amazon EC2 Instance  |
|     Ubuntu Server            |
+------------------------+