# deploying-a-python-flask-application
- Launch an instance (amazon linux 2023, t2.micro) and call it python - app
- Set up the key pair, vpc and security group, add port 8080 and 5000 to the inbound rules


  <img width="1314" height="330" alt="Image" src="https://github.com/user-attachments/assets/1670bfca-cc7a-4f14-a0f5-9cb670c5fc60" />

- Navigate to the advanced and paste the code below in the tab for userdata
```sh
dnf install docker -y
systemctl start docker
systemctl enable docker
```
  
