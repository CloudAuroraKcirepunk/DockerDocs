# Docker Utils Commands

**PostgreSQL Simple**
```powershell
docker run -dp 5432:5432 --name postgresql_container -e POSTGRES_PASSWORD=admin -e POSTGRES_USER=admin postgres
```

**PostgreSQL With Volume**
```powershell
docker volume create postgresql_volume
```

```powershell
docker run -dp 5432:5432  --name postgresql_container -e POSTGRES_PASSWORD=admin -e POSTGRES_USER=admin -v postgresql_volume:/var/lib/postgresql/data postgres
```

**MongoDb**
```powershell
docker run -dp 27017:27017 --name mongodb_container -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=admin mongo
```

**Redis**
```powershell
docker run -dp 6379:6379 --name redis_container redis
```

**Jenkins**
```powershell
docker run -d -p 8081:8080 -p 50000:50000 --name jenkins_container -v jenkins_volume:/var/jenkins_home jenkins/jenkins:lts-jdk17
```
