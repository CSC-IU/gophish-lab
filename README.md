# gophish-lab

# 1. Pull Repo
```bash
git clone https://github.com/CSC-IU/gophish-lab.git
```

# 2. Change Directory
```bash
cd .\gophish-lab\
```

# 3. Compose Docker File
```bash
docker-compose up -d
```

# 4. Find Password to Mailhog
Linux/Mac
```bash
docker logs gophish_demo | grep "User: admin"
```
Windows
```bash
docker logs gophish_demo | Select-String -Pattern "User:admin"
```

# 5. Open Mailhog in Browser
```
http://localhost:8025
```

# 6. Open GoPhish in Browser
```
https://localhost:3333
```
