# gophish-lab
Run GoPhish using a Mailhog SMTP Loopback in Docker

## Installation

#### 1. Pull Repo
```bash
git clone https://github.com/CSC-IU/gophish-lab.git
```

#### 2. Change Directory
```bash
cd .\gophish-lab\
```

#### 3. Compose Docker File
```cmd
docker-compose up -d
```

#### 4. Find Password to Mailhog
Linux/Mac
```bash
docker logs gophish_demo | grep "User: admin"
```
Windows (Powershell)
```bash
docker logs gophish_demo | Select-String -Pattern "User:admin"
```
<img src="https://i.ibb.co/vChg2XXX/image.png" alt="test" width="950"/>

---
## Usage
### 1. Open Mailhog in Browser
```
http://localhost:8025
```

#### 2. Open GoPhish in Browser
```
https://localhost:3333
```
Login with the password you got from the logs, username ``admin``.

#### 3. Setup Sending Profile
<img src="https://i.ibb.co/0yHyDQG4/image.png" alt="sending_profiles" width="800"/>

Settings for Sending Profile:
``` yaml
SMTP From: {Anything@anySite.com} # Since we're using mailhog, this doesn't matter
Host: mailhog:1025 # This is the loopback address mailhog's SMTP server listens on
Username: None
Password: None
```
Now test the profile:

<img src="https://i.ibb.co/RpbpW3y6/image.png" alt="test" width="400"/>
<img src="https://i.ibb.co/KxdRn7yk/image.png" alt="test" width="400"/>

#### 4. Check Mailhog for the Example Email
Go to mailhog in a browser if you haven't already:
```
http://localhost:8025/
```

Check to see if your email delivered:

<img src="https://i.ibb.co/6RhtfcV9/image.png" alt="test" width="1550"/>

#### 5. Figure the rest out by yourself
If you can't do this, you probably shouldn't be phising in the first place.

Good Luck :)
