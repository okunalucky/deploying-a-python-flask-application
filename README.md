# deploying-a-python-flask-application
- Launch an instance (amazon linux 2023, t2.micro) and call it python - app
- Set up the key pair, vpc and security group, add port 8080 and 5000 to the inbound rules


  <img width="1314" height="330" alt="Image" src="https://github.com/user-attachments/assets/1670bfca-cc7a-4f14-a0f5-9cb670c5fc60" />

- Navigate to the advanced and paste the code below in the tab for userdata
```sh
sudo dnf install docker -y
‎sudo hostnamectl set-hostname docker
sudo systemctl start docker
sudo systemctl enable docker
‎sudo usermod -aG docker ec2-user
‎‎sudo su - ec2-user
```
- Install Git

```sh
sudo dnf install git -y
```
- Clone the repo using
```sh
git clone https://github.com/Solavisetech-Team/python-flask-app
```
<img width="645" height="245" alt="Image" src="https://github.com/user-attachments/assets/bf10b702-a353-4cb6-82f5-ba979ef0a705" />


- Run the following codes
```sh
ls
cd python-flask-app/
ls
docker build -t app.py .
docker images
```


<img width="1301" height="518" alt="Image" src="https://github.com/user-attachments/assets/057ee1ab-1a22-4f83-be88-1257dd84fd99" />


- To deploy the application, run the command below
```sh
docker run --name app.py -d -p 8080:5000 app.py
```

<img width="1140" height="166" alt="Image" src="https://github.com/user-attachments/assets/34761b4d-0ae6-4bed-a71f-dfac725ce739" />

-To view the application, navigate to your browser and run the public ip address:8080

<img width="548" height="139" alt="Image" src="https://github.com/user-attachments/assets/f31efbf6-7326-4901-92b6-1a5a818244d8" />



