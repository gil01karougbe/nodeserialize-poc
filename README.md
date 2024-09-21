# nodeserialize-poc
Insecure Deserialization to RCE in NodeJS

This is a vulnerable node js App that uses the node-serialize package for serialization and deserialization.

## How work The app
the /notes endpoint is protected and a user must log in the app before accessing it. others are not
when the user log in the application send to the browser a cookie that is checked when accessing the /notes endpoint.
if the cookie is valid the access is allowed if not it's denied.


## Run the App
#### Use the image
```sh
docker pull lig10/nodeserialize-poc
docker run -p 3000:3000 nodeserialize-poc
```

#### Build the image
```sh
git clone https://github.com/gil01karougbe/nodeserialize-poc.git
cd nodeserialize-poc
docker build -t nodeserialize-poc .
docker run -p 3000:3000 nodeserialize-poc
```

## Access the App
![image](https://github.com/user-attachments/assets/6c626314-1cad-4ddc-ab61-85d3d5633814)

Use the Following creds to login:
```sh
admin:admin
user:iloveyou!
```
## Exploitation
Modify the rce.js to add you IP address
```
node rce.js
```
![image](https://github.com/user-attachments/assets/e5fee4fe-341c-43e5-b5f3-3a2ee9316fe2)
![image](https://github.com/user-attachments/assets/4985f0b6-d346-4028-8feb-865d60bd5da2)
![image](https://github.com/user-attachments/assets/c0f3be6b-a5b2-4103-a308-31b64efe31d4)

