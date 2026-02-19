# gophish-lab

# 1. Pull Repo
```bash
git clone https://github.com/CSC-IU/gophish-lab.git
```

# 2. Change Directory
```bash
cd gophish-lab-main
```

# 3. Compose Docker File
```bash
docker-compose up -d
```

# 4. Find Password to Mailhog
Container name will be in logs.

```bash
docker logs {container name} | grep "User: admin"
```
