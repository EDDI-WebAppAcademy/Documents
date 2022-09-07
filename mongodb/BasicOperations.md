# DB 생성

```make
use sensor
show dbs
db.sensor.insert({"mpu6050": 14.2})
show dbs
```

# root 유저 생성

```make
use admin
db.createUser({user: "root", pwd: "456123", roles: ["userAdminAnyDatabase"], mechanisms: ["SCRAM-SHA-1"]})
```

# 일반 사용자 생성

```make
use sensor
db.createUser({user: "eddi", pwd: "eddi@123", roles: ["readWrite"], mechanisms: ["SCRAM-SHA-1"]})
```

# 유저 리스트 보기

```make
db.getUsers()
```

# 유저 삭제

```make
db.dropUser("name")
```

