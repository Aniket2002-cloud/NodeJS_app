* Following The Steps Off NodeJS app hosting *

1) sudo yum update

2) sudo yum install nodejs -y

3) node -v

4) cd NodeJS_app/

5) nano package.json

6) nano index.js

7) npm install

8) Add Port No 3000 in Security Groups

9) npm start

10) sudo yum install nginx -y

11) sudo service nginx start

    sudo nano /etc/nginx/nginx.conf

     * add the following proxy pass *
    
     location / {
        proxy_pass http://127.0.0.1:3000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;                     
        proxy_set_header X-Forwarded-Proto $scheme;
    }

13) sudo service nginx reload


